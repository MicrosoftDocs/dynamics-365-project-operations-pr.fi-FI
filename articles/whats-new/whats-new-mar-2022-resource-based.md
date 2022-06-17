---
title: Maaliskuun 2022 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa maaliskuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910902"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Maaliskuun 2022 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

*Käytetään: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa*

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.30.0.99
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.25

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Uusi ja uudistettu uudenaikainen kulutyötila tukee nyt päivärahoja. Päivärahoja käyttävät yritykset voivat tämän ominaisuuden avulla antaa käyttäjille helpon tavan lähettää päivärahakulut ja saada heille korvauksen kuluista. Lisätietoja on aiheessa [Päivärahakulut](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Seuraavassa luettelossa on esitetty Project Operationsin maaliskuun 2022 julkaisuun muutetut tai lisätyt kaksoiskirjoituksen yhdistämismääritykset.

| **Entiteetin yhdistämismääritys** | **Päivitetty versio** | **Kommentit** |
| --- | --- | --- |
| Project Operationsin integrointiprojektin toimittajalaskurivin vientientiteetti msdyn\_projectvendorinvoicelines | 1.0.0.3 | Yhdistämismääritykset, jotka on päivitetty vastaamaan toimittajan laskurivin entiteettiä Dataversessa. <br>Älä aktivoi yhdistämisversiota 1.0.0.4. Se on valmis käytettäväksi yhdessä Finance-ympäristön version 10.0.26 kanssa seuraavassa kuukausipäivityksessä. |

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Aika ja kulut | 2388011 | Näytä hylkäyskommentit aikamerkinnän lähettäjille joukkohyväksynnän aikana. |
| Projektin suunnittelu ja seuranta | 2495294 | Projektin tietoja ei voi muokata **Tehtävän tiedot** -sivulla. |
| Laskutus ja hinnoittelu | 2499605 | Tarjouksen välitavoitteista luodut palvelusopimuksen välitavoitteet on merkitty virheellisesti vain luku -tilaan. |
| Projektin suunnittelu ja seuranta | 2506050 | Toimintojoukko pysyy odottavana tunnin, jos tallennettavia muutoksia ei ole. Tämän jälkeen joukko merkitään virheellisesti **Epäonnistunut**-merkinnäksi, mutta se pitäisi suorittaa heti. |
| Laskutus ja hinnoittelu | 2507401 | Oletussopimusyksiköt on syötetty väärin projekteihin virheellisen välimuistin vuoksi. |
| Laskutus ja hinnoittelu | 2541660 | **Myyntitilauksen luonnin vahvistus** kaksoiskirjoituksessa tulisi olla vain projektipohjaisia tilauksia varten. |
| Laskutus ja hinnoittelu | 2552745 | Veroa ei jaeta asiakkaiden kesken, jotka ovat määrittäneet jaetut laskutussäännöt. |
| Laskutus ja hinnoittelu | 2558859 | Parannetut virhesanomat, kun hinnoitteludimensiot on määritetty. |
| Laskutus ja hinnoittelu | 2558933 | **Tuonti projektiarvioista** epäonnistuu, kun **msdyn\_project** lisätään hinnoitteludimensioksi. |
| Laskutus ja hinnoittelu | 2559101 | Projektiparametrien poisto ei ole estetty, ja se aiheuttaa ongelmia. |
|   Mahdollisuuksien hallinta | 2570390 | Kaksoiskirjoituslaajennuksen pakottaa tilityypiksi tarjouksissa, tilauksissa ja mahdollisuuksissa **Asiakas**, vaikka tilityyppi ei olisikaan oikea. |
| Laskutus ja hinnoittelu | 2586097 | Jaettuja laskutettuja kustannuksia ei peruuteta, kun projekti poistetaan projektisopimusriviltä. |
| Laskutus ja hinnoittelu | 2589619 | Lisättyjen materiaalien vero välitetään laskuttamattoman myynnin toteutuneiksi ja laskuun. |
|   Mahdollisuuksien hallinta | 2594015 | Tarjousta ei voi sulkea voitettuna asiakkaille, joilla on **Net60**-maksuehdot. |
| Projektin suunnittelu ja seuranta | 2595841 | Project for the Webissä käyttäjät saavat virhesanoman puuttuvasta kohteesta **msdyn\_actualstart** kun he luovat uuden resurssipyynnön. |
| Aika ja kulu | 2602511 | Aikamerkintöjen **Hylännyt**-kentässä näkyy **Järjestelmä** eikä nimetty käyttäjä hylkääjänä. |
| Aika ja kulu | 2602528 | Projektin hyväksyjä voi hyväksyä niiden projektien ajan, joihin häntä ei ole merkitty hyväksyjäksi. |
| Laskutus ja hinnoittelu | 2608550 | Korjauslaskun voi vahvistaa, vaikka alkuperäiseen versioon ei olisi tehty muutoksia. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektinhallinta ja kirjanpito Dynamics 365 Financessa

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Projektinhallinta ja kirjanpito | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Financen ja Project Operationsin välillä on ristiriita **Luokan tunnus** -kentän sallitussa pituudessa. |
| Projektinhallinta ja kirjanpito | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Kiinteähintaisia projekteja ei voi poistaa, kun **Ennakkolaskutus**-kentän asetuksena on **Voitto ja tappio** ja kun käytetään **Valmistumisprosentti**-periaatetta. |
| Projektinhallinta ja kirjanpito | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Project Operationsin integrointikirjauskansion kuluriveille kuluriveille syötetään virheellinen oletusmyyntiveroryhmä projektin määrityksistä. |
| Projektinhallinta ja kirjanpito | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Projektilaskuehdotusotsikon dimensioita ei voi muokata integroidussa Project Operations -käyttöönotossa. |
| Projektinhallinta ja kirjanpito | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Konsernin sisäisiä toimittajien laskuja ei saa integroida Dataversen kanssa. |
| Projektinhallinta ja kirjanpito | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Asiakkaan saldovaluutassa ja raportointivaluutassa on ristiriita. |
| Projektinhallinta ja kirjanpito | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Voit kirjata projektilaskun, vaikka asiakas olisi pidossa kaikille laskuille. |
| Projektinhallinta ja kirjanpito | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | **Poista kaikki rivit** -painike puuttuu projektilaskuehdotuksista, joilla on **Otsikko**- ja **Rivit**-näkymät. |
| Projektinhallinta ja kirjanpito | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Kun kirjaat toimittajan laskun, tapahtuu seuraava virhe: "Laskun kirjanpitopäivän on oltava samana tilivuotena kuin liittyvän ostetun tilauksen. Suorita ostotilauksen tilikauden lopetusprosessi tai muuta päivämäärä nykyiselle tilikaudelle." |
| Matka ja kulut | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Projektin sidottua kustannusta ei vapauteta, kun matkustuspyynnön sidottu kustannus on vapautettu. |
| Matka ja kulut | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kun lähetät kuluraportin, tulee seuraava virhe: "Pinojäljitys: Yritystä ei ole." |
| Matka ja kulut | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Oletusarvoista **projektitunnusta** ei syötetä kuluraportteihin, kun projektissa on valittu **Vaadi aktiviteetti kirjauskansiolle** -parametri. |
| Matka ja kulut | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | **Kirjaa kulut** -painike ei toimi oikein Project Operationsissa resurssi/ei-varastoitu -skenaarioissa. |
| Matka ja kulut | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Kilometrikuluraportin **Hinta kilometriä kohti** -raportissa on ongelma, jos se sisältää matkustajia. |
| Matka ja kulut | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Työntekijöiden kulujen kilometrihinnat eivät ole oikein yhteenlaskettu, kun **kilometrikorvaustaso**-kululuokassa käytetään kahta eri ajoneuvotyyppiä. |
| Matka ja kulut | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Matkustusehdotusrivin **Projekti**-kentän valinta ei palauta oikeaa projektiluetteloa. |
| Matka ja kulut | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Tarkistettavat kilometrikustannukset** käyttää varoituksen kuluraporteissa. |
| Matka ja kulut | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Kuitin optinen merkkien tunnistuspalvelu (OCR) ei toimi, koska kulujen OCR-palvelun URL-osoitteessa on ongelma. |
| Matka ja kulut | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Kun **Erittele toistuvat kulut nopeasti** -toiminto on käytössä, kuluraporttien eritellyillä riveillä olevat summat muuttuvat aina, kun **Erittele**-sivu avataan. |
| Matka ja kulut | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Kuluraporttia ei voi poistaa, jos väliaikaisluettelossa on useita hyväksyjiä. |

## <a name="removed-and-deprecated-features"></a>Poistetut ja vanhentuneet ominaisuudet

Artikkelissa [Project Operationsin poistetut tai vanhentuneet ominaisuudet](removed-depreciated-features-project.md) käsitellään ominaisuuksia, jotka on poistettu tai vanhentuneet Dynamics 365 Project Operationsissa.

- Poistettu toiminto ei ole enää käytettävissä tuotteessa.
- Vanhentunutta ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Vanhentumisilmoitus näkyy artikkelissa [Project Operationsin poistetut tai vanhentuneet toiminnot](removed-depreciated-features-project.md) 12 kuukautta ennen ominaisuuden poistoa tuotteesta.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä muutokset ovat toiminnallisia päivityksiä, jotka on tehtävä kääntäjään.
