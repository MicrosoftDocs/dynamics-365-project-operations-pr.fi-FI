---
title: Project Finder Mobile -sovelluksen ominaisuuksien käyttöönotto
description: Project Finder Mobile -sovelluksen ominaisuuksien käyttöönotto Project Servicessä
author: JohnPBurrows
ms.prod: ''
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
ms.openlocfilehash: 8651ba591853faf648587dcbd4c50625ba94360958d7b418e89aa0bf09464a89
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004892"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Ota käyttöön Project Finder Mobile -sovelluksen ominaisuudet (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Resurssit voivat käyttää Project Finder Mobile -sovellusta puhelimessa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -palvelun kanssa ja etsiä uusia käsiteltäviä projekteja sekä päivittää osaamisalueitaan.  
  
 Tämä sovellus on saatavilla [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]-, [!INCLUDE[tn_android](../includes/tn-android.md)]- ja [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] -puhelimille.  
    
 Asetukset on valittava organisaatioyksikön parametriasetuksissa, jotta käyttäjät voivat tarkastella projektin resurssivaatimuksia ja päivittää taitojaan.
  
> [!NOTE]
>  Project Finder Mobile -sovellus toimii vain [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] -ympäristössä (ilman paikallisia asennuksia).  
  
1. Siirry kohtaan **Project Service > Parametrit**.  
  
2. Valitse parametrit, jota haluat käyttää Project Finder Mobile -sovelluksen ominaisuuksille.  
  
3. **Yleiset**-alueella aseta **Resurssivaatimukset näkyvillä resursseille** valinnaksi **Kyllä**.  
  
4. Aseta kohdan **Salli resurssin oman osaamisalueen päivittäminen** valinnaksi **Kyllä**.  
  
   ![ProjectService_ProjectFinderEnable.](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Tämä on yleinen asetus. Projektipäälliköt voivat määrittää yksittäisen projektin näkyvyyden kyseisen projektin **projektiryhmän** sivulla.  
  
   ![ProjectService_ProjectTeamVisible.](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Sähköposti-ilmoitukset  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lähettää resurssipyyntöjä koskevat sähköpostit seuraavina kellonaikoina seuraaville vastaanottajille:  
  
|Vastaanottaja|Tapahtuma|  
|---------------|-----------|  
|Projektipäällikkö|- Resurssi rekisteröidään projektiin Project Finder Mobile -sovelluksella.|  
|Resurssi|- Resurssin rekisteröimä projektityö on jo täytetty toisella resurssilla.<br />- Taitojen hyväksymispyyntö on hyväksytty tai hylätty.<br />- Projektin rekisteröitymispyyntö on hyväksytty tai hylätty.|  
  
## <a name="privacy-notice"></a>Tietosuojailmoitus  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Katso myös  
 [Resurssien määrittäminen](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]