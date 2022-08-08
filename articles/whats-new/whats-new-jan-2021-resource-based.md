---
title: Tammikuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Project Operationsin resursseihin/ei-varastoitaviin perustuvien skenaarioiden tammikuun 2021 version päivityksessä olevista laatupäivityksistä.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 4b335503139964d9d0747f9ce7addc033a512f30
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029573"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tammikuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Tämä artikkeli koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

  - Project Operations Dataverse-ympäristön versiossa 4.6.0.154
  - Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.16

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| **Käyttöönotto ja määritys** | 2106818 | Korjattu webresourcen uudelleennimeäminen, joka aiheutti sivun mukauttamiseen liittyviä ongelmia. |
| **Laskutus ja hinnoittelu** | 2091908 | Korjattu **Lukitse hinnoittelu**- ja **Käytä nykyistä hinnoittelua** -vaihtoehtojen näkyvyys **Lasku**-sivulla, kun Project Operations asennetaan yhdessä Dynamics 365 Field Servicen kanssa. |
| **Laskutus ja hinnoittelu** | 2103058 | Päivitetyt **Projektin summat**, jotka käsittelevät tehtävän todellisen kustannuksen tyhjäarvot. |
| **Laskutus ja hinnoittelu** | 2116100 | Parannetut virhesanomat, joita käytetään toiminnossa **Toteutuneiden arvojen oikeat merkinnät**. |
| **Laskutus ja hinnoittelu** | 2116129 | Parannettu kuluarvioiden näkyvyys **Projektit**-sivun **Arviot**-välilehdessä. |
| **Laskutus ja hinnoittelu** | 2119112 | Toteutuneiden myyntien ja toteutuneiden kustannusten kiinteä koostaminen, kun käytössä on eri valuuttakurssit. |
| **Laskutus ja hinnoittelu** | 2134705 | Korjattu virhe "Ei voi lukea ominaisuutta **getResourceString** määrittämätön", kun **Lasku**-sivu avataan ja Field Service asennetaan. |
| **Mahdollisuuksien hallinta** | 2022195 | **Projekti**-sivun tehtäväpohjainen laskutusruudukko sisältää kuvakkeen, joka ilmaisee, että tehtävään on linkitetty sopimus tai tarjousrivi. |
| **Mahdollisuuksien hallinta** | 2029135 | Korjattu liiketoimintaprosessin virhe, joka ilmeni, kun käyttäjä yritti avata laskurivin vahvistetusta laskusta, jonka ennakkosumma on laskutettu. |
| **Mahdollisuuksien hallinta** | 2040713 | Korjattu skriptivirhe, joka ilmeni luotaessa laskua sopimuksesta, kun Field Service on asennettu. |
| **Projektin suunnittelu ja seuranta** | 2090202 | Liiketoimintasäännöt, joita ei enää käytetä, on merkitty **vanhentuneiksi**. |
| **Aika ja kulu** | 2091249 | Ohjausobjekteja on tarkennettu siten, että käyttäjät eivät voi muuttaa tehtävää lähetetyssä tai hyväksytyssä aikamerkinnässä. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektinhallinta ja kirjanpito Dynamics 365 Financessa

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| **Projektinhallinta ja kirjanpito** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Virheellinen sopimussumma **On-account**-sivulla kiinteähintaiselle projektille, jolla on useita rahoituslähteitä. |
| **Projektinhallinta ja kirjanpito** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | **Invoiceproposal.PSAnfRefProjId**-paikkamerkki ei näytä projektitunnusta työnkululle **Projektin laskuehdotusten tarkistaminen**. |
| **Projektinhallinta ja kirjanpito** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Projektilaskuehdotuksia kirjattaessa käytetään väärää käteisalennuksen päivämäärää. |
| **Projektinhallinta ja kirjanpito** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Resurssien delegoinnin poistaminen ja lukeminen Project Operationsissa kaksinkertaistaa projektiennusteen tapahtumat Financessa. |
| **Projektinhallinta ja kirjanpito** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Project Operationsin projektiarvioita ei voi luoda Dataversessä ilman projektin sopimusriviä. |
| **Projektinhallinta ja kirjanpito** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Projektin kulutapahtuman taloushallinnon dimensiota ei synkronoida liittyvän tositteen ja kuluraportin kirjanpidollisen jaon kanssa, kun kuluraportti kirjataan saldoon. |
| **Projektinhallinta ja kirjanpito** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | **Laskun tilan** suodatin kirjatuille projektin tapahtumille kiinteähintaisissa projekteissa ei toimi. |
| **Projektinhallinta ja kirjanpito** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Käänteisen arvion poistaminen ei toimi **Kausittainen**-osassa. |
| **Projektinhallinta ja kirjanpito** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Laskuehdotuksen rivejä voidaan poistaa Dataversen kanssa integroidussa Project Operationsissa. |
| **Projektinhallinta ja kirjanpito** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Estä useiden sopimusrivien käyttöönotto -ominaisuus ilman Dataverse-integraatiota. |
| **Projektinhallinta ja kirjanpito** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Kun tilin laskutus on yhtä kuin voitto ja tappio, laskutettu tuotto listataan nollana Arviot-sivulla. |
| **Projektinhallinta ja kirjanpito** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Laskukorjaukset eivät toimi integroiduissa ympäristöissä. |
| **Projektinhallinta ja kirjanpito** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | KET-myyntiarvon kirjaaminen konsernin sisäisessä projektilaskutuksessa valitsee väärän tilin. |
| **Projektinhallinta ja kirjanpito** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Project Operationsin arviotehtävien riippuvuuksia Dataversessä ei voi päivittää. |
| **Projektinhallinta ja kirjanpito** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Project Operations -integroinnin kirjauskansioiden toistuva poistaminen Finance-liideistä johtaa tietojen menetykseen. |
| **Projektinhallinta ja kirjanpito** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Seuraava virhe ilmenee, kun projektin laskuehdotus kirjataan: "Tapahtuma ei täsmää raportointivaluutassa, kun vähennetty ennakkolasku lisätään". |
| **Projektinhallinta ja kirjanpito** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Väärä projektitunnus sisältyy vähennyksiin, kun oletusprojektisopimus on päivitetty Project Operationsissa. |
| **Projektinhallinta ja kirjanpito** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Arvion ja tuoton tunnistusta ei voi suorittaa, kun Project Operations on otettu käyttöön. |
| **Projektinhallinta ja kirjanpito** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operationsissa projektin poistaminen sopimuksesta ei palauta sopimuksen oletusprojektia. |
| **Projektinhallinta ja kirjanpito** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operationsin konsernin sisäisessä laskussa näkyy väärät kulurivit **Lisää rivi** -luettelossa. |
| **Matka ja kulut** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Kulurivejä ei voi kirjata, koska tuntiasetukset puuttuvat sopimusriviltä. |
| **Matka ja kulut** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Kun projektin/luokan tarkistus on pakollista, projektiin liittyvät kululuokat eivät näy kuluraportissa. |
| **Matka ja kulut** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Käteisennakkosaldoa ei päivitetä, kun kuluraportti kirjataan rivin mukaan. |
| **Matka ja kulut** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | **Päivitä maksutiedot** -työ epäonnistuu käänteisten selvitysten jälkeen, kun laskun selvitykseen liittyy vähintään kaksi maksutapahtumaa. |
| **Matka ja kulut** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Ongelma päivärahakululuokan viimeisen päivän ateriavähennyksen laskennassa. |
| **Matka ja kulut** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | **Kulutyyppi työntekijää kohden** -raportti ei näytä eriteltyjä kuluja, jos käyttäjän ensimmäinen yhteys on ollut kielellä es-MX. |
| **Matka ja kulut** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Kuluraportin laskun toimittajan maksu käyttää väärää yhteenvetotiliä selvityksen kirjausta varten. |
| **Matka ja kulut** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Kun kuluraportti kirjataan käyttäen määritystä **Salli tapahtumien ryhmittely ennakkomaksutilin perusteella** ja **Kirjanpidon päivämäärän oikaiseminen kirjauksen aikana** -määrityksen ollessa käytössä näyttää, että kirjanpitopäivämääriä ei ryhmitellä **Kirjanpidon jakelu** -taulukossa, mikä vaikuttaa arvonlisäverotietueisiin. |
| **Matka ja kulut** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Kulun aliluokan yhdistämismääritys poistetaan, kun Käytä kulussa -valintaruudun valinta poistetaan ja valitaan uudelleen. |
| **Matka ja kulut** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Konsernin sisäistä kuluraporttia ei voi luoda, jos projektitunnus on lisätty otsikkotasolle. |
| **Matka ja kulut** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Kulujen maksuongelma, kun kulujen summa on suurempi kuin käteisennakon määrä. |
| **Matka ja kulut** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Konsernin sisäisen kuluraportin **Projektitunnus**-kenttä on tyhjä, jos käyttäjärooli on delegoitu tietylle organisaatiolle. |
| **Matka ja kulut** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kululuokka lukitaan, kun uusi kulurivi lisätään. |
| **Matka ja kulut** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Jo jaettujen kuluraporttirivien erittely johtaa epätäydelliseen ostoreskontraan\pääkirjaan kirjauksen tositteeseen. Koska **TRVEXPTRANS.SOURCEDOCUMENTLINE** on päällekkäinen, myös Accounting Source Explorer on rikkinäinen. |
| **Matka ja kulut** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Asiakkaan päällekkäiseen **TRVREQUISITIONLINE**-taulukkoon lisätty indeksi saa aikaan virheen päivityksen aikana. |
| **Matka ja kulut** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operationsissa ei voi luoda tai hyväksyä Dataversen konsernin sisäisten tehtävien aikaa. |

## <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset

Tietoja talous- ja toimintosovellusten säädöspäivityksistä on ohjeaiheessa [Säädöspäivitykset](/dynamics365/finance/localizations/regulatory-updates). Voit myös kirjautua LCS:ään ja tutustua suunniteltuihin säännöstenmukaisuuspäivityksiin käyttämällä versiohakutyökalua. Versiohaussa voit käyttää hakuehtona maata, ominaisuustyyppiä ja versiota.


[!INCLUDE[footer-include](../includes/footer-banner.md)]