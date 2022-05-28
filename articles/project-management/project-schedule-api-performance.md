---
title: Projektiaikataulun ohjelmointirajapinnan suorituskyky
description: Tässä aiheessa on tietoja projektiaikataulun ohjelmointirajapintojen suorituskykyilmaisimista ja käytännöistä, jotka liittyvät tehostamiseen.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593838"
---
# <a name="project-schedule-api-performance"></a>Projektiaikataulun ohjelmointirajapinnan suorituskyky

_**Koskee seuraavaa:** Project Operations resursseihin/ei-varastoitaviin perustuville skenaarioille, lite-käyttöönotto - tarjouksesta proformalaskutukseen, Project for the web_

Tässä aiheessa on tietoja projektiaikataulun ohjelmointirajapintojen suorituskykyilmaisimista (API:en) ja käytännöistä, jotka liittyvät käytön tehostamiseen.

## <a name="project-scheduling-service"></a>Projektin aikataulutuspalvelu
Projektin aikataulutuspalvelu on usean vuokraajan palvelu, joka suoritetaan Microsoft Azure -palvelussa. Se on suunniteltu parantamaan vuorovaikutusta tarjoamalla nopean ja sujuvan kokemuksen, kun käyttäjät työskentelevät projekteissa. Tämä parannus saavutetaan hyväksymällä muutospyynnöt, käsittelemällä ne ja palauttamalla tulos välittömästi. Palvelu säilyy asynkronisesti Dataversen kanssa eikä estä käyttäjiä suorittamasta muita toimintoja.

Projektin aikataulutuksen ohjelmointirajapinnat käyttävät projektin aikataulutuspalvelua pyyntöjen suorittamiseen, jotka on kuvattu tarkemmin tämän aiheen myöhemmissä osissa.

Projektiaikataulun ohjelmointirajapinnat on suunniteltu siten, että niiden avulla voi käyttää seuraavia työrakenteen (WBS) entiteettejä:

  - Project
  - Projektin tehtävä
  - Projektitehtävän riippuvuus
  - Projektiryhmän jäsen
  - Resurssien delegointi
  
Sekä tilausten ulkopuolisia kenttiä että mukautettuja kenttiä tuetaan. Ellei toisin ole ilmoitettu, kaikkia yleisiä toimintoja, kuten luontia, päivitystä ja poistoa, tuetaan. Lisätietoja on ohjeaiheessa [Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen ja aikataulutusentiteettien suorittamiseen](schedule-api-preview.md).

Projektiaikataulun ohjelmointirajapintojen osana on lisätty työyksikkömalli. Tätä mallia kutsutaan OperationSet-joukoksi, ja sitä voidaan käyttää, kun useita pyyntöjä on käsiteltävä yhdessä tapahtumassa.

Seuraavassa kuvassa on esitetty työnkulku, jonka kumppani tulee kokemaan, kun tätä ominaisuutta käytetään.

![Dataverse ja projektin aikataulutuspalvelun työnkulku.](./media/dataverse-project-scheduling-service-flow.png)

**Vaihe 1**: Asiakas tekee ohjelmointirajapintakutsun Open Data Protocol (OData) -päätepisteeseen Dataversessä OperationSetin luomiseksi.

**Vaihe 2**: Kun uusi OperationSet on luotu, **OperationSetId**-arvo palautetaan.

**Vaihe 3**: Asiakas tekee **OperationSetId**-arvon avulla toisen projektin aikataulutuksen ohjelmointirajapintapyynnön. Tuloksena on aikataulutusentiteetin luonti-, päivitys- tai poistopyyntö. Kun pyyntö tehdään, metatietojen tarkistus tehdään. Jos tarkistus epäonnistuu, pyyntö päättyy ja näyttöön tulee virhe.

**Vaiheet 4 a–4c**: Nämä vaiheet edustavat ACCEPT-vaihetta. Asiakas kutsuu **ExecuteOperationSetV1**-ohjelmointirajapintaa, joka lähettää kaikki projektin aikataulutuspalveluun tehdyt muutokset yhdessä erässä. Projektin aikataulutuspalvelu suorittaa omat pyyntöjen vahvistukset erän pyynnöille. Kaikki tarkistusvirheet kumoavat erän ja palauttavat poikkeuksen kutsujalle. Jos projektin aikataulutuspalvelu hyväksyy erän, OperationSet-tila päivittyy sen mukaan, että projektin aikataulutuspalvelu käsittelee OperationSetin.

**Vaihe 5**: Tämä vaihe tarkoittaa PERSIST-vaihetta. Projektin aikataulutuspalvelu kirjoittaa asynkronisesti erän tapahtumassa Dataverseen. Jos kirjoitustoiminto onnistuu, OperationSet-arvona on **Valmis**. Mahdolliset virheet varmuuskopioivat tapahtuman ja erän ja OperationSet-joukko on merkitty **Epäonnistuneeksi**.

## <a name="performance-methodology"></a>Suorituskykymenetelmät
Suoritusaika määritetään ajasta, joka alkaa kutsusta **ExecuteOperationSetV1**-ohjelmointirajapintaan, kunnes projektin aikataulutuspalvelu on lopettanut kirjoittamisen Dataverse-kohteeseen. Kaikki toiminnot suoritetaan yhteensä 2 200 kertaa, ja P99-suoritusaikamittaukset raportoidaan. Yksittäistietue- ja joukkotoimintoja mitataan.

Yhden tietueen toimintoa varten OperationSet sisältää yhden pyynnön. Joukkotoiminnoissa se sisältää 20, 50 tai 100 pyyntöä. Kukin joukkokoko ilmoitetaan erikseen.

Nämä toiminnot suoritetaan UR 15 Project Operations Lite -käyttöönotossa Pohjois-Amerikassa.

## <a name="results"></a>Tulokset
### <a name="create-operations"></a>Luo toimintoja
#### <a name="single-record-create-operations"></a>Yhden tietueen luontitoiminnot
Seuraavassa taulukossa on esitetty yhden tietueen luonnin suoritusajat. Ajat ilmoitetaan sekunteina.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tietuetyyppi</th>
    <th class="tg-0lax" colspan="2">Aika</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pakolliset kentät</th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tehtävä</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Delegointi</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ryhmän jäsen</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Riippuvuus</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Joukkoluontitoiminnot
Seuraavassa taulukossa on esitetty monen tietueen luonnin suoritusajat. Microsoft on erityisesti mitannut suoritusaikoja 20, 50 ja 100 tietueen luonnissa yhdessä OperationSet-joukossa. Ajat ilmoitetaan sekunteina.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tietuetyyppi</th>
    <th class="tg-0lax" colspan="6">Aika</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 tietuetta</th>
    <th class="tg-0lax" colspan="2">50 tietuetta</th>
    <th class="tg-0lax" colspan="2">100 tietuetta</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pakolliset kentät</th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
    <th class="tg-0lax">Pakolliset kentät</th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
    <th class="tg-0lax">Pakolliset kentät</th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tehtävä</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Delegointi</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Riippuvuus</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> **Projektin** ja **ryhmän jäsenen** entiteettien joukkoluontitoimintoja ei sisällytetä tähän taulukkoon, koska näiden toimintojen suoritusaika muistuttaa suoritusta, kun ohjelmointirajapintaa kutsutaan useita kertoja yhden tietueen luomiseksi. Nämä ohjelmointirajapinnat suoritetaan heti Dataversessä.

Seuraavassa kuvassa on esitetty **tehtävä**-, **määritys**- ja **riippuvuus**-entiteettien suoritusajat, kun luodaan 20, 50 ja 100 tietuetta ja kaikkia tuettuja kenttiä käytetään.

![Luo tietueen suoritusajan kaavio.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Päivitä toimintoja
#### <a name="single-record-update-operations"></a>Yhden tietueen päivitystoiminnot
Seuraavassa taulukossa on esitetty yhden tietueen päivityksen suoritusajat. Ajat ilmoitetaan sekunteina.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tietuetyyppi</th>
    <th class="tg-0lax" colspan="2">Aika</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pakolliset kentät </th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tehtävä</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ryhmän jäsen</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **Resurssimääritykset**- ja **Projektitehtävän riippuvuus** -entiteettien päivitystoimintoja ei tueta.

#### <a name="bulk-update-operations"></a>Joukkopäivitystoiminnot
Seuraavassa taulukossa on esitetty monen tietueen päivityksen suoritusajat. Microsoft on erityisesti mitannut suoritusaikoja 20, 50 ja 100 tietueen päivityksessä yhdessä OperationSet-joukossa. Ajat ilmoitetaan sekunteina.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tietuetyyppi</th>
    <th class="tg-0lax" colspan="6">Aika</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 tietuetta</th>
    <th class="tg-0lax" colspan="2">50 tietuetta</th>
    <th class="tg-0lax" colspan="2">100 tietuetta</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pakolliset kentät</th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
    <th class="tg-0lax">Pakolliset kentät</th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
    <th class="tg-0lax">Pakolliset kentät</th>
    <th class="tg-0lax">Kaikki tuetut kentät</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tehtävä</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ryhmän jäsen</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **Resurssimääritykset**- ja **Projektitehtävän riippuvuus** -entiteettien päivitystoimintoja ei tueta.

Seuraavassa kuvassa on esitetty tehtävä- ja ryhmän jäsen -entiteettien suoritusajat, kun päivitetään 20, 50 ja 100 tietuetta ja kaikkia tuettuja kenttiä käytetään.

![Päivitä tietueen suoritusajan kaavio.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Poista toiminnot
#### <a name="single-record-delete-operations"></a>Yhden tietueen poistotoiminnot
Seuraavassa taulukossa on esitetty yhden tietueen poiston suoritusajat. Ajat ilmoitetaan sekunteina.

| Tietuetyyppi | Aika  |
|-------------|-------|
| Tehtävä        | 20.12 |
| Delegointi  | 10.86 |
| Ryhmän jäsen | 12.52 |
| Riippuvuus  | 20.89 |

> [!NOTE]
> **Projekti**-kohteen poistotoimintoja ei tueta.

#### <a name="bulk-delete-operations"></a>Joukkopoistotoiminnot
Seuraavassa taulukossa on esitetty monen tietueen poiston suoritusajat. Microsoft on erityisesti mitannut suoritusaikoja 20, 50 ja 100 tietueen poistossa yhdessä OperationSet-joukossa. Ajat ilmoitetaan sekunteina.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tietuetyyppi</th>
    <th class="tg-0lax" colspan="3">Aika</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 tietuetta</th>
    <th class="tg-0lax">50 tietuetta</th>
    <th class="tg-0lax">100 tietuetta</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tehtävä</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Delegointi</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ryhmän jäsen</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Riippuvuus</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **Projekti**-kohteen poistotoimintoja ei tueta.

Seuraavassa kuvassa on esitetty **tehtävä**-, **määritys**-, **ryhmän jäsen** ja **riippuvuus** -entiteettien suoritusajat, kun poistetaan 20, 50 ja 100 tietuetta.

![Poista tietueen suoritusajan kaavio.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Havainnot
Jokaista tietuetoimintoa kohti **ExecuteOperationSet**-ohjelmointirajapinnalta kuluu noin 800 millisekuntia pyynnön lähettämiseen projektin aikataulutuspalveluun. Projektin aikataulutuspalvelulla kestää noin viisi sekuntia käsitellä tiedot ja kutsua Dataverseä. Muu suoritusaika kuluu liiketoimintalogiikan suorittamiseen ja tietojen kirjoittamiseen tietokantaan Dataversessä.

Kun 100 tietuetta luodaan, päivitetään tai poistetaan, **ExecuteOperationSet**-ohjelmointirajapinnalla kestää noin kolme sekuntia pyynnön lähettämiseen projektin aikataulutuspalveluun. Projektin aikataulutuspalvelulla kestää noin viisi sekuntia käsitellä pyynnöt ja kutsua Dataverseä. Joukkotoimintojen on maksettava **projektien aikataulutuspalveluvero** kerran kaikista OperationSet-toiminnon tietueista. Siksi joukkotoimintojen suoritusaika on merkittävästi pienempi kuin yhden tietueen toiminnoissa.

## <a name="scenarios"></a>Skenaariot
Seuraavassa taulukossa on esitetty ajat, jolloin projektiaikataulun ohjelmointirajapintoja käytetään tiettyjen skenaarioiden toteuttamiseen. Ajat ilmoitetaan sekunteina.

| Skenaario                                                                   | Aika  |
|----------------------------------------------------------------------------|-------|
| Luo projekti, jolla on 40 tehtävää.                                      | 36.01 |
| Luo projekti, jolla on 40 tehtävää ja 20 riippuvuutta.                  | 38.11 |
| Luo projekti, jolla on 40 tehtävää ja 30 määritystä.                   | 60.17 |
| Luo projekti, jolla on 40 tehtävää ja 20 riippuvuutta ja 30 määritystä. | 60.27 |

## <a name="best-practices"></a>Parhaat käytännöt
Edellisten skenaarioiden tulosten perusteella ohjelmointirajapinnat toimivat paremmin seuraavissa tilanteissa:

  - Ryhmittele mahdollisimman monta toimintoa yhteen. Joukkotoimintojen keskimääräinen suoritusaika on parempi kuin yhden tietueen toimintojen keskimääräinen suoritusaika. Mitä pienempi käytössä olevien OperationSet-joukon määrä on, sitä nopeampi keskimääräinen suoritusaika on.
  - Määritä vain skenaarion suorituksessa tarvittavat vähimmäismääritteet. Valitse OperationSet-pyyntöjen sisältämien ei-pakollisten kenttien tyypit. Kentät, jotka sisältävät vieraita viite- tai koontikenttiä, vaikuttavat negatiivisesti suorituskykyyn.
