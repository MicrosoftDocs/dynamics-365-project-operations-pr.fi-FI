---
title: Project Operationsin lokakuun 2021 uudet tai muuttuneet ominaisuudet varastoitavissa ja tuotantopohjaisissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operationsin varastoitavissa ja tuotantopohjaisissa skenaarioissa -palvelun marraskuussa 2021 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818468"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Project Operationsin lokakuun 2021 uudet tai muuttuneet ominaisuudet varastoitavissa ja tuotantopohjaisissa skenaarioissa

_**Koskee:** Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_

Tämä aihe koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristöversiossa 10.0.22
 
## <a name="quality-updates"></a>Laatupäivitykset

| Ominaisuusalue | Viitenumero | Laatupäivitys |
|--------------|------------------|----------------|
| Projektinhallinta ja kirjanpito | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projektin työ (KET) ja jaksotetut myyntituottosummat eivät kumoudu oikein, kun konsernin sisäinen asiakkaan lasku kirjataan. |
| Projektinhallinta ja kirjanpito | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **Estä projektin sulkeminen, jos avoimia tapahtumia on** -toiminto ei toimi. |
| Projektinhallinta ja kirjanpito | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Vapaatekstilaskun laskutusluokka ei täytä projektien dimensioita automaattisesti, kun toiminto on käytössä. |
| Projektinhallinta ja kirjanpito | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Muissa kuin yritysten välisissä skenaarioissa KET- ja kertyneiden tulojen summia ei peruuteta oikein, kun projektilasku kirjataan. |
| Projektinhallinta ja kirjanpito | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debet- ja kredit-arvoja vaihdetaan, kun Microsoft Excel -apuohjelmaa käytetään projektikulukirjauksen kanssa ja **Offset-tilityyppi**-kentän asetuksena on **Projekti**. |
| Projektinhallinta ja kirjanpito | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Projektitapahtumista julkaistu summa ohitetaan projektin ostotilauksessa, joka sisältää varastonimikkeet ja jolla on vähennyskelvottomat verosummat, kun **UseTax** on merkitty. |
| Projektinhallinta ja kirjanpito | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Järjestelmä jakaa summan projektin tuotto- ja tappioraporttien ja projektin wip-raporttien välillä. |
| Projektinhallinta ja kirjanpito | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Käytettävissä oleva varasto on virheellinen, kun osittain palautettua nimikevaatimusta on muutettu. |
| Projektinhallinta ja kirjanpito | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Resurssien nimet kopioidaan Project Operationsissa, kun niitä muokataan Microsoft Projectissa. |
| Projektinhallinta ja kirjanpito | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Konsernin sisäisissä kuluraporteissa, joissa on ostoreskontran konsernin välisiä odottavia toimittajan laskun kustannuksia, kirjataan ensimmäisen kerran **projektin keskeneräisen työn kustannusten** kirjaustyyppiin. Käsittelyn aikana arvioituihin kustannuksiin liittyvät kustannukset kuitenkin kirjataan **Projektin kustannuksen** kirjaustyyppiin odotetun **konsernin sisäisten kustannusten** kirjaustyypin asemesta. |
| Projektinhallinta ja kirjanpito | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Toimittajan pidättämisen tulokset eivät näy projektikulutapahtumista. |
| Projektinhallinta ja kirjanpito | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Aikaraportin on pyöristettävä tapahtuman summa tapahtumavaluutassa tiettyyn desimaalin tarkkuuteen kaikissa kirjanpitojakaumissa ja kirjauskansiovarausmerkinnöissä. |
| Projektinhallinta ja kirjanpito | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projektinimikkeen tarpeita koskevat määrät päivittyvät automaattisesti, kun suunnitellut tilaukset on määritetty. |
| Projektinhallinta ja kirjanpito | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Tositenumeroa, tapahtumatyypin toimittajan saldoa ja tilinumeroa ei voi palauttaa ostotilauksen ennakkomaksulaskussa. |
| Projektinhallinta ja kirjanpito | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Konsernin sisäinen toimittajan lasku katkesi, kun toimittajan laskun integrointi on käytössä. |
| Projektinhallinta ja kirjanpito | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Kun luot projektikulukirjaa, kustannussumma näkyy **Kredit**-kentässä. |
| Projektinhallinta ja kirjanpito | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektilaskujen maksuehdot eivät toimi odotetusti. |
| Projektinhallinta ja kirjanpito | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Työaikaraporttien tositteita voidaan käyttää uudelleen, kun numerojärjestys on määritetty jatkuvaksi. |
| Projektinhallinta ja kirjanpito | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | RANSKA: **Manuaalinen pidätyssumma** -logiikka ei vastaa projektisopimuslaskuehdotuksessa **automaattista säilytysmäärä** -logiikkaa. |
| Projektinhallinta ja kirjanpito | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kun toimittajan säilyttäminen julkaistaan, tositteen kirjauksessa on virheellisiä lisärivejä. |
| Projektinhallinta ja kirjanpito | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Kun **Laskun päivämäärä** -kenttää muutetaan **Luo laskuehdotus** -sivulla, voi ilmetä seuraava virhe: "Objektiviittausta ei ole määritetty objektin esiintymään". |
| Projektinhallinta ja kirjanpito | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Virhe, kun yrität hyväksyä tuntilomakkeen **TSLine**-työnkulusta ja työaikaraporttikäytäntö on lauantaille ja sunnuntaille. |
| Projektinhallinta ja kirjanpito | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Projektin alkusaldonimiketyyppiä ei jätetä pois **laskuehdotustapahtuman yhteenvedoista**, kun laskun kokonaissumma lasketaan. |
| Projektinhallinta ja kirjanpito | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Jos projektin tuotantotilauksen kustannus on 0 (nolla), tapahtuu seuraava virhe, kun yrität arvioida, että kustannusta yritettiin jakaa nollalla. |
| Projektinhallinta ja kirjanpito | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Androidin projektin työaikaraportin mobiilisovellus lakkaa vastaamasta. Ongelma liittyy **TimeEntryDataManager ArgumentNullException** -kohteeseen. |
| Projektinhallinta ja kirjanpito | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations -integraatiokirjaus epäonnistuu, kun kirjaat sen, koska tililtä puuttuu dimensiot. Tili, josta puuttuu dimensiot, ei kuitenkaan ole tili, jonne olet lähettämässä. |
| Projektinhallinta ja kirjanpito | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Hakujen **ToDate**-suodatinta ei poisteta, kun se poistetaan **Julkaise kustannus** -sivun **Valitse**-valintaikkunasta. |
| Projektinhallinta ja kirjanpito | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Palauta kaikki jakelu** epäonnistuu ja näkyviin tulee virhe aikaraportteja varten, jotka on luotu **vain aika** -tyyppistä projektia varten. |
| Projektinhallinta ja kirjanpito | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Projekti**-välilehteä ei voi muokata odottavassa toimittajan laskussa, kun nimikkeelle on määritetty lisäluokka. |
| Projektinhallinta ja kirjanpito | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Siirtymisruutu puuttuu, jos et ole kirjautunut Project Operations Dataverseen. |
| Projektinhallinta ja kirjanpito | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Konsernin sisäisissä projektin oikaisutapahtumista on ongelmia kohdeyrityksen kanssa. |
| Projektinhallinta ja kirjanpito | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projektin sidotut kustannukset laskevat väärän määrän ja kustannushinnan, jos ostotilaus on käsitelty **ostotilauksen vuoden loppu -prosessissa** pääkirjassa. |
| Projektinhallinta ja kirjanpito | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kun projektin tuotantotilaus, jolla on laatutilauksia, ilmoitetaan valmiiksi, tapahtuu seuraava virhe: "Varastotapahtumalla ei ole merkitty virtuaalitapahtumaa." |
| Projektinhallinta ja kirjanpito | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Kun projektiin liittyvä ostoreskontralasku kirjataan, tapahtuu seuraava virhe: "Luetteloitussa tekstissä Projekti - kustannus - nimikettä ei ole olemassa." |
| Projektinhallinta ja kirjanpito | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Epäsuorat kustannukset kaksinkertaistetaan, kun jaksotat tuottoa manuaalisesti. |
| Projektinhallinta ja kirjanpito | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Tuoton ja KET:in kirjauksen jaksotus ei tuota tapahtumia. |
| Projektinhallinta ja kirjanpito | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Odottavan hinnan aktivointi epäonnistuu vakiokustannusnimikkeelle, kun vastaanotettiin projektin ostotilaus. |
| Projektinhallinta ja kirjanpito | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Käänteinen KET-arvo laskun kirjauksesta eroaa aikamerkinnän alkuperäisestä kirjatusta KET-arvosta. |
| Projektinhallinta ja kirjanpito | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Projektin laskutetuissa tuloissa on kirjausongelma sovelletuissa pidätystapauksissa, joissa tositteen tapahtumat eivät ole tasapainossa. |
| Projektinhallinta ja kirjanpito | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kun laskuehdotus on julkaistu, arvion luominen estää korjausrivien tuonnin Project Operationsissa. |
| Projektinhallinta ja kirjanpito | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Kokonaan laskutettavan välitavoitetietueen muokkaaminen ei pitäisi olla mahdollista. |
| Projektinhallinta ja kirjanpito | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Kun käytetään automaattisia kuluja, aikaraportin konsernin asiakaslaskua ei voi kirjata ja näkyviin tulee virhesanoma. |
| Projektinhallinta ja kirjanpito | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alikansion osoitetta ei päivitetä oikein. |
| Projektinhallinta ja kirjanpito | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Nimikkeen tarpeita varten määritetty kustannushinta päivittyy konsolidoidun ostotilauksen ostohinnan kanssa. |
| Projektinhallinta ja kirjanpito | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Julkaistu kustannus ei ole oikea, kun ostohinta on päivitetty ja parametri **Aktivoi muutosten hallinta** on otettu käyttöön. |
| Matka ja kulut | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kaikki käyttäjäkulut näkyvät, kun haet luokkaa Kulu-mobiilisovelluksessa. |
| Matka ja kulut | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Toimittaja- ja arvonlisäverotapahtumien virheelliset summat kirjataan kulusta, joka on luotu luottokorttitapahtumasta. |
| Matka ja kulut | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Epäolennainen varoitusviesti näytetään, kun päivität kuluraporttisivut. |
| Matka ja kulut | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Väärää väliaikaista hyväksyjää käytetään, kun poistat väliaikaisen hyväksyjän ja lähetät uudelleen työnkulun kautta. |
| Matka ja kulut | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Näkyviin tulee kilometrien asennukseen liittyvä kirjausvirhe. |
| Matka ja kulut | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Jakelu ei päivitä yritystä, kun aikatauluttamaton tapahtuma lisätään uudelleen kuluraporttiin konsernin sisäisillä kuluilla. |

### <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset

Lisätietoja Finance and Operations -sovellusten säännöstenmukaisuuspäivityksistä on kohdassa [Säännöstenmukaisuuspäivitykset](/dynamics365/finance/localizations/regulatory-updates). Voit myös kirjautua Microsoft Dynamics Lifecycle Services (LCS) -palveluihin ja tarkastella suunniteltuja säädöksen päivityksiä Ongelma-hakutyökalulla. Ongelmahaun avulla voit tehdä haun maan tai alueen, toiminnon tyypin ja julkaisun mukaan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
