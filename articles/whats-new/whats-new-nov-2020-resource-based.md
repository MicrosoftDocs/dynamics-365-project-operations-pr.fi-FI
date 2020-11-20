---
title: Uudet ominaisuudet marraskuussa 2020 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operationsin resursseihin ja ei-varastoitaviin perustuvien skenaarioiden marraskuun 2020 version päivityksissä olevia laatupäivityksiä.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367261"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Uudet ominaisuudet marraskuussa 2020 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Project Operations CDS-ympäristön versiossa 4.4.0.70
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Project Operations resursseihin ja ei-varastoitaviin perustuvien skenaarioiden päivitykset

### <a name="project-operations-on-cds"></a>Project Operations CDS:ssä

| Ominaisuusalue                 | Viitenumero | Laatupäivitys                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Mahdollisuuksien hallinta       | 2036993          | Arviorivi ja resurssin delegoinnin sopimusrivit päivitetään voittavissa tarjouksissa, kun tarjousrivin tyyppi on **Kaikki tehtävät**.                                                 |
| Laskutus ja hinnoittelu          | 2070392          | Projektin sopimusrivit lisääntyvät laskussa joka kerta, kun **Päivitä laskutapahtumat** on valitaan.                                                                         |
| Projektin suunnittelu             | 2043336          | Projektitiimin jäsentietuetta ei voi poistaa.                                                                                                                                  |
| Projektin suunnittelu             | 2046013          | Arviot-merkintäsarakkeiden epäjohdonmukainen toiminta kuormituksen aikana verrattuna aikavaihetyypin muutoksen aikana.                                                                                   |
| Projektin suunnittelu             | 2046647          | Alkamis- ja päättymisaika ovat tunnin väärässä, kun resurssitarpeet luodaan projektitiimin jäsenistä.                                                                      |
| Projektin suunnittelu             | 2053879          | (Tulevan CDS-käyttöönoton mukaan) PublishUnassignedAssignments estää yrityksen tallentaa tehtävä; virhe Kohteelle ConditionOperator.In välitetty arvo on tyhjä.                       |
| Projektin suunnittelu             | 2055501          | Jos **Projektin alkamispäivä** jättäminen tyhjäksi aiheuttaa aikataulun epäonnistumisen.                                                                                                      |
| Projektin suunnittelu             | 2066817          | Yleistä resurssia ei voi luoda **Tehtävät**-välilehden henkilöiden valitsimella.                                                                                                   |
| Projektin suunnittelu             | 2067034          | **Näytä tiedot** -painike ei ole käytettävissä **Tehtävän tiedot** -sivulla.                                                                                                       |
| Resurssien hallinta          | 2046667          | Yleisiä tiimiin jäseniä ei poisteta senkään jälkeen, kun kaikki resurssit on täytetty.                                                                                                    |
| Ajan ja kulun pikamerkintä | 2047499          | Aikamerkintä-sivun **Uusi**-painike avaa **Uusi sähköpostin allekirjoitus** -sivun.                                                                                               |
| Ajan ja kulun pikamerkintä | 2059859          | Odottamaton ponnahdusikkuna avautuu kulumerkintää luotaessa.                                                                                                                         |
| Muusta                        | 2044181          | (Ostotilauksen asennuksen poistaminen) Kun Project Servicen msdyn_ProjectServiceCore_Patch- ja msdyn-perusratkaisuja yritetään poistaa, tapahtuu virhe Tietue ei ole käytettävissä.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito

| Ominaisuusalue        | Viitenumero | Laatupäivitys                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tuoton tunnistus | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Projektin arvioprosentti on valmiina virheellinen, jos sopimus käyttää ulkomaanvaluuttaa ja työn edistymisprosenttia valmistumismenetelmänä.                     |
| Tuoton tunnistus | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Arvioita ei voi kirjata **Toteutunut kustannus** -valmistumismenetelmällä.                                                                                                    |
| Tuoton tunnistus | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminointi epäonnistuu tositteen ristiriitavirheen vuoksi, kun yrityksen valuutta ja tapahtumavaluutta eivät ole samat.                                              |
| Kulujen hallinta  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Muiden kuin järjestelmänvalvojakäyttäjien kulurivisarakkeiden, kuten **Projektin tunnus** ja **Kululuokka**, hakuarvot eivät näy oikein tietoyhdistinkehyksessä. |
| Kulujen hallinta  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Kululuokkien rivin ominaisuuden oletusarvo ei näy.                                                                                                         |
| Kulujen hallinta  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Kulujen integroinnin on sisällettävä kuluraportin rivin ominaisuus.                                                                                             |
| Laskutus           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Projektin laskuehdotuksia ei voi kirjata, sillä virhesanoman mukaan FD-yhdistämää ei vahvistettu.                                                    |
| Laskutus           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Tapahtumia ei voi tarkastella **laskun** tietosivulta.                                                                                                              |
| Laskutus           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Laskuehdotusrivejä voi poistaa.                                                                                                                                  |
| Projektin kirjanpito  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **Ennuste**-valikkovaihtoehdot eivät näy **Projektit**-luettelosivulla.                                                                                                   |
| Projektin kirjanpito  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Valinta **Projektilaskelma**   > **Tapahtumat ja ennuste** ei ole mahdollinen.                                                                                                       |
| Projektin kirjanpito  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Kirjanpidon oikaisu** ei ole otettu käyttöön laskutetuissa projektitapahtumissa.                                                                                                  |
| Projektin kirjanpito  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Kirjanpidon tiedot eivät sisälly **ProjCDSActualsImport**-taulukkoon, kun **integroinnin** kirjauskansio kirjataan.                                                  |
| Projektin kirjanpito  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Projektiennustemerkintä kaksinkertaistuu, kun poistat ja sitten lisäät resurssin delegoinnin uudelleen.                                                                            |
| Projektin kirjanpito  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Projektin tunnus -linkin valitseminen ei avaa tarkan CDS-linkin URL-osoitetta.                                                                                                         |
| Projektin kirjanpito  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Tehtävän alkamispäivää ei voi päivittää CDS:ssä.                                                                                                                           |
| Projektin kirjanpito  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Useiden sopimusrivien toiminnon käyttöönottaminen ei ole mahdollista CDS-integrointia.                                                                                   |

### <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset
Lisätietoja Finance and Operations -sovellusten säännöstenmukaisuuspäivityksistä on kohdassa [Säännöstenmukaisuuspäivitykset](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Voit myös kirjautua LCS:ään ja tutustua suunniteltuihin säännöstenmukaisuuspäivityksiin käyttämällä versiohakutyökalua. Versiohaussa voit käyttää hakuehtona maata, ominaisuustyyppiä ja versiota.
