---
title: Maaliskuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operationsin resursseihin/ei-varastoitaviin perustuvien skenaarioiden maaliskuun 2021 version päivityksessä olevista laatupäivityksistä.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 95a9251707de3699322471535aa93070ba4fb2ae
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499995"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Maaliskuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Project Operations Dataverse-ympäristön versiossa 4.8.0.91 
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.16 

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä


| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2133873 | Korjattiin **Yksikön myyntihinnan** valuuttasymbolin näkymä **Kuluarviot**-ruudukossa. |
| Laskutus ja hinnoittelu | 2174616 | Kun tarjous voitetaan, sopimuksen mukautettuun hinnastoon viitataan sopimusrivin tiedoissa, jotka kopioidaan tarjouksesta. |
| Mahdollisuuksien hallinta | 2167475 | Korjauslaskun kiinteä verosumma, josta laskuttamaton todellinen tapahtuma on peräisin. |
| Mahdollisuuksien hallinta | 2176285 | Verosummaa ei saa kopioida myyntisopimuksen/tarjousrivin tiedoista kustannuksen sopimuksen/tarjouksen rivin tietoihin. |
| Mahdollisuuksien hallinta | 2188079 | Jaettua laskutussääntöä ei saa luoda sopimuksille, jotka eivät perustu työhön. |
| Suunnittelu ja seuranta | 2125274 | **Projektin alkamispäivän yhdistämisen** **Projektin kaksoiskirjoituksen yhdistämisen** -määrite päivitetty versiosta **msdyn\_taskearlieststart** versioon **msdyn\_actualstart**. |
| Suunnittelu ja seuranta | 2138853 | Projektin kopiointitoiminto päivitettiin. Tämä varmistaa, että tehtäviin viittaavat kuluarviorivit kopioidaan kohdeprojektiin. |
| Suunnittelu ja seuranta | 2154306 | Korjattiin ongelma, jossa kuluarviot poistettiin Project Operationsissa resurssipohjaisia skenaarioita varten. |
| Suunnittelu ja seuranta | 2173259 | Kopioi projekti -toiminto päivitettiin. Näin varmistetaan, että se ei näytä **Kopioidaan työrakennetta** -virhesanomaa tietyissä skenaarioissa. |
| Aika ja kulu | 2148910 | Korjattiin näyttöongelma, jossa **Muokkaa merkintää** -sivu näkyi **Aikamerkintä**-ruudukossa. |
| Aika ja kulu | 2159798 | Ohjausobjekteja on tarkennettu, jotta varmistettaisiin, että hyväksyttyjä kulumerkintöjä ei voi muokata. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito

Lisätietoja on kohdassa [Tammikuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset

Lisätietoja Finance and Operations -sovellusten säännöstenmukaisuuspäivityksistä on kohdassa [Säännöstenmukaisuuspäivitykset](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Saat lisätietoa säännöstenmukaisuuspäivityksistä myös kirjautumalla sisään LCS:ään ja tarkastelemalla suunniteltuja säännöstenmukaisuuspäivityksiä versiohakutyökalulla. Versiohaussa voit käyttää hakuehtona maata, ominaisuustyyppiä ja versiota.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
