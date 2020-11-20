---
title: Project Finder Mobile -sovelluksen ominaisuuksien käyttöönotto
description: Project Finder Mobile -sovelluksen ominaisuuksien käyttöönotto Project Servicessä
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132959"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="3b2c2-103">Ota käyttöön Project Finder Mobile -sovelluksen ominaisuudet (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3b2c2-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3b2c2-104">Resurssit voivat käyttää Project Finder Mobile -sovellusta puhelimessa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -palvelun kanssa ja etsiä uusia käsiteltäviä projekteja sekä päivittää osaamisalueitaan.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="3b2c2-105">Tämä sovellus on saatavilla [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]-, [!INCLUDE[tn_android](../includes/tn-android.md)]- ja [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] -puhelimille.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="3b2c2-106">Joudut määrittämään muutamia parametreja organisaatioyksiköllesi, jotta käyttäjät voivat tarkastella projektin resurssivaatimuksia ja päivittää taitojaan.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3b2c2-107">Project Finder Mobile -sovellus toimii vain [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] -ympäristössä (ilman paikallisia asennuksia).</span><span class="sxs-lookup"><span data-stu-id="3b2c2-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="3b2c2-108">Siirry kohtaan **Project Service > Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="3b2c2-109">Valitse parametrit, jota haluat käyttää Project Finder Mobile -sovelluksen ominaisuuksille.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="3b2c2-110">**Yleiset**-alueella aseta **Resurssivaatimukset näkyvillä resursseille** valinnaksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="3b2c2-111">Aseta kohdan **Salli resurssin oman osaamisalueen päivittäminen** valinnaksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="3b2c2-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="3b2c2-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="3b2c2-113">Tämä on yleinen asetus.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-113">This is a global setting.</span></span> <span data-ttu-id="3b2c2-114">Projektipäälliköt voivat määrittää yksittäisen projektin näkyvyyden kyseisen projektin **projektiryhmän** sivulla.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="3b2c2-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="3b2c2-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="3b2c2-116">Sähköposti-ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="3b2c2-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="3b2c2-117">lähettää resurssipyyntöjä koskevat sähköpostit seuraavina kellonaikoina seuraaville vastaanottajille:</span><span class="sxs-lookup"><span data-stu-id="3b2c2-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="3b2c2-118">Vastaanottaja</span><span class="sxs-lookup"><span data-stu-id="3b2c2-118">Recipient</span></span>|<span data-ttu-id="3b2c2-119">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="3b2c2-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="3b2c2-120">Projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="3b2c2-120">Project manager</span></span>|<span data-ttu-id="3b2c2-121">- Kun resurssi rekisteröityy projektiin Project Finder Mobile -sovelluksella.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="3b2c2-122">Resurssi</span><span class="sxs-lookup"><span data-stu-id="3b2c2-122">Resource</span></span>|<span data-ttu-id="3b2c2-123">- Kun resurssin rekisteröimä projektityö on jo täytetty toisella resurssilla.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="3b2c2-124">- Kun heidän taitojensa hyväksymispyyntö on hyväksytty tai hylätty.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="3b2c2-125">- Kun heidän projektinsa rekisteröitymispyyntö on hyväksytty tai hylätty.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="3b2c2-126">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="3b2c2-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="3b2c2-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3b2c2-127">See Also</span></span>  
 [<span data-ttu-id="3b2c2-128">Resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3b2c2-128">Set up resources</span></span>](../psa/set-up-resources.md)
