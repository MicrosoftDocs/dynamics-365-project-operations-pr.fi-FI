---
title: Project Finder Mobile -sovelluksen ominaisuuksien käyttöönotto
description: Project Finder Mobile -sovelluksen ominaisuuksien käyttöönotto Project Servicessä
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751109"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Ota käyttöön Project Finder Mobile -sovelluksen ominaisuudet (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Resurssit voivat käyttää Project Finder Mobile -sovellusta puhelimessa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -palvelun kanssa ja etsiä uusia käsiteltäviä projekteja sekä päivittää osaamisalueitaan.  
  
 Tämä sovellus on saatavilla [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]-, [!INCLUDE[tn_android](../includes/tn-android.md)]- ja [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] -puhelimille.  
  
 Joudut määrittämään muutamia parametreja organisaatioyksiköllesi, jotta käyttäjät voivat tarkastella projektin resurssivaatimuksia ja päivittää taitojaan.  
  
> [!NOTE]
>  Project Finder Mobile -sovellus toimii vain [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] -ympäristössä (ilman paikallisia asennuksia).  
  
1. Siirry kohtaan **Project Service > Parametrit**.  
  
2. Valitse parametrit, jota haluat käyttää Project Finder Mobile -sovelluksen ominaisuuksille.  
  
3. **Yleiset**-alueella aseta **Resurssivaatimukset näkyvillä resursseille** valinnaksi **Kyllä**.  
  
4. Aseta kohdan **Salli resurssin oman osaamisalueen päivittäminen** valinnaksi **Kyllä**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Tämä on yleinen asetus. Projektipäälliköt voivat määrittää yksittäisen projektin näkyvyyden kyseisen projektin **projektiryhmän** sivulla.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Sähköposti-ilmoitukset  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lähettää resurssipyyntöjä koskevat sähköpostit seuraavina kellonaikoina seuraaville vastaanottajille:  
  
|Vastaanottaja|Tapahtuma|  
|---------------|-----------|  
|Projektipäällikkö|- Kun resurssi rekisteröityy projektiin Project Finder Mobile -sovelluksella.|  
|Resurssi|- Kun resurssin rekisteröimä projektityö on jo täytetty toisella resurssilla.<br />- Kun heidän taitojensa hyväksymispyyntö on hyväksytty tai hylätty.<br />- Kun heidän projektinsa rekisteröitymispyyntö on hyväksytty tai hylätty.|  
  
## <a name="privacy-notice"></a>Tietosuojatiedot  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Katso myös  
 [Resurssien määrittäminen](../project-service/set-up-resources.md)
