---
title: Tarjousrivin laskutettavan osan määrittäminen
description: Tässä ohjeaiheessa on tietoja laskutettavan ja ei-laskutettavan komponentin määrittämisestä projektipohjaisella tarjousrivillä.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858289"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="21090-103">Tarjousrivin laskutettavan komponentin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21090-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="21090-104">_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_</span><span class="sxs-lookup"><span data-stu-id="21090-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="21090-105">Projektipohjaiseen tarjousrivillä on *sisällytettyjen* osien ja *laskutettavien* osien käsitteet.</span><span class="sxs-lookup"><span data-stu-id="21090-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="21090-106">Sisällytettyjä osia voivat olla seuraavat:</span><span class="sxs-lookup"><span data-stu-id="21090-106">Included components are subject to:</span></span>

  - <span data-ttu-id="21090-107">Laskutustapa ja asiakasjako</span><span class="sxs-lookup"><span data-stu-id="21090-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="21090-108">Ei-ylitettävät rajoitukset</span><span class="sxs-lookup"><span data-stu-id="21090-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="21090-109">Projektipohjaisella tarjousrivillä määritetyt laskun toistumisasetukset</span><span class="sxs-lookup"><span data-stu-id="21090-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="21090-110">Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **laskutustyyppi**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="21090-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="21090-111">**Laskutustyyppi**-kenttä on asetusjoukko, joka sallii seuraavat arvot tarjousrivin kontekstissa:</span><span class="sxs-lookup"><span data-stu-id="21090-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="21090-112">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-112">Chargeable</span></span>
  - <span data-ttu-id="21090-113">Ei veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-113">Non-chargeable</span></span>

<span data-ttu-id="21090-114">Laskutettavat komponentit voidaan määrittää tehtäville, rooleille ja tapahtumaluokille.</span><span class="sxs-lookup"><span data-stu-id="21090-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="21090-115">Maksukyky määritetään tarjousrivin tehtäville, ja se koskee kaikkia siihen riviin sisältyviä tapahtumaluokkia.</span><span class="sxs-lookup"><span data-stu-id="21090-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="21090-116">Jos sopimusrivin **Sisällytä tehtävät** -kentän asetus on **Koko projekti** tai se on jätetty tyhjäksi, **Veloitettavat tehtävät** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="21090-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="21090-117">Laskutettavuus määritetään tarjousrivin rooleissa, ja se koskee vain **Ajan** tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="21090-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="21090-118">Jos **Sisällytä aika** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat roolit** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="21090-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="21090-119">Veloitettavuus määritetään tarjousrivin tapahtumaluokissa ja koskee vain **Kulu**-tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="21090-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="21090-120">Jos **Sisällytä kulut** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat luokat** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="21090-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="21090-121">Projektitehtävän päivittäminen laskutettavaksi tai ei-laskutettavaksi</span><span class="sxs-lookup"><span data-stu-id="21090-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="21090-122">Projektitehtävä voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin yhteydessä, mikä mahdollistaa seuraavan asennuksen.</span><span class="sxs-lookup"><span data-stu-id="21090-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="21090-123">Jos projektiin perustuva tarjousrivi sisältää **Ajan** ja tehtävän **T1**, tehtävä liitetään tarjousriviin laskutettavana.</span><span class="sxs-lookup"><span data-stu-id="21090-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="21090-124">Jos on olemassa toinen tarjousrivi, joka sisältää **Kulut**, voit liittää **T1**-tehtävän tarjousriviin ei-laskutettavana.</span><span class="sxs-lookup"><span data-stu-id="21090-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="21090-125">Tuloksena on, että kaikki tehtävään kirjattu aika on laskutettavaa ja kaikki tehtävään kirjatut kulut ovat ei-laskutettavia.</span><span class="sxs-lookup"><span data-stu-id="21090-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="21090-126">Tehtävän laskutustyyppi voidaan määrittää projektipohjaisen tarjousrivin **Veloitettavat tehtävät** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Tarjousrivin tehtävät** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="21090-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="21090-127">Vaihtoehtoisesti projektitehtävän laskutustyyppi voidaan päivittää sen aliruudukon **Laskutustyyppi**-kentässä, joka on tehtävään liitetyt tarjousrivit näyttävän projektin tehtävän laskutusasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="21090-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="21090-128">Roolin päivittäminen laskutettavaksi tai ei-laskutettavaksi</span><span class="sxs-lookup"><span data-stu-id="21090-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="21090-129">Rooli voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="21090-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="21090-130">Roolin laskutustyyppi voidaan määrittää tarjousrivin **Veloitettavat roolit** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat roolit** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="21090-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="21090-131">Päivitä tapahtumaluokka laskutettavaksi tai ei-laskutettavaksi</span><span class="sxs-lookup"><span data-stu-id="21090-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="21090-132">Tietyn tarjousrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.</span><span class="sxs-lookup"><span data-stu-id="21090-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="21090-133">Tapahtuman laskutustyyppi voidaan määrittää tarjousrivin **Veloitettavat luokat** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat luokat** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="21090-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="21090-134">Selvitä verosaatavan syntyminen</span><span class="sxs-lookup"><span data-stu-id="21090-134">Resolve chargeability</span></span>
<span data-ttu-id="21090-135">Aikaa varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="21090-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="21090-136">**Aika** sisältyy tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="21090-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="21090-137">**Rooli** on määritetty laskutettavaksi tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="21090-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="21090-138">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="21090-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="21090-139">Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään myös laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="21090-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="21090-140">Kulua varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="21090-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="21090-141">**Kulu** sisältyy tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="21090-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="21090-142">**Tapahtumaluokka** on määritetty laskutettavaksi tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="21090-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="21090-143">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="21090-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="21090-144">Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään myös laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="21090-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="21090-145">Materiaalia varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:</span><span class="sxs-lookup"><span data-stu-id="21090-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="21090-146">**Materiaalit** sisältyy tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="21090-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="21090-147">**Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="21090-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="21090-148">Jos nämä kaksi asiaa ovat tosia, **Tehtävä** tulisi myös määrittää laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="21090-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-149">
                    <strong>Sisältää ajan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="21090-150">
                    <strong>Sisältää kulun</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="21090-151">
                    <strong>Sisältää materiaalit</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="21090-152">
                    <strong>Sisällytettävät tehtävät</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-153">
                    <strong>Rooli</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-154">
                    <strong>Luokka</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-155">
                    <strong>Tehtävä</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="21090-156">
                    <strong>Laskutettavuusvaikutus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-157">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-158">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-159">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-160">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="21090-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-161">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-162">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-163">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-164">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-165">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-166">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-167">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-168">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-169">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-170">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="21090-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-171">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-172">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-173">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-174">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-175">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-176">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-177">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-178">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-179">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-180">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="21090-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-181">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-182">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-183">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-184">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-185">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-186">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-187">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-188">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-189">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-190">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="21090-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-191">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-192">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-193">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-194">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-195">Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-196">Laskutustyyppi materiaalin toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-197">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-198">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-199">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-200">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="21090-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-201">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-202">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-203">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-204">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-205">Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-206">Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-207">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-208">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-209">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-210">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="21090-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-211">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-212">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-213">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-214">Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-215">Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-216">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-218">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-220">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="21090-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-221">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-222">
                    <strong>Veloitettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-223">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-224">Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-225">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-226">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-228">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-229">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-230">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="21090-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-231">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-232">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-233">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-234">Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-235">Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-236">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-237">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="21090-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-239">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-240">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="21090-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-241">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-242">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-243">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-244">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-245">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-246">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-247">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="21090-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="21090-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-250">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="21090-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-251">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-252">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-253">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-254">Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-255">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-256">Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-257">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-258">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="21090-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-260">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="21090-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-261">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-262">Veloitettava</span><span class="sxs-lookup"><span data-stu-id="21090-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-263">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-264">Laskutus toteutuneesta ajasta: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-265">Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava</span><span class="sxs-lookup"><span data-stu-id="21090-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="21090-266">Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="21090-267">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="21090-268">Kyllä</span><span class="sxs-lookup"><span data-stu-id="21090-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="21090-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="21090-270">Koko projekti</span><span class="sxs-lookup"><span data-stu-id="21090-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="21090-271">
                    <strong>Ei-laskutettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="21090-272">
                    <strong>Ei veloitettava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="21090-273">Ei voi määrittää</span><span class="sxs-lookup"><span data-stu-id="21090-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="21090-274">Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-275">Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei-laskutettava </strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="21090-276">Laskutustyyppi materiaalin toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21090-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
