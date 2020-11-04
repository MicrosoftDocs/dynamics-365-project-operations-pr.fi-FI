---
title: Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa
description: Tässä aiheessa on tietoja siitä, miten hinnoitteludimensioita voidaan käyttää sellaisen resurssin hinnoittelun ja kustannuslaskennan tukemiseen, joka täyttää useita rooleja projektissa.
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
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075400"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="ea57c-103">Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa</span><span class="sxs-lookup"><span data-stu-id="ea57c-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="ea57c-104">Projektipohjaiset yritykset tarvitsevat usein yhden resurssin suorittamaan useita rooleja projektissa.</span><span class="sxs-lookup"><span data-stu-id="ea57c-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="ea57c-105">Kukin näistä rooleista voidaan hinnoitella ja kustannuslaskea eri tavalla, mikä tarkoittaa sitä, että saman resurssin aika projektissa voi saada erilaisen talousarvion kunkin roolin laskutus- ja kustannushinnan mukaan.</span><span class="sxs-lookup"><span data-stu-id="ea57c-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="ea57c-106">Project Service Automation sallii nimetyn resurssin Ryhmän jäsen -tietueen arvojen määrittämisen ja sallii eri korvaamiset kullekin tehtävälle, johon ryhmän jäsen on delegoitu.</span><span class="sxs-lookup"><span data-stu-id="ea57c-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="ea57c-107">Seuraavassa esimerkissä selitetään, miten tämän arvon yksinkertainen korvaaminen mahdollistaa sen, että resurssilla voi olla useita rooleja projektissa, ja kussakin roolissa eri kustannus- ja laskutushinnat.</span><span class="sxs-lookup"><span data-stu-id="ea57c-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="ea57c-108">Tehtävien luominen</span><span class="sxs-lookup"><span data-stu-id="ea57c-108">Create tasks</span></span>
<span data-ttu-id="ea57c-109">Luo kaksi projektitehtävää, jotka ovat 40 tuntia, tehtävä A ja tehtävä B. Valitse tehtävän B edeltäjäksi tehtävä A.</span><span class="sxs-lookup"><span data-stu-id="ea57c-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="ea57c-110">Yleisen projektiryhmän jäsenen roolin ja organisaatioyksikön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ea57c-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="ea57c-111">Valitse **Aikataulu** -sivulla tehtävän A **Tehtävä** -rivi.</span><span class="sxs-lookup"><span data-stu-id="ea57c-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="ea57c-112">Valitse **Resurssit** -kentässä avattavasta luettelosta **Luo**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="ea57c-113">Määritä **Ryhmän jäsenen pikaluonti** -sivulla sen yleisen ryhmän jäsenen määritteet, joka voi suorittaa tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="ea57c-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="ea57c-114">Valitse haluamasi rooli ja organisaatioyksikkö ja valitse sitten **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="ea57c-115">Yleinen ryhmän jäsen luodaan ja delegoidaan tähän tehtävään.</span><span class="sxs-lookup"><span data-stu-id="ea57c-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="ea57c-116">Toista nämä vaiheet tehtävän B kohdalla ja varmista, että tehtävään B luodun yleisen ryhmän jäsenen rooli ja organisaatioyksikkö ovat eri kuin tehtävässä A.</span><span class="sxs-lookup"><span data-stu-id="ea57c-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="ea57c-117">Projektitehtävän roolin ja organisaatioyksikön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ea57c-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="ea57c-118">Kun olet luonut tehtävän A, valitse se ja valitse sitten **Muokkaa tehtävää**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="ea57c-119">Etsi **Tehtävän tiedot** -sivulla **Rooli** - ja **Organisaatioyksikkö** -kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot.</span><span class="sxs-lookup"><span data-stu-id="ea57c-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="ea57c-120">Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Consulting Lead** ja **Fabrikam US** organisaatioyksiköksi.</span><span class="sxs-lookup"><span data-stu-id="ea57c-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="ea57c-121">Valitse tehtävä B ja valitse sitten **Muokkaa tehtävää**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="ea57c-122">Etsi **Tehtävän tiedot** -sivulla **Rooli** - ja **Organisaatioyksikkö** -kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot.</span><span class="sxs-lookup"><span data-stu-id="ea57c-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="ea57c-123">Varmista, että **Rooli** - ja **Organisaatioyksikkö** -kentissä on eri arvot ovat tehtävissä A ja B.</span><span class="sxs-lookup"><span data-stu-id="ea57c-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="ea57c-124">Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Network Technician** ja **Fabrikam US** organisaatioyksiköksi.</span><span class="sxs-lookup"><span data-stu-id="ea57c-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="ea57c-125">Tallenna ja sulje **Tehtävän tiedot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="ea57c-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="ea57c-126">Tiimin jäsenen ja arvioiden käyttäytyminen</span><span class="sxs-lookup"><span data-stu-id="ea57c-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="ea57c-127">Valitse **Tehtävän tiedot** -sivun **Ryhmän jäsen** -kohdassa kaksi yleistä ryhmän jäsentä ja valitse sitten **Luo tarpeet**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="ea57c-128">Tämä luo resurssitarpeet.</span><span class="sxs-lookup"><span data-stu-id="ea57c-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="ea57c-129">Valitse ryhmän jäsenen rivi **Consulting Lead** ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="ea57c-130">Aikataulutaulukko avautuu ja varaa resurssin tälle tarpeelle.</span><span class="sxs-lookup"><span data-stu-id="ea57c-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="ea57c-131">Valitse ryhmän jäsenen rivi **Network Technician** ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="ea57c-132">Aikataulutaulukko avautuu ja varaa saman resurssin kyseiselle tarpeelle.</span><span class="sxs-lookup"><span data-stu-id="ea57c-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="ea57c-133">Ryhmän jäsen -ruudukko</span><span class="sxs-lookup"><span data-stu-id="ea57c-133">Team Member grid</span></span> 
<span data-ttu-id="ea57c-134">Huomaa **Ryhmän jäsen** -ruudukossa, että kaksi yleistä ryhmän jäsenen tietuetta poistetaan ja että ne on korvattu yhdellä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="ea57c-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="ea57c-135">Kyseiselle resurssille on määritetty yksi arvojoukko, joka näyttää **Rooli** - ja **Organisaatioyksikkö** -kenttien oletusarvojoukot.</span><span class="sxs-lookup"><span data-stu-id="ea57c-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="ea57c-136">Kun laajennat kyseisen Ryhmän jäsen -tietueen riviä, näet kummallekin tehtävälle erilliset delegoinnit Ryhmän jäsen -tietueessa.</span><span class="sxs-lookup"><span data-stu-id="ea57c-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="ea57c-137">Kullakin delegointirivillä on tehtäväkohtaiset arvot kentille **Rooli** ja **Organisaatioyksikkö**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="ea57c-138">Arvioruudukko</span><span class="sxs-lookup"><span data-stu-id="ea57c-138">Estimates grid</span></span> 
<span data-ttu-id="ea57c-139">Kun siirryt **Arviot** -ruudukkoon, huomaat, että saman resurssin molemmat delegoinnit hinnoitellaan eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="ea57c-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="ea57c-140">Resurssin delegointi tehtävssä A on hinnoiteltu käyttämällä **Rooli** -määritteen arvoa **Consulting Lead**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="ea57c-141">Saman resurssin delegointi tehtävssä B on hinnoiteltu käyttämällä **Rooli** -määritteen arvoa **Network Technician**.</span><span class="sxs-lookup"><span data-stu-id="ea57c-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





