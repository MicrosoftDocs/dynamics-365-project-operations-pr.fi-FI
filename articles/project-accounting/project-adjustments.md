---
title: Projektin muutokset
description: Tässä artikkelissa on tietoja projektin muutoksista.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788296"
---
# <a name="project-adjustments"></a>Projektin muutokset

_**Koskee:** Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_

## <a name="adjustments-overview"></a>Muutosten yleiskatsaus

Voit määrittää Microsoft Dynamics 365 Project Operationsin niin, että käyttäjät voivat tehdä muutoksia julkaistuihin tapahtumiin. Voit muuttaa projektitapahtumia yksi kerrallaan tai valita luettelosta kaikki projektitapahtumat. Projektimuutoksia käytetään esimerkiksi laskutettavan tilan joukkopäivitykseen, kustannusten uudelleenlaskentaan määritysmuutoksen jälkeen tai rahoituslähteiden päivittämiseen.

Käyttäjät voivat käyttää projektin oikaisutoimintoja useilla tavoilla:

- Käyttämällä **Oikaise tapahtumia** -sivua , jota voi käyttää **projektinhallinnan ja kirjanpidon** \> **asetuksista**.
- Käyttämällä **Muutos**-painiketta **Kirjatut projektitapahtumat** -sivulla, jota voidaan käyttää kohdasta **Projektinhallinta ja kirjanpito** \> **Tapahtumat**.
- Käyttämällä **Muutos**-painiketta **Kirjatut projektitapahtumat** -sivulla projektin kontekstissa. Tätä sivua voi käyttää kohdasta **Projektinhallinta ja kirjanpito** \> **Kaikki projektit**.

Vähintään yksi tapahtuman tila on otettava käyttöön kohdassa **Projektinhallinta ja kirjanpito** \> **Projektinhallinnan ja kirjanpidon parametrit** **Yleset**-välilehdellä osassa **Salli tapahtuman tilan muuttaminen**, jotta muutoksia voidaan tehdä. Esimerkkejä tapahtumien tilasta ovat julkaistut tapahtumat, laskutetut tapahtumat ja poistetut tapahtumat. Kun tapahtuman tilaksi on määritetty **Ei** , tilassa on tapahtumia, jotka eivät näy oikaisuprosessissa valittavissa oikaisua varten.

Määritysvaihtoehto nimeltä **Luo aina oikaisutapahtuma** on tällä hetkellä käytettävissä projektinhallinnan ja kirjanpidon parametreissa. Voit poistaa tämän vaihtoehdon käytöstä, jos haluat päivittää alkuperäisen tapahtuman sen sijaan, että loisit uusia tapahtumia oikaisun aikana aliskenaarioiden alijoukossa. Parametrin on ilmoitettu vanhentuvan 1.3.2023 mennessä. 1.3.2023 jälkeen järjestelmä toimii aina samalla tavalla kuin vaihtoehto olisi otettu käyttöön.

## <a name="adjustments-process-flow"></a>Muutosprosessin työnkulku

Seuraavissa vaiheissa näkyy tyypillinen työnkulku muutosten käsittelyä varten.

1. Avaa **Projektin oikaisut** -sivu.
2. Valitse **Valitse** , jos haluat hakea tapahtumia, jotka vastaavat odotettuja oikaisuehtoja.
3. Valitse tapahtumien luettelosta kaikki tapahtumat tai tapahtumien alijoukko oikaisua varten.
4. Valitse **Muokkaa** ja muokkaa rivin määritteitä. Jos arvot on määritetty manuaalisesti tapahtuman kirjauksen aikana, voit myös määrittää järjestelmäarvojen oletusarvot.
5. Tapahtumaluettelo palautetaan ja **Odottaa muutosta** -sarakkeeseen tulee valintamerkki, joka osoittaa, missä muutokset on tehty. Kaikki odottavat muutokset näkyvät sivun alaosassa. Siellä voit tehdä yksityiskohtaisia lisämuutoksia edellisellä sivulla näkyvien muutosten lisäksi.
6. Kirjaa muutostapahtumat valitsemalla **Kirjaa**.

Määrityksestä riippuen oikaisulle luodaan yleensä uusia tapahtumia.

- Alkuperäisen tapahtuman **Laskun tila** -kentän arvoksi päivittyy **Oikaistu**.
- Peruutustapahtuma luodaan alkuperäisen tapahtuman peruutusta varten ja **Tila**-kentän  arvoksi tulee **Muutettu**.
- Luodaan uusi tapahtuma, johon on tehty oikaisuprosessin aikana tehdyt muutokset.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Useiden kirjattujen projektitapahtumien valitseminen kerrallaan oikaisuja ja hyvityslaskuja varten

Julkaisussa 10.0.30 käyttöön otettu uusi ominaisuus mahdollistaa useiden tapahtumien valinnan oikaisua varten kerrallaan **Kirjatut projektitapahtumat** -sivulta.

Ennen kuin käytät tätä toimintoa, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat tarkistaa **Ominaisuuksien hallinnan** työtilassa ominaisuuden tilan sekä ottaa sen käyttöön tarvittaessa. Hae ja valitse **Ominaisuuksien hallinta** -työtilassa **Kirjattujen projektitapahtumien monivalinta muutoksia ja hyvityslaskuja varten** ja valitse sitten **Ota käyttöön nyt**.

Tämä toiminto ottaa käyttöön seuraavat toiminnot:

- Sitä voidaan käyttää projektin kirjatun tapahtuman sivulta käyttämällä olemassa olevaa **Oikaisu**-painiketta.
- Se ottaa käyttöön monirivisen valintaohjausobjektin **Julkaistut projektitapahtumat** -sivulla. Voit ottaa suodattimet käyttöön luettelosivulla ja valita tietueet, ennen kuin aloitat oikaisut.
- Se poistaa **Oikaisu**-painikkeen  käytöstä, jos yhtäkään tapahtumaa ei voi oikaista tai jos valitset hyvityslaskujen ja kirjausten yhdistelmiä yksitellen valitsemisen asemesta.
- Monirivisen valintaohjausobjektin lisäämisen vuoksi valintanauhan **Sidottu kustannus** -linkkiä ei enää poisteta käytöstä, jos valittuna on useita rivejä.
- Se lisää seuraavan varoitussanoman: "Olet valinnut oikaisua varten enemmän kuin (valittu numero) tietuetta. Tämän toiminnon jatkaminen voi kestää jonkin aikaa. Haluatko varmasti jatkaa tätä toimintoa?

Tämä ominaisuus poistaa myös vaiheen 2 aiemmin tässä artikkelissa kuvatusta prosessista. Tämän vuoksi kaikki tapahtumat, jotka on valittu ennen **Oikaise tapahtumat** -sivun avaamista, sisällytetään oikaisutapahtumien luetteloon. Sinun ei tarvitse hakea niitä **Valinta**-painikkeella.

> [!NOTE] 
> Vaikka tämä toiminto ei olisi käytössä, voit silti valita useita tietueita oikaisua varten. Vain yksi tietue *säilyy valittuna*, ja  **Valitse tapahtumat** -valintaikkuna tulee näkyviin heti, kun olet valinnut oikaisujen avaamisen.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Oikaisutapahtumien tilat, jotka voidaan ottaa käyttöön tai poistaa käytöstä oikaisuissa

Seuraavat tilat voidaan ottaa käyttöön tai poistaa käytöstä **Yleiset**-välilehdellä **Projektinhallinta ja kirjanpitoparametrit** sivulla:

- Kirjattu
- Laskuehdotus
- Laskutettu
- Arvioitu
- Poistettu
- Aloitussaldon (tunti)

## <a name="adjustment-parameters"></a>Muutosparametrit

Nämä parametrit on lueteltu **Projektinhallinta ja kirjanpitoparametrit** -sivulla **Yleiset** välilehdellä **Muutos**-ryhmän alla ja ne muokkaavat muutosten käsittelyn toimintaa. 

| Parametrin nimi | Description |
|----------------|-------------
| Luo aina oikaisutapahtuma | Jos tämä parametri on käytössä, oikaisuprosessi luo aina uuden peruutustapahtuman ja uuden oikaistun tapahtuman, kun vaikutus on taloudellinen tai raportointi. Jos parametri ei ole käytössä, oikaisuprosessi päivittää alkuperäisen tapahtuman sen sijaan, että luotaisiin peruutustapahtuma ja uusi tapahtuma esimerkiksi tapahtumatekstin päivitykseen. |
| Päivitä kenttä automaattisesti | Jos tämä parametri on käytössä, järjestelmä laskee kustannushinnan ja myyntihinnan uudelleen. |
| Käytä oikaisupäivämäärää uutena projektina | Tämän parametrin avulla voidaan siirtää tapahtumia tulevaisalle kirjanpitokaudelle ennen kuin järjestelmä tukee tätä toimintoa. Sen käyttöä ei suositella, koska se muuttaa tapahtuman liiketoimintapäivämäärää ja vanhentuu myöhemmin. |
| Salli suljetut aktiviteetit | Tapahtumia ei yleensä voi luoda suljetuille tapahtumille. Jos tämä parametri on käytössä, tämä toiminta ohitetaan. Siksi suljettuihin aktiviteetteihin voidaan luoda oikaisuja. |
