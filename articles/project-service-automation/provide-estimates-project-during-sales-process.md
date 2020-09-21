---
title: Anna projektin työarvioinnit myyntiprosessin aikana
description: Työarviointien antaminen projektille myyntiprosessin aikana Project Servicessä
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751232"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="c2c0d-103">Anna projektin työarvioinnit myyntiprosessin aikana (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c2c0d-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c2c0d-104">Myyntiprosessin aikana voit käsitellä myyntiarviota alhaalta ylöspäin tarjouspyynnön riveillä.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="c2c0d-105">-ratkaisun [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -toiminnot ovat tieteellisempi ja määrätietoisempi tapa muodostaa myyntiarviota erittelemällä työkohteita ja liittämällä oikeanlaisia määritteitä, jotka vaikuttavat projektin työrakenteen arvioihin.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="c2c0d-106">Kun voitat myynnin, voit käyttää liittyvää työrakennetta projektisuunnitelmassa, määrittelemällä sen tarvittaessa uudelleen projektin viemiseksi onnistuneesti päätökseen.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="c2c0d-107">Linkitä projekti tarjouspyynnön riviin</span><span class="sxs-lookup"><span data-stu-id="c2c0d-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="c2c0d-108">Kun luot projektipohjaisen tarjouspyyntörivin, voit luoda uuden projektin tarjouspyynnön rivistä.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="c2c0d-109">Voit sitten käyttää projektimalleja, jotka ovat joko valmiiksi määritetyn standardin mukaisia projektisuunnitelmia ja organisaation yhteisiä rahoitusta koskevia arvioita tai kopio projektisuunnitelmasta ja edelliseen projektiin perustuvia arvioita.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="c2c0d-110">Kun luot projektin, projektimallin valinta luo pohjan projektisuunnitelman, arvioiden ja roolin vaatimusten tarkentamiselle.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="c2c0d-111">Luomalla projektin tarjouksesta, projekti liitetään automaattisesti tarjouspyynnön riviin.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="c2c0d-112">Projektin arvion komponentit</span><span class="sxs-lookup"><span data-stu-id="c2c0d-112">Project estimate components</span></span>  
 <span data-ttu-id="c2c0d-113">Projektin työrakenteen avulla työ voidaan eritellä tehtäviksi, ylläpitää tehtävähierarkiaa ja delegoida kunkin tehtävän suorittamiseen tarvittavan työmäärän arvio.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="c2c0d-114">Voit myös liittää roolit tehtävään osoittamaan arvioituja resurssin tyyppejä, joita tarvitaan tehtävän ja aikataulun suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="c2c0d-115">Työrakenne auttaa sinua määrittämään työmäärä- ja aikatauluarviot.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="c2c0d-116">Projekti käyttää oletusarvoisesti oletushinnastot, jotka on aiemmin määritetty.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="c2c0d-117">Hinnastossa määritetyt kustannukset ja hinnat auttavat määrittämään projektin työrakenteen taloudelliset arviot.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="c2c0d-118">Jos projektiin on liitetty tarjous, tarjouksella on oletusarvoisesti eri hinnasto. Tarjouksen hinnastoa käytetään rahoitusta koskevissa arvioissa.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="c2c0d-119">Tuo arvioita projektista tarjoukseen</span><span class="sxs-lookup"><span data-stu-id="c2c0d-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="c2c0d-120">Kun projektissa on projektiarvioita, voit tuoda nämä arviot tarjouspyynnön riville.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="c2c0d-121">**Tarjousrivin tiedot**-kohdassa valitse **Tuo kustannusarvioista**.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="c2c0d-122">Valitse, tuotko projektin arvioita, jotka on tiivistetty tapahtumatyypin, roolin tai työrakenteen solmun tasolla.</span><span class="sxs-lookup"><span data-stu-id="c2c0d-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c2c0d-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c2c0d-123">See Also</span></span>  
 [<span data-ttu-id="c2c0d-124">Projektipäällikön opas</span><span class="sxs-lookup"><span data-stu-id="c2c0d-124">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
