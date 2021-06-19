---
title: Tarjousrivin laskutettavan osan määrittäminen
description: Tässä ohjeaiheessa on tietoja laskutettavan ja ei-laskutettavan komponentin määrittämisestä projektipohjaisella tarjousrivillä.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003762"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="5697a-103">Tarjousrivin laskutettavan komponentin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5697a-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="5697a-104">_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_</span><span class="sxs-lookup"><span data-stu-id="5697a-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5697a-105">Projektipohjaiseen tarjousrivillä on *sisällytettyjen* osien ja *laskutettavien* osien käsitteet.</span><span class="sxs-lookup"><span data-stu-id="5697a-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="5697a-106">Sisällytettyjä osia voivat olla seuraavat:</span><span class="sxs-lookup"><span data-stu-id="5697a-106">Included components are subject to:</span></span>

  - <span data-ttu-id="5697a-107">Laskutustapa ja asiakasjako</span><span class="sxs-lookup"><span data-stu-id="5697a-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="5697a-108">Ei-ylitettävät rajoitukset</span><span class="sxs-lookup"><span data-stu-id="5697a-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="5697a-109">Projektipohjaisella tarjousrivillä määritetyt laskun toistumisasetukset</span><span class="sxs-lookup"><span data-stu-id="5697a-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="5697a-110">Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **laskutustyyppi**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="5697a-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="5697a-111">**Laskutustyyppi**-kenttä on asetusjoukko, joka sallii seuraavat arvot tarjousrivin kontekstissa:</span><span class="sxs-lookup"><span data-stu-id="5697a-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="5697a-112">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-112">Chargeable</span></span>
  - <span data-ttu-id="5697a-113">Ei veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-113">Non-chargeable</span></span>

<span data-ttu-id="5697a-114">Laskutettavat komponentit voidaan määrittää tehtäville, rooleille ja tapahtumaluokille.</span><span class="sxs-lookup"><span data-stu-id="5697a-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="5697a-115">Maksukyky määritetään tarjousrivin tehtäville, ja se koskee kaikkia siihen riviin sisältyviä tapahtumaluokkia.</span><span class="sxs-lookup"><span data-stu-id="5697a-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="5697a-116">Jos sopimusrivin **Sisällytä tehtävät** -kentän asetus on **Koko projekti** tai se on jätetty tyhjäksi, **Veloitettavat tehtävät** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5697a-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="5697a-117">Laskutettavuus määritetään tarjousrivin rooleissa, ja se koskee vain **Ajan** tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="5697a-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="5697a-118">Jos **Sisällytä aika** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat roolit** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5697a-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="5697a-119">Veloitettavuus määritetään tarjousrivin tapahtumaluokissa ja koskee vain **Kulu**-tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="5697a-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="5697a-120">Jos **Sisällytä kulut** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat luokat** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5697a-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="5697a-121">Projektitehtävän päivittäminen laskutettavaksi tai ei-laskutettavaksi</span><span class="sxs-lookup"><span data-stu-id="5697a-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="5697a-122">Projektitehtävä voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin yhteydessä, mikä mahdollistaa seuraavan asennuksen.</span><span class="sxs-lookup"><span data-stu-id="5697a-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="5697a-123">Jos projektiin perustuva tarjousrivi sisältää **Ajan** ja tehtävän **T1**, tehtävä liitetään tarjousriviin laskutettavana.</span><span class="sxs-lookup"><span data-stu-id="5697a-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="5697a-124">Jos on olemassa toinen tarjousrivi, joka sisältää **Kulut**, voit liittää **T1**-tehtävän tarjousriviin ei-laskutettavana.</span><span class="sxs-lookup"><span data-stu-id="5697a-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="5697a-125">Tuloksena on, että kaikki tehtävään kirjattu aika on laskutettavaa ja kaikki tehtävään kirjatut kulut ovat ei-laskutettavia.</span><span class="sxs-lookup"><span data-stu-id="5697a-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="5697a-126">Tehtävän laskutustyyppi voidaan määrittää projektipohjaisen tarjousrivin **Veloitettavat tehtävät** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Tarjousrivin tehtävät** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="5697a-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="5697a-127">Vaihtoehtoisesti projektitehtävän laskutustyyppi voidaan päivittää sen aliruudukon **Laskutustyyppi**-kentässä, joka on tehtävään liitetyt tarjousrivit näyttävän projektin tehtävän laskutusasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="5697a-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="5697a-128">Roolin päivittäminen laskutettavaksi tai ei-laskutettavaksi</span><span class="sxs-lookup"><span data-stu-id="5697a-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="5697a-129">Rooli voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="5697a-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="5697a-130">Roolin laskutustyyppi voidaan määrittää tarjousrivin **Veloitettavat roolit** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat roolit** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="5697a-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="5697a-131">Päivitä tapahtumaluokka laskutettavaksi tai ei-laskutettavaksi</span><span class="sxs-lookup"><span data-stu-id="5697a-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="5697a-132">Tietyn tarjousrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.</span><span class="sxs-lookup"><span data-stu-id="5697a-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="5697a-133">Tapahtuman laskutustyyppi voidaan määrittää tarjousrivin **Veloitettavat luokat** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat luokat** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="5697a-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="5697a-134">Selvitä verosaatavan syntyminen</span><span class="sxs-lookup"><span data-stu-id="5697a-134">Resolve chargeability</span></span>
<span data-ttu-id="5697a-135">Aikaa varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="5697a-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="5697a-136">**Aika** sisältyy tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="5697a-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="5697a-137">**Rooli** on määritetty laskutettavaksi tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="5697a-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="5697a-138">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="5697a-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="5697a-139">Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään myös laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="5697a-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="5697a-140">Kulua varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="5697a-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="5697a-141">**Kulu** sisältyy tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="5697a-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="5697a-142">**Tapahtumaluokka** on määritetty laskutettavaksi tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="5697a-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="5697a-143">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="5697a-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="5697a-144">Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään myös laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="5697a-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="5697a-145">Materiaalia varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="5697a-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="5697a-146">**Materiaalit** sisältyy tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="5697a-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="5697a-147">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="5697a-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="5697a-148">Jos nämä kaksi asiaa ovat tosia, **Tehtävä** tulisi myös määrittää laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="5697a-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-149">
                    <strong>Sisältää ajan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="5697a-150">
                    <strong>Sisältää kulun</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="5697a-151">
                    <strong>Sisältää materiaalit</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="5697a-152">
                    <strong>Sisällytettävät tehtävät</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-153">
                    <strong>Rooli</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-154">
                    <strong>Luokka</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-155">
                    <strong>Tehtävä</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="5697a-156">
                    <strong>Laskutettavuusvaikutus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-157">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-158">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-159">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-160">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="5697a-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-161">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-162">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-163">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-164">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-165">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-166">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-167">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-168">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-169">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-170">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="5697a-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-171">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-172">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-173">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-174">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-175">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-176">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-177">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-178">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-179">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-180">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="5697a-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-181">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-182">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-183">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-184">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-185">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-186">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-187">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-188">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-189">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-190">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="5697a-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-191">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-192">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-193">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-194">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-195">Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-196">Laskutustyyppi materiaalin toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-197">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-198">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-199">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-200">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="5697a-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-201">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-202">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-203">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-204">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-205">Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-206">Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-207">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-208">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-209">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-210">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="5697a-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-211">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-212">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-213">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-214">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-215">Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-216">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-218">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-220">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="5697a-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-221">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-222">
                    <strong>Veloitettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-223">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-224">Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-225">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-226">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-228">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-229">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-230">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="5697a-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-231">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-232">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-233">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-234">Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-235">Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-236">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-237">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="5697a-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-239">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-240">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="5697a-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-241">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-242">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-243">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-244">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-245">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-246">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-247">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="5697a-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="5697a-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-250">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="5697a-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-251">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-252">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-253">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-254">Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-255">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-256">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-257">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-258">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="5697a-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-260">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="5697a-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-261">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-262">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="5697a-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-263">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-264">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-265">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="5697a-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="5697a-266">Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="5697a-267">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="5697a-268">Kyllä</span><span class="sxs-lookup"><span data-stu-id="5697a-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="5697a-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="5697a-270">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="5697a-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5697a-271">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="5697a-272">
                    <strong>Ei veloitettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5697a-273">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="5697a-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="5697a-274">Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-275">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="5697a-276">Laskutustyyppi materiaalin toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5697a-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
