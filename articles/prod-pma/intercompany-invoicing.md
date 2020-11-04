---
title: Konsernin sisäinen laskutus
description: Tässä artikkelissa on tietoja ja esimerkkejä projektien laskutuksesta konsernin sisällä.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075374"
---
# <a name="intercompany-invoicing"></a>Konsernin sisäinen laskutus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja ja esimerkkejä projektien laskutuksesta konsernin sisällä.

Organisaatiolla voi olla useita osastoja, tytäryhtiöitä ja muita juridisia kohteita, jotka siirtävät tuotteita ja palveluja toisiinsa projekteissa. Palvelua tai tuotetta tarjoavaa yritystä kutsutaan *Lainauksen tekeväksi yritykseksi* , ja palvelua tai tuotetta vastaanottavaa yritystä kutsutaan *Lainaavaksi yritykseksi*. 

Seuraavassa kuvassa on tyypillinen skenaario, jossa kaksi yritystä, SI FR (lainauksen tekevä yritys) ja SI USA (lainaava yritys) jakavat resursseja asiakkaan A projektin toimittamiseksi. Tässä skenaariossa SI FR toimittaa työn asiakkaalle A. 

[![Konsernin sisäinen laskutusesimerkki](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Tavoitteena on helpottaa konserniyritysten välisten projektitapahtumien kustannusten hallintaa, tuottojen tunnustamista, veroja ja siirtohintaa. Lisäksi käytettävissä ovat seuraavat ominaisuudet:

-   Luo asiakkaan laskuja lainauksen tekevän yrityksen projektia varten käyttämällä yritysten välisiä taulukoita, kuluja ja toimittajien laskuja lainaavassa yrityksessä.
-   Tue verolaskelmia ja välillisiä kustannuksia.
-   Siirrä tuoton tuloutus lainauksen tekevälle yritykselle ja silloin, kun lainaavan yrityksen on hyväksyttävä kustannus.
-   Jaksota keskeneräisen työn tuotto (KET) lainauksen tekevässä yrityksessä.
-   Määritä siirtohinnat, jotka voivat perustua erilaisiin hinnoittelumalleihin. Seuraavassa on joitakin esimerkkejä.
    -   **Määrä** – **Hinnoittelu** -kenttään syöttämäsi summa on todellinen kustannus per määrä tai yksikkö.
    -   **Kulujen summa** – Hinta/kustannus tapahtumaa kohti sekä **Hinnoittelu** -kenttään syöttämäsi kulujen summa.
    -   **Kuluprosentti** – Siirtohinta on hinta/kustannus tapahtumaa kohden kerrottuna **Hinnoittelu** -kenttään syöttämälläsi kuluprosentilla.
    -   **Myyntihinnan prosenttiosuus** – Lainauksen tekevälle yritykselle siirretyn myyntihinnan prosenttiosuus.
    -   **Myyntihinnan alapuolella oleva määrä** – Määrä, jonka lainaava yritys pidättää myyntihinnoista ennen kuin se siirretään lainauksen tekevälle yritykselle.
    -   **Kateprosentti** – **Hinnoittelu** -kenttään syöttämäsi numero on kateprosentti, joka ilmaistaan prosentteina myyntihinnasta.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Esimerkki 1: konsernin sisäisen laskutuksen parametrien määrittäminen
Tässä esimerkissä USSI on lainauksen tekevä yritys, ja sen resurssit raportoivat aikaa suhteessa lainaavaan yritykseen, FRSI, joka omistaa sopimuksen loppuasiakkaan kanssa. Tunnit ja kulut, jotka USSI-työntekijät raportoivat, voidaan sisällyttää projektilaskuun, jonka FRSI luo. Lisäksi on olemassa kolmas tapahtumalähde, joka voi olla peräisin lainauksen tekevästä yrityksestä (tässä esimerkissä), kun se tarjoaa jaettuja toimittajapalveluita tytäryhtiöille (esimerkiksi FRSI) ja siirtää nämä kustannukset kyseisten tytäryritysten projekteihin. Kaikki vastaavat laskun asiakirjat ja verolaskelmat täytetään Financessa. 

Tässä esimerkissä FRSI:n on oltava USSI-yrityksen asiakas, ja USSI-kohteen on oltava FRSI-yrityksen toimittaja. Tämän jälkeen voit määrittää konserniyritysten välisen suhteen kahden yrityksen välille. Seuraavassa kuvataan, miten parametrit määritetään niin, että molemmat yritykset voivat osallistua konsernin sisäiseen laskutukseen.

1. Määritä FRSI asiakkaana USSI-yrityksessä ja määritä USSI toimittajaksi FRSI-yritykseen. Tässä tehtävässä tarvittavissa vaiheissa on kolme kohtaa.

   | Osavaihe |                                                       Merkintäkohta                                                        |                                                                                                                                                                                               Kuvaus                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Valitse kohdassa USSI <strong>Myyntireskontra</strong> &gt; <strong>Asiakkaat</strong> &gt; <strong>Kaikki asiakkaat</strong>. |                                                                                                                                                                  Luo FRSI:n uusi asiakastietue ja valitse asiakasryhmä.                                                                                                                                                                  |
   |  B   |    Valitse FRSI-kohdassa <strong>Ostoreskontra</strong> &gt; <strong>Toimittajat</strong> &gt; <strong>Kaikki toimittajat</strong>.     |                                                                                                                                                                    Luo USSI:n uusi toimittajatietue ja valitse toimittajaryhmä.                                                                                                                                                                    |
   |  C   |                                  Avaa FRSI-ohjelmassa juuri luomasi toimittajatietue.                                  | Valitse toimintoruudussa <strong>Yleiset</strong>-välilehden <strong>Asetukset</strong>-ryhmässä <strong>Konsernin sisäinen</strong>. Määritä <strong>Konsernin sisäinen</strong> -sivun <strong>Kauppasuhde</strong>-välilehdessä <strong>Aktiivinen</strong>-liukusäätimen arvoksi <strong>Kyllä</strong>. Valitse <strong>Asiakasyritys</strong>-kentässä vaiheessa A luomasi asiakastietue. |


2. Valitse **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Projektinhallinnan kirjanpitoparametrit** ja valitse sitten **Konserniyritysten välinen** -välilehti. Parametrien määritystapa määräytyy sen mukaan, onko kyseessä lainaava yritys vai lainauksen tekevä yritys.
   -   Jos olet lainaava yritys, valitse hankintaluokka, jota käytetään automaattisesti muodostettavien toimittajalaskujen täsmäyttämiseksi.
   -   Jos olet lainauksen tekevä yritys, valitse kullekin lainaavalle yritykselle oletusprojektiluokka kutakin tapahtumatyyppiä kohti. Projektiluokkia käytetään veromäärityksessä, kun konserniyritysten välisissä tapahtumissa laskutettu luokka on vain lainaavassa yrityksessä. Voit määrittää, että konserniyritysten väliset tapahtumat jaksotetaan. Tämä jaksotus tehdään, kun tapahtumat kirjataan, joten se palautetaan, kun konsernin sisäinen lasku kirjataan.

3. Valitse **Projektinhallinta ja kirjanpito** &gt; **Määritys** &gt; **Hinnat** &gt; **Siirtohinta**.
4. Valitse valuutta, tapahtumatyyppi ja siirtohintamalli. Laskussa käytettävä valuutta on valuutta, joka on määritetty lainaavan yrityksen lainauksen tekevän yrityksen asiakastietueessa. Valuuttaa käytetään täsmäyttämään siirtohintataulukon tapahtumia.
5. Valitse **Pääkirjanpito** &gt; **Kirjausasetukset** &gt; **Konserniyritysten välinen laskenta** ja määritä USSI- ja FRSI-suhteelle suhde.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Esimerkki 2: konserniyritysten välisen työaikaraportin luominen ja kirjaaminen
USSI, Lainauksen tekevän yrityksen on luotava ja postitettava projektin työaikaraportti FRSI:stä, joka on lainaava yritys. Tässä tehtävässä tarvittavissa vaiheissa on kaksi kohtaa.

| Osavaihe | Merkintäkohta                                                                       | Kuvaus                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektinhallinta ja kirjanpito** &gt; **Työaikaraportit** &gt; **Kaikki työaikaraportit** | Uuden työaikaraportin luominen. Valitse tuntiaikaraportin rivin **Yritys** -kentässä **FRSI**. Valitse **Projektitunnus** -kentässä projekti FRSI-ohjelmassa. Anna kunkin viikonpäivän tunnit. |
| B    | **Työaikaraportti** -sivu                                                                | Kun työnkulku on suoritettu, kirjaa tuntilomake ja merkitse tositenumero.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Esimerkki 3: konserniyritysten välisen toimittajalaskun luominen ja kirjaaminen
USSI, Lainauksen tekevän yrityksen on luotava ja postitettava projektin konsernin sisäinen toimittajalasku FRSI:stä, joka on lainaava yritys. Tämä toimittajalasku edustaa alihankkijoita, jotka on suorittanut USSI:n maksamat toimittajat. Tässä tehtävässä tarvittavissa vaiheissa on kaksi kohtaa.

| Osavaihe | Merkintäkohta                                                                                      | Kuvaus                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Ostoreskontra** &gt; **Laskut** &gt; **Avaa toimittajalaskut** &gt; **Uusi toimittajalasku** | Luo uusi toimittajalasku ja kirjoita FRSI-projektin puolesta hankitut palvelut.                                                                                                                                                                                  |
| B    | **Toimittajalasku** -sivu                                                                      | Anna rivit, jotka edustavat ulkoistettuja palveluita FRSI:n puolesta. Kirjoita laskun rivin **Projekti** -välilehden **Rivin tiedot** -pikavälilehden **Projekti yritys** - kenttään **FRSI**. Anna projekti ja vastaavat tiedot. Kirjaa sitten toimittajalasku. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Esimerkki 4: konserniyritysten välisen laskun luominen ja kirjaaminen
USSI:n, lainauksen tekevän yrityksen, täytyy luoda ja kirjata konsernilasku. Tässä tehtävässä tarvittavissa vaiheissa on kaksi kohtaa.

| Osavaihe | Merkintäkohta                                                                                             | Kuvaus                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektinhallinta ja kirjanpito** &gt; **Projektilaskut** &gt; **Konsernin sisäinen myyntilasku**  | Avaa **Luo konsernin lasku** -sivu valitsemalla **Uusi**.                                                                                  |
| B    | **Projektinhallinta ja kirjanpito** &gt; **Projektilaskut** &gt; **Konsernin sisäiset myyntilaskut** | Kirjoita **Luo konserninsisäinen lasku** -sivulle yritys, määritä sisällytettävä tapahtuma ja valitse sitten **Hae**. |
| C    | **Projektinhallinta ja kirjanpito** &gt; **Projektilaskut** &gt; **Konsernin sisäiset myyntilaskut** | Valitse laskutettavat tapahtumat tai valitse **Valitse kaikki** , jos haluat laskuttaa kaikki luettelon tapahtumat, ja valitse sitten **OK**.                  |
| D    | **Konsernin sisäinen lasku** -sivu                                                                       | Näkyviin tulee konsernin sisäinen myyntilaskuehdotus.                                                                                             |
| E    | **Konsernin sisäinen lasku** -sivu                                                                       | Valitse **Julkaise**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Esimerkki 5: toimittajalaskun kirjaaminen ja asiakkaan laskuttaminen
Kun lainauksen tekevä yritys, USSI, kirjaa konserniyritysten välisen myyntilaskun, vastaavan odottavan toimittajan lasku luodaan lainaavassa yrityksessä, FRSI. Kun tämä toimittajan lasku on kirjattu, FRSI laskuttaa myös projektiasiakkaan syöttämien tuntien ajan. Tässä tehtävässä tarvittavissa vaiheissa on kolme kohtaa.

| Osavaihe | Merkintäkohta                                                                                        | Kuvaus                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Osto reskontra** &gt; **Laskut** &gt; **Odottavat toimittajan laskut**                            | Tarkista lasku tarkistamalla, että tuntilomakkeen arvot on sisällytetty, ja kirjaa sitten toimittajan lasku.                  |
| B    | **Projektinhallinta ja kirjanpito** &gt; **Projektilaskut** &gt; **Projektin laskuehdotukset** | Luo projektille uusi projektilasku ja tarkista, että kirjatut tuntitapahtumat tulevat näkyviin.            |
| C    | **Projektilasku** -sivu                                                                       | Valitse projektilasku ja tarkastele sitten kustannusta ja myyntihintaa valitsemalla **Näytä tiedot**. Kirjaa sitten lasku. |


Lisätietoja on aiheessa [Konsernin sisäisen projektilaskutuksen määrittäminen](tasks/configure-intercompany-project-invoicing.md).


