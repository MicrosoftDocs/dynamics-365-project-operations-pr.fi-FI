---
title: suojausmalli
description: Tässä aiheessa on tietoja suojausmallista Dynamics 365 Project Operationsissa.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951205"
---
# <a name="security-model"></a><span data-ttu-id="9528a-103">Suojausmalli</span><span class="sxs-lookup"><span data-stu-id="9528a-103">Security Model</span></span>

<span data-ttu-id="9528a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="9528a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9528a-105">Microsoft Dynamics 365 Project Operations sisältää yksilöllisen suojausmallin, joka mahdollistaa roolipohjaisen liiketoiminnan suojausmallin, joka toimii yhteistyössä Microsoft Office -ryhmien kanssa.</span><span class="sxs-lookup"><span data-stu-id="9528a-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="9528a-106">Käyttöoikeusroolit</span><span class="sxs-lookup"><span data-stu-id="9528a-106">Security roles</span></span>
<span data-ttu-id="9528a-107">Project Operationsin edustatoiminnot sisältävät seuraavat roolit:</span><span class="sxs-lookup"><span data-stu-id="9528a-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="9528a-108">Rooli</span><span class="sxs-lookup"><span data-stu-id="9528a-108">Role</span></span>                          | <span data-ttu-id="9528a-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="9528a-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="9528a-110">Laajuus</span><span class="sxs-lookup"><span data-stu-id="9528a-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="9528a-111">Toiminnon johtaja</span><span class="sxs-lookup"><span data-stu-id="9528a-111">Practice manager</span></span>              | <span data-ttu-id="9528a-112">Tukee projektien välisiä raportteja.</span><span class="sxs-lookup"><span data-stu-id="9528a-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="9528a-113">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-113">Business unit</span></span>              |
| <span data-ttu-id="9528a-114">Projektin hyväksyjä</span><span class="sxs-lookup"><span data-stu-id="9528a-114">Project approver</span></span>              | <span data-ttu-id="9528a-115">Hyväksyy ajan ja kulut projektissa.</span><span class="sxs-lookup"><span data-stu-id="9528a-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="9528a-116">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-116">Business unit</span></span> |
| <span data-ttu-id="9528a-117">Projektiaskutuksen järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="9528a-117">Project billing administrator</span></span> | <span data-ttu-id="9528a-118">Luo laskuehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="9528a-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="9528a-119">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-119">Business unit</span></span> |
| <span data-ttu-id="9528a-120">Projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-120">Project manager</span></span>               | <span data-ttu-id="9528a-121">Luo projektisuunnitelman ja pyytää resursseja.</span><span class="sxs-lookup"><span data-stu-id="9528a-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="9528a-122">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-122">Business unit</span></span> |
| <span data-ttu-id="9528a-123">Projektiresurssi</span><span class="sxs-lookup"><span data-stu-id="9528a-123">Project resource</span></span>              | <span data-ttu-id="9528a-124">Ryhmän jäsenet, jotka voidaan varata ja jotka voivat raportoida aikaa.</span><span class="sxs-lookup"><span data-stu-id="9528a-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="9528a-125">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-125">Business unit</span></span>|
| <span data-ttu-id="9528a-126">Reusrssipäällikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-126">Resource manager</span></span>              | <span data-ttu-id="9528a-127">Kaikki resurssienhallintatoiminnot, kuten resurssipyyntöjen ja varauksien toteuttaminen, erotetaan toisistaan tukemaan hybridiä projektipäällikkö + resurssipäällikkö -kokoonpanoa ja keskitettyä resurssipäällikkö -roolia.</span><span class="sxs-lookup"><span data-stu-id="9528a-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="9528a-128">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-128">Business unit</span></span> |


<span data-ttu-id="9528a-129">Microsoft Project -verkkoversio sisältää seuraavat roolit:</span><span class="sxs-lookup"><span data-stu-id="9528a-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="9528a-130">Rooli</span><span class="sxs-lookup"><span data-stu-id="9528a-130">Role</span></span>           | <span data-ttu-id="9528a-131">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="9528a-131">Description</span></span>                                                                                                        | <span data-ttu-id="9528a-132">Laajuus</span><span class="sxs-lookup"><span data-stu-id="9528a-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="9528a-133">Projektikäyttäjä</span><span class="sxs-lookup"><span data-stu-id="9528a-133">Project user</span></span>   | <span data-ttu-id="9528a-134">Projektin yhteistyökäyttäjä, joka voi luoda omia projektejaan ja tarkastella projekteja, jotka on jaettu hänen kanssaan.</span><span class="sxs-lookup"><span data-stu-id="9528a-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="9528a-135">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="9528a-135">User</span></span>   |
| <span data-ttu-id="9528a-136">Projektijärjestelmä</span><span class="sxs-lookup"><span data-stu-id="9528a-136">Project system</span></span> | <span data-ttu-id="9528a-137">Sovelluskontekstissa käytettävä rooli.</span><span class="sxs-lookup"><span data-stu-id="9528a-137">Role used for application   context.</span></span> <span data-ttu-id="9528a-138">Asiakkaat eivät saa käyttää tätä järjestelmäroolia.</span><span class="sxs-lookup"><span data-stu-id="9528a-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="9528a-139">Yleiset</span><span class="sxs-lookup"><span data-stu-id="9528a-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="9528a-140">Suojauksen pakotus</span><span class="sxs-lookup"><span data-stu-id="9528a-140">Security enforcement</span></span>
<span data-ttu-id="9528a-141">Projektitasolla suoritettavat toiminnot suoritetaan kirjautuneen käyttäjän kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="9528a-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="9528a-142">Tämä tarkoittaa sitä, että jos haluat luoda, avata tai poistaa projektin, käyttäjällä on oltava käyttöoikeus CDS:ssä.</span><span class="sxs-lookup"><span data-stu-id="9528a-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="9528a-143">CDS-käyttöoikeus voidaan myöntää millä tahansa ympäristöön sisältyvillä mahdollisilla mekanismeilla.</span><span class="sxs-lookup"><span data-stu-id="9528a-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="9528a-144">Esimerkiksi, käyttäjä, jolla on suurempi vaikutusalue, voi käyttää projektia tai myös siinä tapauksessa, että on suoritettu erillinen projektin jakotoiminto, joka myöntää käyttöoikeudet käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="9528a-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="9528a-145">On tärkeää huomioida tämä, kun projekteja luodaan Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="9528a-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="9528a-146">Moderni ryhmän yhteistyö Project Operationsissa</span><span class="sxs-lookup"><span data-stu-id="9528a-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="9528a-147">Project-verkkoversio ja Project Operations tukevat moderneja yhteistyöryhmiä.</span><span class="sxs-lookup"><span data-stu-id="9528a-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="9528a-148">Käyttäjät, jotka on lisätty projektiin ryhmän kautta, voivat muokata projektisuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="9528a-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="9528a-149">Project-verkkoversio lisää käyttäjät ryhmään automaattisesti delegoinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="9528a-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="9528a-150">Ryhmät sallivat projektin käyttöoikeudet ja tukevat yhteistyöartefaktien käsittelyä yhteistyönä.</span><span class="sxs-lookup"><span data-stu-id="9528a-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="9528a-151">Seuraavassa kaaviossa on kuvattu ryhmän delegointiprosessin aikana tapahtuvat tapahtumat ja tilan muutokset.</span><span class="sxs-lookup"><span data-stu-id="9528a-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="9528a-152">Project Operations ei luo ryhmää implisiittisen toiminnon kautta, vaan se tapahtuu vain, jos painat Ryhmät-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="9528a-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="9528a-153">Ryhmän jäsenen haku **Ryhmän hallinta** -valintaikkunassa rajoittuu niihin, jotka on määritetty osana ympäristön suojausryhmää.</span><span class="sxs-lookup"><span data-stu-id="9528a-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="9528a-154">Lisätietoja: [Ympäristön käyttöoikeuksien hallinta: käyttöoikeusroolit ja käyttöoikeudet](/power-platform/admin/control-user-access).</span><span class="sxs-lookup"><span data-stu-id="9528a-154">For more information, see [Control user access to environments: security groups and licenses](/power-platform/admin/control-user-access).</span></span>

![Ryhmätila](./media/groupsmode.png)

1. <span data-ttu-id="9528a-156">Projekti luodaan ja sen omistaa projektin luonut käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="9528a-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="9528a-157">Projektin omistaja päivitetään ryhmään.</span><span class="sxs-lookup"><span data-stu-id="9528a-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="9528a-158">Omistajaryhmä on yhdistetty määritettyyn tai luotuun Office-ryhmään.</span><span class="sxs-lookup"><span data-stu-id="9528a-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="9528a-159">Projektin alkuperäinen omistaja on lisätty Office-ryhmään.</span><span class="sxs-lookup"><span data-stu-id="9528a-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="9528a-160">Käyttöönottosuositukset</span><span class="sxs-lookup"><span data-stu-id="9528a-160">Deployment recommendation</span></span>
<span data-ttu-id="9528a-161">Kun Office-ryhmän yhteiskäyttömalli kehittyy, toiminnallisuutta lisätään, jotta aikaa voidaan hallita tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="9528a-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="9528a-162">Asiakkaita, jotka ottavat tänään käyttöön Project Operationsin, kehotetaan käyttämään perinteistä Microsoft Dynamics 365 -suojausmallia.</span><span class="sxs-lookup"><span data-stu-id="9528a-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="9528a-163">Lisätietoja: [Common Data Servicen suojaus](/power-platform/admin/wp-security).</span><span class="sxs-lookup"><span data-stu-id="9528a-163">For more information, see [Security in Common Data Service](/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="9528a-164">Project Operationsin ja Microsoft Dynamics 365 Financen suojaus</span><span class="sxs-lookup"><span data-stu-id="9528a-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="9528a-165">Project Operations sisältää seuraavat roolit:</span><span class="sxs-lookup"><span data-stu-id="9528a-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="9528a-166">Projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="9528a-166">Project manager</span></span>
- <span data-ttu-id="9528a-167">Projektin kirjanpitäjä</span><span class="sxs-lookup"><span data-stu-id="9528a-167">Project accountant</span></span>

<span data-ttu-id="9528a-168">Lisätietoja Financen suojauksesta on aiheessa [Roolipohjainen suojaus](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span><span class="sxs-lookup"><span data-stu-id="9528a-168">For more information about security in Finance, see [Role-based security](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]