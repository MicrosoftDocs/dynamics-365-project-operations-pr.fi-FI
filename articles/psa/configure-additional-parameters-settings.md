---
title: Lisäparametrien asetusten määrittäminen
description: Lisäparametrien asetusten määrittäminen Project Servicessä
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 75fe0aab8ea8bf41fcb98f4318380c93ac52fef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919228"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Lisäparametrien asetusten määrittäminen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kun kohteet on määritetty edellisiin artikkeleihin, projekteissa käytettävät projektin lisäparametrit on määritettävä. Loit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -asennuksen yhteydessä parametriasetuksen kaikkien [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -palvelussa tarvittavien tietueiden luomista varten. Tämän jälkeen palataan taaksepäin ja määritetään lisäkenttiä tätä asetusta varten.  
  
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
  
3. **Yleinen**-alueessa määritä projektiparametrien asetukset.  
  
4. **Hinnasto**-alueessa valitse **+** ja lisää hinnasto, valitse hinnasto avattavasta **Projektin parametrin hinnasto** -luettelosta ja valitse sitten **Tallenna**.  
  
5. Napsauta näytön oikeassa alakulmassa **Tallenna**-painiketta.  

> [!NOTE]
> Projektiparametritietue on säilytettävä, jotta Project Service toimisi oikein. Tätä tietuetta ei pitäisi poistaa.

### <a name="see-also"></a>Katso myös  
 [Resurssien määrittäminen](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
