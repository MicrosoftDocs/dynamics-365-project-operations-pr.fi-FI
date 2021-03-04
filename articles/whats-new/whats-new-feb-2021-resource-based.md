---
title: Helmikuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operationsin resursseihin/ei-varastoitaviin perustuvien skenaarioiden helmikuun 2021 version päivityksessä olevista laatupäivityksistä.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141305"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Helmikuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Project Operations Dataverse-ympäristössä 4.7.0.95
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.16 

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| **Laskutus ja hinnoittelu** | 2053736 | Laskurivin tiedot ovat nyt käytettävissä kohdassa **Lasku** > **Liittyvät tiedot**. |
| **Laskutus ja hinnoittelu** | 2122613 | **Aktivoi**- ja **Poista aktivointi** -toiminnot poistettiin **Hinnasto**-kytkentäentiteeteistä. |
| **Laskutus ja hinnoittelu** | 2128606 | Ratkaistu **ullReferenceException**-ongelma **GetEstimatesForProject**-laajennuksessa. |
| **Käyttöönotto ja määritys** | 2139346 | Ratkaistu ongelma tuotaessa hallitsematonta **Dynamics365ProjectOperationsDualWrite**-ratkaisua. |
| **Käyttöönotto ja määritys** | 2140569 | Projektiratkaisua ei tule asentaa Dataverse Teams -ympäristöön. |
| **Käyttöönotto ja määritys** | 2086991 | Web-resurssien lokalisoinnin mukauttamista on rajoitettu. |
| **Mahdollisuuksien hallinta** | 2136794 | Oikea virhesanoma näytetään, kun **Vahvista lasku** tai **Merkitse lasku maksetuksi** -prosessit epäonnistuvat. |
| **Mahdollisuuksien hallinta** | 2139330 | Projektin projektipäällikön muuttaminen ei saa palauttaa omistavaa yritystä oletusarvoon. |
| **Mahdollisuuksien hallinta** | 2146376 | Korjattu verosumma ei-veloitettavassa toteutuneessa maksussa luodaan laskun vahvistuksesta. |
| **Projektin suunnittelu ja seuranta** | 2099879 | Dataverse-ympäristön käyttöönoton on luotava oletustapahtumaluokka, jolla on staattinen tunnus, eikä luotava tunnusta satunnaisesti ympäristöä kohden. |
| **Projektin suunnittelu ja seuranta** | 2128577 | Korjattu Project Servicen käyttöoikeudet resurssivarauksen tapahtumaluokan päivittämiseksi. |
| **Projektin suunnittelu ja seuranta** | 2164035 | Korjattu **Kopioi projekti** -toimintoon liittyvät ongelmat. |
| **Aikamerkintä** | 2129161 | Tiukemmat rajoitukset, jotta käyttäjät eivät voi muuttaa ja päivittää lähetettyä tai hyväksyttyä aikamerkintää. |
| **Aikamerkintä** | 2103572 | Muiden kuin projektiaikamerkintöjen aikahyväksyntä ei saa etsiä projektin hyväksyjän roolia. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito 

Lisätietoja Projektinhallinnasta ja kirjanpidosta Dynamics 365 Financessa on aiheessa [Tammikuun 2021 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Säännöstenmukaisuuspäivitykset

Lisätietoja Finance and Operations -sovellusten säännöstenmukaisuuspäivityksistä on kohdassa [Säännöstenmukaisuuspäivitykset](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Saat lisätietoa säännöstenmukaisuuspäivityksistä myös kirjautumalla sisään Lifecycle Servicesiin (LCS) ja tarkastelemalla suunniteltuja säännöstenmukaisuuspäivityksiä versiohakutyökalulla. Versiohaussa voit käyttää hakuehtona maata, ominaisuustyyppiä ja versiota.


[!INCLUDE[footer-include](../includes/footer-banner.md)]