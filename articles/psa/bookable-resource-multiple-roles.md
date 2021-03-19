---
title: Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa
description: Tässä aiheessa kerrotaan, miten hinnoitteludimensioita käytetään sellaisen resurssin hinnoittelun ja kustannusten tukemiseen, joka täyttää useita rooleja projektissa.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290985"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="fd1e7-103">Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa</span><span class="sxs-lookup"><span data-stu-id="fd1e7-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fd1e7-104">Projektipohjaiset yritykset tarvitsevat usein yhden resurssin täyttämään useita rooleja projektissa.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="fd1e7-105">Kukin näistä rooleista voidaan hinnoitella ja kustannuslaskea eri tavalla, mikä tarkoittaa sitä, että saman resurssin aika projektissa voi saada erilaisen talousarvion kunkin roolin laskutus- ja kustannushinnan mukaan.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="fd1e7-106">Project Service Automation sallii nimetyn resurssin Ryhmän jäsen -tietueen arvojen määrittämisen ja sallii eri korvaamiset kullekin tehtävälle, johon ryhmän jäsen on delegoitu.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="fd1e7-107">Seuraavassa esimerkissä selitetään, miten tämän arvon yksinkertainen korvaaminen mahdollistaa sen, että resurssilla voi olla useita rooleja projektissa, ja kussakin roolissa eri kustannus- ja laskutushinnat.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="fd1e7-108">Tehtävien luominen</span><span class="sxs-lookup"><span data-stu-id="fd1e7-108">Create tasks</span></span>
<span data-ttu-id="fd1e7-109">Luo kaksi projektitehtävää, jotka ovat 40 tuntia, tehtävä A ja tehtävä B. Valitse tehtävän B edeltäjäksi tehtävä A.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="fd1e7-110">Yleisen projektiryhmän jäsenen roolin ja organisaatioyksikön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fd1e7-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="fd1e7-111">Valitse **Aikataulu**-sivulla tehtävän A **Tehtävä**-rivi.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="fd1e7-112">Valitse **Resurssit**-kentässä avattavasta luettelosta **Luo**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="fd1e7-113">Määritä **Ryhmän jäsenen pikaluonti** -sivulla sen yleisen ryhmän jäsenen määritteet, joka voi suorittaa tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="fd1e7-114">Valitse haluamasi rooli ja organisaatioyksikkö ja valitse sitten **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="fd1e7-115">Yleinen ryhmän jäsen luodaan ja delegoidaan tähän tehtävään.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="fd1e7-116">Toista nämä vaiheet tehtävän B kohdalla ja varmista, että tehtävään B luodun yleisen ryhmän jäsenen rooli ja organisaatioyksikkö ovat eri kuin tehtävässä A.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="fd1e7-117">Projektitehtävän roolin ja organisaatioyksikön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fd1e7-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="fd1e7-118">Kun olet luonut tehtävän A, valitse se ja valitse sitten **Muokkaa tehtävää**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="fd1e7-119">Etsi **Tehtävän tiedot**-sivulla **Rooli**- ja **Organisaatioyksikkö**-kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="fd1e7-120">Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Consulting Lead** ja **Fabrikam US** organisaatioyksiköksi.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="fd1e7-121">Valitse tehtävä B ja valitse sitten **Muokkaa tehtävää**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="fd1e7-122">Etsi **Tehtävän tiedot**-sivulla **Rooli**- ja **Organisaatioyksikkö**-kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="fd1e7-123">Varmista, että **Rooli**- ja **Organisaatioyksikkö**-kenttien arvot ovat erilaiset tehtävälle B kuin tehtävälle A.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="fd1e7-124">Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Network Technician** ja **Fabrikam US** organisaatioyksiköksi.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="fd1e7-125">Tallenna ja sulje **Tehtävän tiedot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="fd1e7-126">Ryhmän jäsenen ja arvioiden toiminta</span><span class="sxs-lookup"><span data-stu-id="fd1e7-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="fd1e7-127">Valitse **Tehtävän tiedot** -sivun **Ryhmän jäsen** -kohdassa kaksi yleistä ryhmän jäsentä ja valitse sitten **Luo tarpeet**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="fd1e7-128">Valitse ryhmän jäsenen rivi **Consulting Lead** ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="fd1e7-129">Aikataulutaulukko avautuu ja varaa resurssin tälle tarpeelle.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="fd1e7-130">Valitse ryhmän jäsenen rivi **Network Technician** ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="fd1e7-131">Aikataulutaulukko avautuu ja varaa saman resurssin kyseiselle tarpeelle.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="fd1e7-132">Ryhmän jäsen -ruudukko</span><span class="sxs-lookup"><span data-stu-id="fd1e7-132">Team Member grid</span></span> 
<span data-ttu-id="fd1e7-133">Huomaa **Ryhmän jäsen** -ruudukossa, että kaksi yleistä ryhmän jäsenen tietuetta poistetaan ja että ne on korvattu yhdellä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="fd1e7-134">Kyseiselle resurssille on määritetty yksi arvojoukko, joka näyttää **Rooli**- ja **Organisaatioyksikkö**-kenttien oletusarvojoukot.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="fd1e7-135">Kun laajennat kyseisen Ryhmän jäsen -tietueen riviä, näet kummallekin tehtävälle erilliset delegoinnit Ryhmän jäsen -tietueessa.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="fd1e7-136">Kullakin delegointirivillä on tehtäväkohtaiset arvot kentille **Rooli** ja **Organisaatioyksikkö**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="fd1e7-137">Arvioruudukko</span><span class="sxs-lookup"><span data-stu-id="fd1e7-137">Estimates grid</span></span> 
<span data-ttu-id="fd1e7-138">Kun siirryt **Arviot**-ruudukkoon, huomaat, että saman resurssin molemmat delegoinnit hinnoitellaan eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="fd1e7-139">Resurssin delegointi tehtävssä A on hinnoiteltu käyttämällä **Rooli**-määritteen arvoa **Consulting Lead**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="fd1e7-140">Saman resurssin delegointi tehtävssä B on hinnoiteltu käyttämällä **Rooli**-määritteen arvoa **Network Technician**.</span><span class="sxs-lookup"><span data-stu-id="fd1e7-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]