---
title: Project Operationsin syyskuun 2021 uudet tai muuttuneet ominaisuudet varastoitavissa ja tuotantopohjaisissa skenaarioissa
description: Tässä artikkelissa on tietoja Project Operationsin varastoitavissa ja tuotantopohjaisissa skenaarioissa syyskuussa 2021 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916514"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Project Operationsin syyskuun 2021 uudet tai muuttuneet ominaisuudet varastoitavissa ja tuotantopohjaisissa skenaarioissa

_**Koskee:** Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.21
 
## <a name="quality-updates"></a>Laatupäivitykset

| Ominaisuusalue | Viitenumero | Laatupäivitys |
|---|---|---|
| Projektinhallinta ja kirjanpito | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jos ostopäällikön roolille on annettu käyttöoikeus yhteen oikeushenkilöön, se antaa myös käyttöoikeuden kaikkien oikeushenkilöiden kaikkiin projekteihin. |
| Projektinhallinta ja kirjanpito | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Arvonlisäveron (ALV) pyöristysongelma ilmenee, kun hyvityslasku hyvitetään alkuperäistä projektilaskua vastaan. |
| Projektinhallinta ja kirjanpito | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Käytä budjetin tarkistamiseen vaihtoehtoista projektibudjettia. |
| Projektinhallinta ja kirjanpito | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | **Myyntihinnan tunti** -hintaryhmää ei lasketa projektitarjousten työrakenteen mukaan. |
| Projektinhallinta ja kirjanpito | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Arvion eliminointi epäonnistuu, kun **Ota projektin sopimusvaluutta käyttöön arvion laskemista varten** -ominaisuus otetaan käyttöön. |
| Projektinhallinta ja kirjanpito | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Määrän mukaan lisätty myyntiverolasku lisätään myyntihinnan summaan, kun projektikulukirjauksen myyntiveroryhmässä käytetään veroa. |
| Projektinhallinta ja kirjanpito | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Ehdollista veroa ei lasketa oikein viimeiselle maksulle, kun toimittajan säilytys ja ennakkomaksu on kohdistettu ostotilauksen laskuihin. |
| Projektinhallinta ja kirjanpito | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Oikaisun seuranta ei toimi alkusaldokirjauksia varten. |
| Projektinhallinta ja kirjanpito | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Projektibudjetin version kohdistus kauden mukaan** jaetaan kaikkien budjettijaksojen välillä. Kun kohdistus lähetetään, tietuetta ei tyhjennetä. |
| Projektinhallinta ja kirjanpito | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Keskeneräisen työn (KET) kirjauksissa pääkirjanpitoon on virheellinen summa. |
| Projektinhallinta ja kirjanpito | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Projektituntikirjan hyväksyntä ei toimi. |
| Projektinhallinta ja kirjanpito | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Projektin oikaisun myyntihintaa ei päivitetä epäsuorilla kustannuksilla, kun rahoitusrajoitusta ei ole määritetty. |
| Projektinhallinta ja kirjanpito | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Nimikkeen tarvetta ei voi luoda, kun Myynti-taulukon otsikko laskutetaan ja aiemmin luotujen rivien taustaostotilaus on viimeistelty. |
| Projektinhallinta ja kirjanpito | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Sellaisen laskutussäännön säilytyssummaa, jolla on toisen projektin välitavoite, ei julkaista välitavoitteelle valitussa projektitunnuksessa. Sen sijaan se on julkaistu ensimmäisellä projektilla. |
| Projektinhallinta ja kirjanpito | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kun valitset laskuehdotukseen **taloushallinnon dimensiojoukon**, tapahtuu seuraava virhe: "Dynamics.AX.Application.FormIntControl-tyyppistä objektia ei voida lähettää tyyppiin "Dynamics.AX.Application.FormStringControl"." |
| Projektinhallinta ja kirjanpito | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **Projektin lasku** -raportti ohittaa rivejä. |
| Projektinhallinta ja kirjanpito | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Virhe laskettaessa investointiprojektin kustannusten hallintaa. |
| Projektinhallinta ja kirjanpito | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable::InitFromCustTable - canDeletePostalAddress** -menetelmä aiheuttaa suorituskykyongelman. |
| Projektinhallinta ja kirjanpito | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Virhesanoman on oltava selkeämpi kuin "Odottamaton virhe". |
| Projektinhallinta ja kirjanpito | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Projektin laskun kirjauserätyö käsittelee ja kirjaa laskuehdotuksen, vaikka laskurivejä ei olisi luotu. |
| Projektinhallinta ja kirjanpito | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Pyöristysongelma ilmenee, kun julkinen käyttöoikeuslisenssin määritysavain on poistettu käytöstä. Työaikaraportin tuntiin luodaan virheellinen kustannus tai myyntihinta palvelusopimuksille, joissa on useita löytämislähteitä. |
| Projektinhallinta ja kirjanpito | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Projektin laskutetussa ostotilauksessa projektin myyntihinta lasketaan virheellisesti, kun myyntihintamalli on **Kateprosentti**. |
| Projektinhallinta ja kirjanpito | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Järjestelmä ei ota huomioon välissä olevia aktiivisia päiviä, kun se laskee työntekijän tehokkaan työmäärän. |
| Projektinhallinta ja kirjanpito | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Konsernin sisäisessä aikaraportissa tapahtuu kirjausvirhe seuraavan tarkistusvirheen takia: "Liikekumppania ei ole määritetty juridiseen entiteettiin". |
| Projektinhallinta ja kirjanpito | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Ostotilauksen kuvausta, jolla on kululuokka, ei noudeta julkaistusta projektitapahtumaluettelosta. |
| Projektinhallinta ja kirjanpito | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Projektiin kirjatuissa nimikekirjakirjoissa on virheellinen muunnos. |
| Projektinhallinta ja kirjanpito | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Voit vahvistaa ostotilauksen, vaikka rahoitusrajoitus olisi ylittynyt. |
| Projektinhallinta ja kirjanpito | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Vapaatekstilaskun **Korjaus-/peruutuslasku**-osa katoaa näkyvistä, kun projektitunnus valitaan. |
| Projektinhallinta ja kirjanpito | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Suorituskykyongelmia on silloin, kun projektilaskuehdotus kirjataan projektin myyntitilauksesta, joka sisältää varastonimikkeen. |
| Projektinhallinta ja kirjanpito | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projektin ostolaskuja ei voi julkaista, koska seuraava virhe ilmenee: "Function AccDistProcessorProjectExtension.createForProjectRevenueLine on kutsuttu virheellisesti." |
| Projektinhallinta ja kirjanpito | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Päivitä projektin arvioerätöiden luominen useiden alitehtävien suorittamisen tueksi. |
| Projektinhallinta ja kirjanpito | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Tuntilomakkeen tilaa ei voi päivittää **luonnokseksi**, kun työnkulku juuttuu **peruutettuun** tilaan. |
| Projektinhallinta ja kirjanpito | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Säilyttämissummia ei lasketa hyvityslaskun laskuehdotuksessa, jos rivejä on useita. |
| Projektinhallinta ja kirjanpito | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kun yrität muuttaa luodun laskun summaa ostotilauksesta, tapahtuu seuraava virhe: "Kupongin tapahtumat eivät ole saldossa XX/XX/XXXX. (kirjanpitovaluutta: 0,00 – raportointivaluutta: 0,01)." |
| Projektinhallinta ja kirjanpito | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Suorituskykyongelma, joka liittyy projektilaskuehdotukseen, kirjataan erätilassa **GeneralJournalAccountEntry**-liitoksen vuoksi. |
| Projektinhallinta ja kirjanpito | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Työaikaraporttia julkaistaessa on suorituskykyongelmia. |
| Projektinhallinta ja kirjanpito | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Työerittelyrakenteen kustannusarviohierarkiaa ei tasata oikein, kun kaikki tehtävät on laajennettu tai kun yksittäinen tehtävä on laajennettu manuaalisesti. |
| Projektinhallinta ja kirjanpito | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excel-projektitarjousmallia ei voi lisätä **Avaa Excelissä** -valikkoon. |
| Projektinhallinta ja kirjanpito | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Oikeushenkilön verovapautusnumeroa ei sisällytetä tulostettuun projektilaskuun. |
| Projektinhallinta ja kirjanpito | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Varastoyksikkövirheessä ei päivitetä taloustietoja, kun projektia oikaistaan suhteessa kreditriveihin. |
| Projektinhallinta ja kirjanpito | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Kun olet kohdistanut tietokannan 461935, et voi julkaista arvioita, jos siirryt jatkuvien numerosarjojen käyttöön. |
| Projektinhallinta ja kirjanpito | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** saa projektin Androidin aikataulukkomobiilisovelluksen lakkaamaan vastaamasta. |
| Projektinhallinta ja kirjanpito | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Käänteinen KET-arvo laskun kirjauksesta eroaa aikamerkinnän alkuperäisestä kirjatusta KET-arvosta. |
| Projektinhallinta ja kirjanpito | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Sovellettavissa pidätystapauksissa tositteen tapahtumat eivät ole tasapainossa, kun projektin laskutetut tulot kirjataan. |
| Projektinhallinta ja kirjanpito | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Kun **projektiresurssien aikataulutuksen suorituskyvyn parannus** -ominaisuus on käytössä, desimaaliarvot pyöristetään väärin resurssien käytettävyyden ja kapasiteetin mukaan. |
| Projektinhallinta ja kirjanpito | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Kun **Luo projektiarvioita useiden erätehtävien** -ominaisuutta käytetään, niiden arvioiden luominen erään, jossa on useita alitehtäviä, toimii vain kuluvalla ajanjaksolla. |
| Matka ja kulut | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Matkaehdotuskäytäntö ohitetaan ja työnkulku hyväksytään ilman virheitä. |
| Matka ja kulut | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobiilikulut-sovellus ei tallenna seuraavia tietoja kuluriville:</p><ul><li>Projektin tunnus</li><li>Se, onko kulu laskutettava</li><li>Aktiviteetin numero</li></ul> |
| Matka ja kulut | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | **Liitetyt kuitit** -kenttä määritetään arvoon **Kyllä**, vaikka kuluriviin ei olisi liitetty kuittia. |
| Matka ja kulut | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Virhe tapahtuu, kun kululuokaksi muutetaan **Henkilökohtainen**. |
| Matka ja kulut | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Et voi liittää kuittia ja muokata pääkuluja sen jälkeen, kun luottokorttitapahtuma on jaettu henkilökohtaiseksi kuluksi. |
| Matka ja kulut | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Kulukäytäntö ei toimi oikein niissä konsernin sisäisissä tapahtumissa, joilla on projektitunnus. |
| Matka ja kulut | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Julkaistu päivämäärätieto puuttuu julkaistuista kuluraporteista. |
| Matka ja kulut | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Kulun mobiilisovelluksessa on maksutapaongelmia. |
| Matka ja kulut | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Matkaehdotusta, joka on luotu yhdelle työntekijälle, voidaan käyttää toisen työntekijän kuluraportissa ennen delegointipäivää. |
| Matka ja kulut | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kun kulu luodaan, taloushallinnon dimensioarvojen muutoksia ei päivitetä oikein **Kulujen hallinta** -työtilan kirjanpidollisen jaon tasolla. |
| Matka ja kulut | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Pääkulurivin hyväksyntätila ei synkronoidu eritellyn rivin työnkulun hyväksynnän tilan kanssa. |
| Matka ja kulut | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Virhe, jos kirjaat kuluraportin ja veropalautus on otettu käyttöön. |
| Matka ja kulut | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Edustaja ei voi poistaa irtisanottujen työntekijöiden kuluasiakirjoja. |
| Matka ja kulut | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Kulurivin poistaminen kestää odotettua pitempään, ja se vaikuttaa suorituskykyyn. |
| Matka ja kulut | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** aiheuttaa **TaxUncommitted** -orpotietueen, koska vain **SourceDocumentLine** poistetaan. |
| Matka ja kulut | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ei todenna **trvExpTrans.ReferenceDataAreaId**-koodia, jos haluat luoda uuden numerojärjestyksen. |

## <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset

Tietoja talous- ja toimintosovellusten säädöspäivityksistä on ohjeaiheessa [Säädöspäivitykset](/dynamics365/finance/localizations/regulatory-updates). Voit myös kirjautua Microsoft Dynamics Lifecycle Services (LCS) -palveluihin ja tarkastella suunniteltuja säädöksen päivityksiä Ongelma-hakutyökalulla. Ongelmahaun avulla voit tehdä haun maan tai alueen, toiminnon tyypin ja julkaisun mukaan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
