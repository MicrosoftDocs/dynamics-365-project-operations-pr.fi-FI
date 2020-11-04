---
title: Määritä resurssin roolit
description: Resurssiroolien määrittäminen Project Servicessä
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
ms.openlocfilehash: 5f899d17980df16602c964bab4bbab1e976b3ebf
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075346"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="0dd31-103">Määritä resurssin roolit (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0dd31-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0dd31-104">Rooleilla on tärkeä osa projektin suunnittelussa, kun määritetään resurssivaatimuksia tai projektin kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="0dd31-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="0dd31-105">Kullekin roolille, joita projektit edellyttävät, sinun täytyy luoda resurssin rooli ja liittää osaamisalueet ja pätevyydet kyseiseen rooliin.</span><span class="sxs-lookup"><span data-stu-id="0dd31-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="0dd31-106">Haluat ehkä esimerkiksi luoda roolit kehittäjälle, projektipäällikkölle tai pelitestaajalle.</span><span class="sxs-lookup"><span data-stu-id="0dd31-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="0dd31-107">Määrität myös roolin edellyttämät taito- ja pätevyystasot.</span><span class="sxs-lookup"><span data-stu-id="0dd31-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="0dd31-108">Määritä resurssien roolit ja varmistaakseen tehokas projektin arvio organisaatiollesi.</span><span class="sxs-lookup"><span data-stu-id="0dd31-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="0dd31-109">Varmista myös, että määrität tarkasti laskutustyypin.</span><span class="sxs-lookup"><span data-stu-id="0dd31-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="0dd31-110">Kohde, jolle on määritetty ei-veloitettava laskutustyyppi, ei näy sopimus- tai tarjousriveillä.</span><span class="sxs-lookup"><span data-stu-id="0dd31-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="0dd31-111">Kun olet määrittänyt resurssin roolit, voit määrittää kustannus- ja myyntihinnat ja hinnaston.</span><span class="sxs-lookup"><span data-stu-id="0dd31-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="0dd31-112">Toimi seuraavasti jokaisen lisätävän roolin osalta:</span><span class="sxs-lookup"><span data-stu-id="0dd31-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="0dd31-113">Siirry kohtaan **Project Service > Resurssin roolit**.</span><span class="sxs-lookup"><span data-stu-id="0dd31-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="0dd31-114">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0dd31-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="0dd31-115">Anna **Yleinen** -alueella roolin nimi kohdassa **Nimi** ja täytä muut kentät tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0dd31-115">In the **General** area, enter a name for the role in **Name** , and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="0dd31-116">Valitse **Tallenna** ja luo tietue, jotta voit jatkaa muokkaamista.</span><span class="sxs-lookup"><span data-stu-id="0dd31-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="0dd31-117">Jos haluat lisätä osaamisalueen, valitse **Osaamisalueet** -alueella **+**.</span><span class="sxs-lookup"><span data-stu-id="0dd31-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="0dd31-118">**Roolin osaamistarve** -ruudussa valitse **Osaamisalue** -kenttä, paina **Etsi** ‑painiketta ja valitset sitten osaamisalue.</span><span class="sxs-lookup"><span data-stu-id="0dd31-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="0dd31-119">Valitse osaamisaluetta vastaava pätevyys ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0dd31-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="0dd31-120">Jatka osaamisalueiden lisäämistä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0dd31-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="0dd31-121">Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="0dd31-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="0dd31-122">Tuo tämän resurssin rooli projektien käyttöön valitsemalla **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="0dd31-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0dd31-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0dd31-123">See Also</span></span>  
 [<span data-ttu-id="0dd31-124">Resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0dd31-124">Set up resources</span></span>](../psa/set-up-resources.md)
