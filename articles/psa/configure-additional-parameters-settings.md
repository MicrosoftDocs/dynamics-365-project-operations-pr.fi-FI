---
title: Lisäparametrien asetusten määrittäminen
description: Lisäparametrien asetusten määrittäminen Project Servicessä
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075348"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Lisäparametrien asetusten määrittäminen (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kun olet määrittänyt kohteet edellisiin aiheisiin, sinun on tehtävä muiden projektiparametrien asetukset, joita käytetään projektissa. Loit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -asennuksen yhteydessä parametriasetuksen kaikkien [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -palvelussa tarvittavien tietueiden luomista varten. Tämän jälkeen palataan taaksepäin ja määritetään lisäkenttiä tätä asetusta varten.  
  
 Seuraavat asetukset pitää määrittää:  
  
-   Organisaatioyksikkö  
  
-   Laskutustiheys  
  
-   Työtuntimalli  
  
-   Hinnasto  
 
Tässä vaiheessa voit myös osoittaa, miten resurssit kohdistetaan:  
  
- **Keskitetty**. Vain resurssipäälliköt voivat kohdistaa resursseja projekteihin.  
  
- **Hybridi**. Projektien resursseja voivat kohdistaa resurssipäälliköt, projektipäälliköt ja asiakkuuspäälliköt.  
  
 
Projektin parametriasetusten tekeminen:  
  
1. Siirry kohtaan **Project Service > Parametrit**.  
  
2. Valitse parametrien asetus, jonka haluat määrittää (sama, jonka loit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -asennuksen yhteydessä), tai luo uusi valitsemalla **Uusi**.  
  
3. **Yleinen** -alueessa määritä projektiparametrien asetukset.  
  
4. **Hinnasto** -alueessa valitse **+** ja lisää hinnasto, valitse hinnasto avattavasta **Projektin parametrin hinnasto** -luettelosta ja valitse sitten **Tallenna**.  
  
5. Napsauta näytön oikeassa alakulmassa **Tallenna** -painiketta.  

> [!NOTE]
> Projektiparametritietue on säilytettävä, jotta Project Service toimisi oikein. Tätä tietuetta ei pitäisi poistaa.

### <a name="see-also"></a>Katso myös  
 [Resurssien määrittäminen](../psa/set-up-resources.md)
