---
title: Projektipohjaisen sopimusrivin veloitettavien komponenttien määrittäminen
description: Tässä ohjeaiheessa on tietoja laskutettavan osan lisäämisestä projektitoimintojen sopimusriveille.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003717"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="4da3d-103">Projektipohjaisen sopimusrivin veloitettavien komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4da3d-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="4da3d-104">_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_</span><span class="sxs-lookup"><span data-stu-id="4da3d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4da3d-105">Projektipohjaiseen sopimusriviin on *sisällytetty* komponentteja ja *laskutettavia* osia.</span><span class="sxs-lookup"><span data-stu-id="4da3d-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="4da3d-106">Sisältyvät komponentit ovat komponentteja, joihin liittyy:</span><span class="sxs-lookup"><span data-stu-id="4da3d-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="4da3d-107">Laskutustapa ja asiakasjako</span><span class="sxs-lookup"><span data-stu-id="4da3d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="4da3d-108">Ei-ylitettävät rajoitukset</span><span class="sxs-lookup"><span data-stu-id="4da3d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="4da3d-109">Projektipohjaisella sopimusrivillä määritetyt laskun toistumisasetukset</span><span class="sxs-lookup"><span data-stu-id="4da3d-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="4da3d-110">Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **laskutustyyppi**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="4da3d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="4da3d-111">**Laskutustyyppi**-kenttä on asetusjoukko, joka sallii seuraavat arvot sopimusrivin kontekstissa:</span><span class="sxs-lookup"><span data-stu-id="4da3d-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="4da3d-112">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-112">Chargeable</span></span>
  - <span data-ttu-id="4da3d-113">Ei veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-113">Non-chargeable</span></span>

<span data-ttu-id="4da3d-114">Laskutettavat komponentit voidaan määrittää tehtäville, rooleille ja tapahtumaluokille.</span><span class="sxs-lookup"><span data-stu-id="4da3d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="4da3d-115">Maksukyky määritetään projektisopimusrivin tehtäville, ja se koskee kaikkia riviin sisältyviä tapahtumaluokkia.</span><span class="sxs-lookup"><span data-stu-id="4da3d-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="4da3d-116">Jos sopimusrivin **Sisällytä tehtävät** -kenttä on tyhjä tai sen asetus on **Koko projekti**, **Veloitettavat tehtävät** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4da3d-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="4da3d-117">Projektisopimusrivin rooleihin määritetty maksuvalmius koskee vain **ajan** tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="4da3d-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="4da3d-118">Jos sopimusrivin **Sisällytä aika** -kentän sen asetus on **Ei**, **veloitettavat roolit** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4da3d-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="4da3d-119">Projektisopimusrivin tapahtumakategorioihin määritetty maksuvalmius koskee vain **Kulu** tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="4da3d-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="4da3d-120">Jos **Sisällytä kulut** -kentän sen asetus on **Ei**, **Veloitettavat kategoriat** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4da3d-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="4da3d-121">Projektitehtävän päivittäminen laskutettavana tai ei-laskutettavana</span><span class="sxs-lookup"><span data-stu-id="4da3d-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="4da3d-122">Projektitehtävä voi olla laskutettava tai ei-laskutettava tietyllä sopimusrivillä, joten seuraavat asetukset ovat mahdollisia:</span><span class="sxs-lookup"><span data-stu-id="4da3d-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="4da3d-123">Jos projektiin perustuva sopimusrivi sisältää **Aikaa** ja tietyn tehtävän, **T1** liitetään siihen laskutettavana.</span><span class="sxs-lookup"><span data-stu-id="4da3d-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="4da3d-124">Jos on olemassa toinen sopimusrivi, joka sisältää **Kulun**, voit liittää T1-tehtävän sopimusriviin ei-laskutettavana.</span><span class="sxs-lookup"><span data-stu-id="4da3d-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="4da3d-125">Tuloksena on se, että kaikki tehtävään kirjatut ajat ovat veloitettavissa ja kaikki kulut eivät ole laskutettavia.</span><span class="sxs-lookup"><span data-stu-id="4da3d-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="4da3d-126">Tehtävän laskutustyyppi voidaan määrittää sopimusrivin **Veloitettavat tehtävät** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä sopimusrivin tehtävien aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="4da3d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="4da3d-127">Vaihtoehtoisesti **Laskutustyyppi**-kenttä voidaan päivittää sen projektin tehtävän laskutusasetusten aliruudukossa, joka näyttää tehtävään liitetyt sopimusrivit.</span><span class="sxs-lookup"><span data-stu-id="4da3d-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="4da3d-128">Roolin päivittäminen laskutettavana tai ei-laskutettavana</span><span class="sxs-lookup"><span data-stu-id="4da3d-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="4da3d-129">Tietyn sopimusrivin rooli voi olla laskutettava tai ei-laskutettava.</span><span class="sxs-lookup"><span data-stu-id="4da3d-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="4da3d-130">Roolin laskutustyyppi voidaan määrittää sopimusrivin **laskutettavat roolit** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4da3d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="4da3d-131">Se tehdään päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat roolit** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="4da3d-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="4da3d-132">Tapahtumaluokan päivittäminen laskutettavana tai ei-laskutettavana</span><span class="sxs-lookup"><span data-stu-id="4da3d-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="4da3d-133">Tietyn sopimusrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.</span><span class="sxs-lookup"><span data-stu-id="4da3d-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="4da3d-134">Tapahtuman laskutustyyppi voidaan määrittää projektipohjaisen sopimusrivin **laskutettavat luokat** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4da3d-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="4da3d-135">Se tehdään päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat luokat** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="4da3d-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="4da3d-136">Selvitä verosaatavan syntyminen</span><span class="sxs-lookup"><span data-stu-id="4da3d-136">Resolve chargeability</span></span>

<span data-ttu-id="4da3d-137">Aikaa varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="4da3d-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="4da3d-138">**Aika** sisältyy sopimusriviin.</span><span class="sxs-lookup"><span data-stu-id="4da3d-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="4da3d-139">**Rooli** on määritetty laskutettavaksi sopimusrivillä.</span><span class="sxs-lookup"><span data-stu-id="4da3d-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="4da3d-140">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** sopimusrivillä.</span><span class="sxs-lookup"><span data-stu-id="4da3d-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="4da3d-141">Jos nämä kolme asiaa ovat tosia, tehtävä määritetään laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="4da3d-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="4da3d-142">Kulua varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="4da3d-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="4da3d-143">**Kulu** sisältyy sopimusriviin</span><span class="sxs-lookup"><span data-stu-id="4da3d-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="4da3d-144">**Tapahtumaluokka** on määritetty laskutettavaksi sopimusrivillä</span><span class="sxs-lookup"><span data-stu-id="4da3d-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="4da3d-145">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** sopimusrivillä</span><span class="sxs-lookup"><span data-stu-id="4da3d-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="4da3d-146">Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="4da3d-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="4da3d-147">Materiaaleja varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="4da3d-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="4da3d-148">**Materiaalit** sisältyy sopimusriviin</span><span class="sxs-lookup"><span data-stu-id="4da3d-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="4da3d-149">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** sopimusrivillä</span><span class="sxs-lookup"><span data-stu-id="4da3d-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="4da3d-150">Jos nämä kaksi asiaa ovat tosia, **Tehtävä** määritetään laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="4da3d-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-151">
                    <strong>Sisältää ajan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4da3d-152">
                    <strong>Sisältää kulun</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4da3d-153">
                    <strong>Sisältää materiaalit</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="4da3d-154">
                    <strong>Sisällytettävät tehtävät</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-155">
                    <strong>Rooli</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-156">
                    <strong>Luokka</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-157">
                    <strong>Tehtävä</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="4da3d-158">
                    <strong>Laskutettavuusvaikutus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-159">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-160">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-161">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-162">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="4da3d-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-163">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-164">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-165">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-166">Laskutus ajan toteutuneella arvolla: <strong>Laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-167">Laskutustyyppi kulun toteutuneella arvolla: <strong>Laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-168">Laskutustyyppi materiaalin toteutuneella arvolla: <strong>Laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-169">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-170">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-171">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-172">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="4da3d-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-173">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-174">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-175">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-176">Laskutus ajan toteutuneella arvolla: <strong>Laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-177">Laskutustyyppi kulun toteutuneella arvolla: <strong>Laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-178">Laskutustyyppi materiaalin toteutuneella arvolla: <strong>Laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-179">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-180">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-181">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-182">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="4da3d-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-183">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-184">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-185">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-186">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-187">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4da3d-188">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-189">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-190">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-191">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-192">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="4da3d-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-193">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-194">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-195">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-196">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-197">Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-198">Laskutustyyppi materiaalin toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-199">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-200">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-201">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-202">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="4da3d-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-203">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-204">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-205">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-206">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-207">Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-208">Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-209">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-210">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-211">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-212">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="4da3d-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-213">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-214">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-215">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-216">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-217">Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-218">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-220">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-221">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-222">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="4da3d-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-223">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-224">
                    <strong>Veloitettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-225">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-226">Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-227">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4da3d-228">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-230">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-231">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-232">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="4da3d-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-233">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-234">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-235">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-236">Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-237">Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-238">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-239">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4da3d-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-241">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-242">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="4da3d-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-243">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-244">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-245">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-246">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4da3d-247">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-248">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4da3d-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4da3d-251">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-252">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="4da3d-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-253">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-254">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-255">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-256">Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-257">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-258">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-259">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-260">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4da3d-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-262">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="4da3d-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-263">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-264">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-265">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-266">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4da3d-267">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="4da3d-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4da3d-268">Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4da3d-269">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4da3d-270">Kyllä</span><span class="sxs-lookup"><span data-stu-id="4da3d-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4da3d-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4da3d-272">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="4da3d-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4da3d-273">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4da3d-274">
                    <strong>Ei veloitettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4da3d-275">Ei voida määrittää</span><span class="sxs-lookup"><span data-stu-id="4da3d-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4da3d-276">Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-277">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4da3d-278">Laskutustyyppi materiaalin toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4da3d-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
