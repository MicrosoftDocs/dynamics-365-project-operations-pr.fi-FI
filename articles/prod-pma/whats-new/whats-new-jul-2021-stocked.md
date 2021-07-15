---
title: Heinäkuun 2021 uudet ja muuttuneet ominaisuudet – Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa
description: Tässä aiheessa on tietoja laatupäivityksistä, jotka ovat käytettävissä Project Operationsin heinäkuussa 2021 julkaistussa versiossa varastoitavien ja tuotantopohjaisissa skenaarioissa.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: fb1814330b5e474ccbda0ab85dd67758a6f270a9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334531"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Heinäkuun 2021 uudet ja muuttuneet ominaisuudet – Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa

_**Koskee:** Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.20
 
### <a name="quality-updates"></a>Laatupäivitykset
                                                                                                                                                                                  
| Ominaisuusalue                      | Viitenumero| Laatupäivitys                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektinhallinta ja kirjanpito | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Ostositoumustietueet ostoehdotuksesta tyhjennetään heti, kun ostotilaus vapautetaan ostoehdotuksesta.                                                                           |
| Projektinhallinta ja kirjanpito | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Budjetin tarkistus tapahtuu kahdesti ostoehdotuksessa. Tämän kahdennuksen vuoksi hankintapyyntöä ei voi sulkea eikä vastaavaa ostotilausta luoda.                                                                                                                        |
| Projektinhallinta ja kirjanpito | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | **Laskutusprosentti**-laskutussääntöä ei voi suorittaa pyöristysongelman vuoksi.                                                                              |
| Projektinhallinta ja kirjanpito | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Kun oikaiset tapahtuman ja prosenttiosuutena on desimaalit, kustannusta ja myyntihintaa ei muuteta oikein.                                      |
| Projektinhallinta ja kirjanpito | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Kirjanpidon lähteen hallinta näyttää tunnit yhdelle tuntilomakkeen riville katseltaessa useita tuntilomakkeen rivejä, joilla on eri aktiviteetteja.                                      |
| Projektinhallinta ja kirjanpito | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Tallennettujen näkymien ja tuntilomakeriivn yksityiskohtien mukauttaminen aiheuttaa sen, että järjestelmä avaa aina ensimmäisen tuntilomakkeen tiedot luettelossa, kun se yrittää avata tuntilomakkeen.  |
| Projektinhallinta ja kirjanpito | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Projektin pääsolmu katoaa näkyvistä ja työrakenteen tietueet poistetaan tuonnin jälkeen.                                                                                             |
| Projektinhallinta ja kirjanpito | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Kun nimikkeet vastaanotetaan ja lähetetään osittain nimikevaatimuksesta, järjestelmä päivittää väärän budjetin tasapainon. |
| Projektinhallinta ja kirjanpito | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Projektin pidätettyjen ostotilausten summat eivät näy oikein **Summat** -ruudussa tai **Odottava lasku** -ruudussa.                                                                  |
| Projektinhallinta ja kirjanpito | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Kun suljet varastoa, projektinimikkeen kustannusten oikaisut kirjataan tulostilin asemesta saldotilille.                                                            |
| Projektinhallinta ja kirjanpito | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Projektin kirjaamalla tapahtumatositteella ja arviotositteella kirjanpitovaluutana käytetään USD:tä, mutta summa näyttää summan, joka vastaa CAD-summaa.              |
| Projektinhallinta ja kirjanpito | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Sidotut kustannukset, joilla on nimiketarve ja ostotilaus, ovat virheellisiä ostotilauksen laskuprosessissa, kun tuotteen osakuittaus ja osalaskutus on tehty.       |
| Projektinhallinta ja kirjanpito | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Projektin oikaisu ei päivitä myyntisummaa oikein välillisin kustannuksin.                                                                                    |
| Projektinhallinta ja kirjanpito | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | **Työaikalomake**-taulokosta puuttuu määritetty suhde **Työntekijä tai resurssi** -näkymään.                                                                                   |
| Projektinhallinta ja kirjanpito | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | **Aktiviteettinumero**-kenttää ei voi täyttää, kun valitset sen konsernin sisäisen aikaraportin avattavasta valikosta.                                                                 |
| Projektinhallinta ja kirjanpito | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Mukautettua **Tarkoitus**- tai **Aktiviteetin kuvaus** -kenttää ei voi lisätä seuraaville sivuille: **Projektin kirjattu tapahtuma**, **Laskuehdotuksen luominen** tai **Laskuehdotus**.  |
| Projektinhallinta ja kirjanpito | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Väärä toimituspäivän ohjausobjekti annetaan, kun luot nimiketarpeita tietojen hallinnan (**ProjSalesItemRequirementEntity**) avulla.                                              |
| Projektinhallinta ja kirjanpito | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Kun valitset Financessa projektisopimustunnuksen, integroitu Project Operations -ympäristö avaa sivun ja luo uuden tietueen aiemmin luodun projektisopimussivun avaamisen asemesta.                                                                                                                 |
| Projektinhallinta ja kirjanpito | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Merkintää ”@SYS4083080” (”Unable to find a unique Worker record   corresponding to the entered values”) ei ole käännetty tanskan kielelle.                                |
| Projektinhallinta ja kirjanpito | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | **Nimikkeen arvonlisäveroryhmä** -kenttää ei voi muokata laskuehdotuksessa.                                                                               |
| Projektinhallinta ja kirjanpito | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Sidottu kustannus on liian suuri, kun käytössä on arvonlisäverosummia, jotka eivät ole vähennyskelpoisia.                                                                                                    |
| Projektinhallinta ja kirjanpito | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Yritysten välisen tuntilomakkeen, jossa on useita projekteja ja taloushallinnon dimensioita, kirjaaminen luo odottamattomia arvoja pääkirjanpitoon.                             |
| Projektinhallinta ja kirjanpito | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Laskuehdotusrivitovat päällekkäisiä, koska samanaikaisesti käynnissä on useita **tuo väliympäristöstä** -vaiheittaisten jaksottaisten prosessien esiintymiä.                                      |
| Projektinhallinta ja kirjanpito | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Hyvityslaskun laskuehdotuksessa on virhe, joten tositteen tapahtumat eivät täsmää.    |
| Projektinhallinta ja kirjanpito | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Projektin sidotut kustannukset muuttuvat virheellisiksi, kun pidossa olleet laskut vapautetaan.                                                                             |
| Projektinhallinta ja kirjanpito | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Hyvityslaskua ei voi luoda projektin myyntitilaukselle, jos vero on eri valuuttana kuin yrityksen valuutta.                                      |
| Projektinhallinta ja kirjanpito | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Palvelusopimuksen poistaminen poistaa myös asiakkaaseen liittyvän osoitteen.                                                                                     |
| Projektinhallinta ja kirjanpito | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Negatiivisesta aikatapahtuman korjauksesta johtuvaa laskuehdotusta ei voi kirjata.                                                                    |
| Matka ja kulut                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Vero lasketaan kuluraporteissa eri tavalla.                                                                                                                  |
| Matka ja kulut                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Julkaisupäivitys **DB72_Expense.updateTrvExpTransProjTransId()** ei salli **trvExpTrans.ReferenceDataAreaId**:n luoda uutta numerosarjaa.                    |
| Matka ja kulut                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Esitetty summa ei näy pakollisessa kentässä.                                                                                                             |
| Matka ja kulut                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Suorituskykyparannuksia kulun liittämisessä kuluraporttiin, kun käytetään Uudelleen suunnitellut kulut -käyttöliittymää.                                                            |
| Matka ja kulut                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Voit poistaa julkaistuja kuluraportteja.                                                                                           |
| Matka ja kulut                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Kulukäytäntösanoma näkyy useita kertoja.                                                                                                       |
| Matka ja kulut                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | **Maksutapa**-kenttä näkyy **Uusi kulu** -ruudussa.                                                                                                       |
| Matka ja kulut                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | **Palauta kuluasiakirjan tila** -työkalun tulisi asettaa kuluraportin tilaksi **Luonnos**, jos työnkulkua ei löytynyt. 

### <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset
Lisätietoja Finance and Operations -sovellusten säännöstenmukaisuuspäivityksistä on kohdassa [Säännöstenmukaisuuspäivitykset](/dynamics365/finance/localizations/regulatory-updates). Voit myös kirjautua Lifecycle Services (LCS) -palveluihin ja tarkastella suunniteltuja säädösten päivityksiä Issue-hakutyökalulla. Versiohaussa voit käyttää hakuehtona maata, ominaisuustyyppiä ja versiota.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
