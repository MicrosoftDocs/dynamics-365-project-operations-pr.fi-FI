---
title: Uudet ominaisuudet joulukuussa 2020 – Project Operations resursseihin/ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operationsin resursseihin/ei-varastoitaviin perustuvien skenaarioiden joulukuun 2020 version päivityksessä olevista laatupäivityksistä.
author: sigitac
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3889402ab991e307bc3fe5463098dfab383a53b4
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727876"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Uudet ominaisuudet joulukuussa 2020 – Project Operations resursseihin/ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Project Operations Dataverse-ympäristön versiossa 4.5.0.134
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.15

Tietoja tämän version päivittämisestä on aiheessa [Project Operationsin päivittäminen Finance-ympäristössä](ur5-nonstocked-installation.md).

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet
Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

  - [Konsernin sisäinen laskutus](../project-accounting/intercompany-invoicing-overview.md) 
  - [Asiakkaiden ennakkomaksut ja maksuennakot](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Project Operations resursseihin ja ei-varastoitaviin perustuvien skenaarioiden päivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue                    | Viitenumero | Laatupäivitys                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Laskutus ja hinnoittelu             | 1986009          | Manuaalisesti luotujen kirjauskansion rivien suorituskyky on epäyhtenäinen, kun ne vahvistetaan ennen kuin projekti linkitetään sopimusriviin tai poistetaan siitä                     |
| Laskutus ja hinnoittelu             | 2028174          | Laskun rivin tietojen päivitysten tulisi noudattaa korjauskirjauskansion logiikkaa                                                                                  |
| Laskutus ja hinnoittelu             | 2028315          | Muokattavan sisäkkäisen ruudukon käyttäytymisen korjaukset                                                                                                                        |
| Laskutus ja hinnoittelu             | 2031070          | Korjauslaskun rivin tietojen muokkaamisen tulisi noudattaa korjauskirjauskansion logiikkaa                                                                              |
| Laskutus ja hinnoittelu             | 2034186          | Projekti on pystyttävä päivittämään sopimusrivillä                                                                                                        |
| Laskutus ja hinnoittelu             | 2034206          | Muokkauksen tila täytyy määrittää todellisen peruutuksen aikana, kun projektin linkitys sopimusriviin puretaan                                                        |
| Laskutus ja hinnoittelu             | 2040871          | Salli yksikön ja yksikköryhmän solupäivitykset kuluarvioruudukossa                                                                                       |
| Laskutus ja hinnoittelu             | 2053754          | Laskujen muokkauksista luotuihin todellisiin arvoihin ei merkitä muokkaustilaa ja laskutustilaa                                                                |
| Laskutus ja hinnoittelu             | 2057874          | Laskurivin tietojen muokkauksen aikana luodun tapahtuman yhteyden korjaaminen                                                                                     |
| Laskutus ja hinnoittelu             | 2057875          | Laskurivin tietojen muokkauksen aikana luodun tapahtuman alkuperän korjaaminen                                                                                        |
| Laskutus   ja hinnoittelu           | 2057944          | Ei voi ylittää -tilaksi on määritetty Sidottu todellisille arvoille, jotka eivät ole valmiita laskutusta varten laskun korjauksesta                                             |
| Laskutus   ja hinnoittelu           | 2066169          | Päivitä kirjanpitopäivämäärä negatiivisille laskuttamattoman myynnin tietueille yhdistettäessä kaksoiskirjoittamisen avulla                                                            |
| Laskutus   ja hinnoittelu           | 2067622          | Käsittelykuvake tulisi näyttää välitavoitteita luotaessa                                                                                                |
| Laskutus   ja hinnoittelu           | 2067624          | Sopimussumma tulisi merkitä Liiketoiminnan suosittelemaksi välitavoitteita luotaessa                                                                      |
| Laskutus   ja hinnoittelu           | 2086880          | Piilota **Ehdotus**-painike valintanauhassa projektiin perustuville tarjousriveille                                                                                                |
| Laskutus   ja hinnoittelu           | 2098140          | Näytä **Korjaa lasku** -painike integroiduille ympäristöille                                                                                             |
| Käyttöönotto   ja määritys  | 2101152          | Uudessa ympäristössä, joka on luotu käyttämällä  Project Operations -mallia Power Platform Admin Centeristä, on oltava kaikki asennuksen jälkeiset toiminnot suoritettuina               |
| Mahdollisuuksien   hallinta        | 2086601          | Passivoituja rooleja ja luokkia ei tulisi kopioida Laskutettavien roolien ja Laskutettavien luokkien luetteloon tarjousriveillä ja sopimusriveillä |
| Projektin   suunnittelu ja seuranta | 1949065          | Tietojen näkyvyys toimii oikein 200 % zoomilla                                                                                                                   |
| Projektin   suunnittelu ja seuranta | 2046317          | Mahdollisuus nimetä projekti-entiteetti uudelleen Project Operationsissa                                                                                   |
| Projektin   suunnittelu ja seuranta | 2057171          | Päivitetty virhesanoma, kun **Projektin alkamispäivä** -kenttä on tyhjä **Projekti**-sivulla                                                           |
| Projektin   suunnittelu ja seuranta | 2057197          | Arviorivin kopiota, jossa on tehtäväviittaus, ei tueta                                                                                                     |
| Projektin   suunnittelu ja seuranta | 2060687          | Aikavyöhykevaroitus poistuu nyt määritetyn ajan kuluttua                                                                                                      |
| Resurssien   hallinta           | 1832887          | Oletusresurssiluokan tunnuksen on oltava staattinen toistettavan tietojen hakemisen varmistamiseksi Dataverse- ja Finance-ympäristöistä                                                 |
| Aika ja   kulu              | 2081793          | **Kululuokan nimi** on yhdistettävä **Kululuokan kuvaus** -kenttään Finance and Operations -sovelluksissa                                                  |
| Aika ja   kulu              | 2034882          | **Uusi**-painike näkyy aikamerkinnöille kaksi kertaa komentopalkissa, kun Dynamics 365 Field Service on asennettu                                          |
| Aika ja   kulu              | 2056028          | Päivitä **Ajan muokkaus** -sivu sisältämään aikajanan                                                                                                              |
| Aika ja   kulu              | 1983747          | Ajansyöttökaavio näyttää lisätietoja                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito

| Ominaisuusalue                        | Viitenumero | Laatupäivitys                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektinhallinta ja kirjanpito | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | Nimiketarpeen palautusten muokkaukset estetty                                                                                                                                                                                                        |
| Projektinhallinta ja kirjanpito | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | Lomakehuomautukset, jotka eivät näy muotoilluissa projektilaskuissa                                                                                                                                                                                                          |
| Projektinhallinta ja kirjanpito | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | MEXICO CFDI 33 projektilaskuille ei ole sallittua päivittää maksutapaa laskuehdotuksesta                                                                                                                                                           |
| Projektinhallinta ja kirjanpito | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | Parametria, joka määrittää kirjanpitopäivämäärän automaattisesti avoimelle kaudelle, ei oteta huomioon **Integraatio**-kirjauskansiossa                                                                                                                                                             |
| Projektinhallinta ja kirjanpito | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Ennustevalikkovaihtoehdot eivät näy **Projektit**-luettelosivulla                                                                                                                                                                                                      |
| Projektinhallinta ja kirjanpito | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | **Projektilaskelma** > **Tapahtumat ja ennuste** ei aukea                                                                                                                                                                                                      |
| Projektinhallinta ja kirjanpito | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Resurssien delegoinnin poistaminen ja lukeminen kaksinkertaistaa projekti ennusteen tapahtumat Financessa                                                                                                                                                                   |
| Projektinhallinta ja kirjanpito | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | Projektiarvioiden luominen ei onnistu Dataversessä, jos projektissa ei ole sopimusriviä                                                                                                                                                                 |
| Projektinhallinta ja kirjanpito | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Poisto epäonnistuu tositteen ristiriitavirheen vuoksi, kun yrityksen valuutta ja tapahtumavaluutta ovat  erit                                                                                                                                            |
| Projektinhallinta ja kirjanpito | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | Laskun tilan suodatin kirjatuille projektin tapahtumille kiinteähintaisissa projekteissa ei toimi                                                                                                                                                            |
| Projektinhallinta ja kirjanpito | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Tehtävän alkamispäivää ei voi päivittää Dataversessä                                                                                                                                                                                                                    |
| Projektinhallinta ja kirjanpito | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | Laskuehdotuksen rivejä voidaan poistaan Project Operationsin integroidussa skenaariossa                                                                                                                                                                                    |
| Projektinhallinta ja kirjanpito | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | Laskuehdotuksen  rivejä voidaan poistaan Project Operationsin integroidussa skenaariossa                                                                                                                                                                                    |
| Projektinhallinta ja kirjanpito | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Estä useiden sopimusrivien käyttöönotto -ominaisuus ilman Dataverse-integraatiota                                                                                                                                                                                        |
| Projektinhallinta ja kirjanpito | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | Arvionäytön laskutettu tuotto on nolla(0), kun Tilin laskutus = voitto ja tappio                                                                                                                                                                          |
| Projektinhallinta ja kirjanpito | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | Käynnissä oleva työ – myyntiarvon kirjaaminen yritysten välisessä projektilaskutuksessa poimii odottamattoman tilin                                                                                                                                                                           |
| Projektinhallinta ja kirjanpito | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | Arviota/tuoton kirjaamista ei voi suorittaa, jos Project Operations on otettu käyttöön                                                                                                                                                                         |
| Aika   ja kulut                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | Edustajan syöttäma kulu palautetaan kulukäyttäjälle eikä edustajalle                                                                                                                                                                                           |
| Aika   ja kulut                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | Kuluraportin työnkulun delegointikäyttäjän lähettäessä työnkulun häntä ei tunnisteta työnkulun aloittajaksi                                                                                                                                                             |
| Aika   ja kulut                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | Yrityksen ohitusten oletusdimensiot eivät näy yritysten välisissä kuluraporteissa                                                                                                                                                                    |
| Aika   ja kulut                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | Ongelma päivärahakululuokan viimeisen päivän ateriavähennyksen laskennassa                                                                                                                                                                                    |
| Aika   ja kulut                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | **Täsmäytettävä summa** -kenttä **Matkaehdotus**-sivulla ei päivity, kun kulurivin nimike poistetaan kuluraportista, joka liittyy matkaehdotukseen                                                                                                       |
| Aika   ja kulut                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | Kuluraportti vahvisti käytännön työnkulkuun lähettämisen jälkeen                                                                                                                                                                                           |
| Aika   ja kulut                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | Matkakulukuitit eivät näy oikein merkinnän edustajalle                                                                                                                                                                                            |
| Aika   ja kulut                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | Kulutyyppi työntekijää kohti ei näytä eriteltyjä kuluja, kun käyttäjän kieleksi on määritetty es-MX                                                                                                                         |
| Aika   ja kulut                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | Kuluraportti sallii väärän alaluokan syöttämisen kululuokalle                                                                                                                                                                                       |
| Aika   ja kulut                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | Käteisennakon täsmäytys kuluraportin kanssa ei toimi odotetulla tavalla, kun kuluraportin summa on suurempi kuin käteisennakon määrä                                                                                                           |
| Aika   ja kulut                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | Suorituskykyongelmia liittyen ProjProjectLookup-kyselyihin. Asiakas on estetty, koska kyselyn suorittaminen vie kauan aikaa.                                                                                                                     |
| Aika   ja kulut                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | Kuluraportit, jotka on kirjattu käyttäen määritystä **Salli tapahtumien ryhmittely ennakkomaksutilin perusteella** ja **Kirjanpidon päivämäärän oikaiseminen kirjauksen aikana** -määrityksen ollessa käytössä näyttää, että kirjanpitopäivämääriä ei ryhmitellä **Kirjanpidon jakelu** -taulukossa, mikä vaikuttaa arvonlisäverotietueisiin |
| Aika   ja kulut                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | Tuodut luottokorttitapahtumat, joiden valuutta on ulkomaan valuutta, luovat virheellisiä toimittaja tapahtumia, jos **Käänteinen arvonlisävero** on käytössä kuluraportin riveillä                                                                                                                     |
| Aika   ja kulut                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | Yritysten välistä kuluraporttia ei voi luoda, jos projektitunnus on lisätty otsikkotasolle                                                                                                                                                                 |
| Aika   ja kulut                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | Kulujen maksuongelma, kun kulujen summa on suurempi kuin käteisennakon määrä                                                                                                                                                                          |
| Aika   ja kulut                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | Yritysten välisen kuluraportin projektitunnustiedot ovat tyhjät, jos käyttäjärooli on delegoitu tietylle organisaatiolle                                                                                                                                           |
| Aika   ja kulut                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | Kuluraportin automaattinen kirjaustyönkulku on valmis, mutta laskua ei kirjata                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset
Lisätietoja Finance and Operations -sovellusten säännöstenmukaisuuspäivityksistä on kohdassa [Säännöstenmukaisuuspäivitykset](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Voit myös kirjautua LCS:ään ja tutustua suunniteltuihin säännöstenmukaisuuspäivityksiin käyttämällä versiohakutyökalua. Versiohaussa voit käyttää hakuehtona maata, ominaisuustyyppiä ja versiota.


[!INCLUDE[footer-include](../includes/footer-banner.md)]