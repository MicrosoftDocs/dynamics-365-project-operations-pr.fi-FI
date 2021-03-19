---
title: Projektitarjousten analysointi
description: Tässä aiheessa on tietoja projektitarjousten analysoinnista.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291255"
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