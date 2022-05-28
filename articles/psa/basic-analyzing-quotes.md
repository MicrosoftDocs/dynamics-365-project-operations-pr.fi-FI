---
title: Projektitarjousten analysointi
description: Tässä aiheessa on tietoja projektitarjousten analysoinnista.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f3bff90f91e1df8bda495912a4aad0fa69342396
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592412"
---
# <a name="analysis-of-project-quotes"></a>Projektitarjousten analysointi

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analysoi projektitarjouksia kannattavuuden arvioimiseksi. Se analysoi myös, kuinka hyvin tarjous vastaa asiakkaan odotuksia toimituspäivän tai valmistumispäivän sekä budjetoinnin osalta.

## <a name="profitability-analysis"></a>Kannattavuusanalyysi

Project Service Automation analysoi kannattavuutta käyttämällä käyttökatetta ja korjattua käyttökatetta.

- Käyttökatteet lasketaan seuraavalla kaavalla:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Korjattu käyttökate lasketaan seuraavalla kaavalla:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Jos käyttökatteen ja korjatun käyttökatteen arvoissa on suuri ero, suuri osa tarjouksen työstä on luokiteltu ei-veloitettavaksi.

## <a name="analysis-of-customer-expectations"></a>Analyysi asiakkaan odotuksista

Voit analysoida tarjouksia ja luoda kaavioita asiakkaan odotuksista aikataulun ja budjetin suhteen, jos syötät arvot seuraaville kentille:

- Tarjouksen otsikon **Pyydetty toimituspäivä** -kenttä.
- Kunkin tarjousrivin **Asiakasbudjetti** (projektiperusteisilla ja tuoteperusteisilla riveillä).

Asiakkaan odotukset aikataulun suhteen analysoidaan vertaamalla tarjousrivin tietojen myöhäisintä päättymispäivää pyydettyyn toimituspäivään kaikilla tarjouksen tarjousriveillä.

Asiakkaan odotukset budjetin osalta analysoidaan vertaamalla asiakkaan kokonaisbudjetin summaa tarjottuun summaan kaikilla tarjousriveillä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
