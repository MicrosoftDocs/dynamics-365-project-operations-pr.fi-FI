---
title: Todelliset arvot
description: Tässä aiheessa on tietoja projektin todellisista arvoista.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751237"
---
# <a name="actuals"></a><span data-ttu-id="f5a5c-103">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="f5a5c-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f5a5c-104">Todelliset arvot vastaavat työmäärää, joka projektissa on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="f5a5c-105">Projektin todelliset arvot voidaan jäljittää lähdeasiakirjoihinsa.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="f5a5c-106">Lähdeasiakirjoja ovat aika, kulu, kirjauskansioviennit ja myös laskut.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Projektin todellisten arvojen jäljittäminen lähdeasiakirjoihin](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="f5a5c-108">Aikamerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-108">Submitting a time entry</span></span>

<span data-ttu-id="f5a5c-109">Kun PSA:ssa lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f5a5c-110">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f5a5c-111">Kun lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="f5a5c-112">Oletushintojen antamisen logiikka on kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="f5a5c-113">Kaikkien aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="f5a5c-114">Nämä kentät sisältävät tapahtuman päiväyksen, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="f5a5c-115">Oletushintoihin vaikuttavat kentät, kuten **Rooli** ja **Organisaatioyksiköt** varmistavat, että kirjauskansion riville täytetään oletusarvoisesti asianmukainen hinta.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="f5a5c-116">Jos lisäät aikamerkintään muokatun kentän ja haluat, että kentän arvo välitetään todellisiin arvoihin, luo kenttä Todelliset arvot -entiteettiin ja käytä kenttien yhdistämistä kopioidaksesi kentän aikamerkinnästä todelliseen arvoon.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="f5a5c-117">Kulumerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-117">Submitting an expense entry</span></span>

<span data-ttu-id="f5a5c-118">Kun PSA:ssa lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f5a5c-119">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f5a5c-120">Kun lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="f5a5c-121">Kulujen oletushintojen antamisen logiikka perustuu kululuokkaan, joka valitaan **Kulumerkintä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="f5a5c-122">Oikean hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f5a5c-123">Itse hinnan osalta käyttäjän antama summa asetetaan oletusarvoisesti suoraan siihen liittyvien kulujen kirjauskansion kustannus- ja myyntirivien arvoksi.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="f5a5c-124">Nykyisessä PSA:n versiossa, luokkaperusteista merkintää yksikkökohtaisista kulumerkintöjen oletushinnoista ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="f5a5c-125">Kirjauskansioiden käyttö kustannusten tallentamiseen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-125">Using journals to record costs</span></span>

<span data-ttu-id="f5a5c-126">PSA:ssa voit tallentaa kustannuksia tai tuottoja luokkiin materiaali, maksu, kulu ja verotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f5a5c-127">Kirjauskansiossa on otsikko, rivejä ja **Vahvista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="f5a5c-128">Seuraavassa on skenaarioita, joissa saatetaan käyttää kirjauskansiota:</span><span class="sxs-lookup"><span data-stu-id="f5a5c-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="f5a5c-129">Sinun on tallennettava projektin materiaalien todellisia kustannuksia ja myyntejä.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="f5a5c-130">Sinun on siirrettävä tapahtumien todellisia arvoja toisesta järjestelmästä PSA:han.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="f5a5c-131">Sinun on tallennettava toisessa järjestelmässä aiheutuneita kustannuksia, kuten hankinta- tai alihankintakustannuksia.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="f5a5c-132">Todellisten arvojen tallentaminen projektitapahtumien perusteella</span><span class="sxs-lookup"><span data-stu-id="f5a5c-132">Recording actuals based on project events</span></span>

<span data-ttu-id="f5a5c-133">PSA tallentaa projektin aikana esiintyvät taloudelliset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f5a5c-134">Nämä tapahtumat kirjataan muodossa **Todelliset arvot**.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="f5a5c-135">Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="f5a5c-136">**Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö**</span><span class="sxs-lookup"><span data-stu-id="f5a5c-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f5a5c-137">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="f5a5c-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f5a5c-138">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f5a5c-139">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="f5a5c-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f5a5c-140">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f5a5c-141">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="f5a5c-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f5a5c-142">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f5a5c-143">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="f5a5c-143">Actuals</span></span></th>
<th><span data-ttu-id="f5a5c-144">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-144">Transaction currency</span></span></th>
<th><span data-ttu-id="f5a5c-145">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-145">Fixed price</span></span></th>
<th><span data-ttu-id="f5a5c-146">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f5a5c-147">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f5a5c-148">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-149">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f5a5c-150">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5a5c-151">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5a5c-152">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-152">Cost actual</span></span></td>
<td><span data-ttu-id="f5a5c-153">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-154">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-155">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f5a5c-156">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-157">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-158">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="f5a5c-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f5a5c-159">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5a5c-160">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5a5c-161">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-161">Cost actual</span></span></td>
<td><span data-ttu-id="f5a5c-162">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-163">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-164">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-165">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-166">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-167">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="f5a5c-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5a5c-168">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-169">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5a5c-170">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5a5c-171">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5a5c-172">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5a5c-173">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-174">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-175">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-176">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-177">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-178">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-178">Billed sales</span></span></td>
<td><span data-ttu-id="f5a5c-179">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5a5c-180">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5a5c-181">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5a5c-182">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-183">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-184">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-185">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-187">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="f5a5c-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5a5c-188">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-189">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5a5c-190">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5a5c-191">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5a5c-192">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5a5c-193">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f5a5c-194">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f5a5c-195">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="f5a5c-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f5a5c-196">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-197">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-198">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-199">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-199">Billed sales</span></span></td>
<td><span data-ttu-id="f5a5c-200">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5a5c-201">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5a5c-202">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5a5c-203">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-204">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f5a5c-205">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-206">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="f5a5c-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5a5c-207">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f5a5c-208">**Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön**</span><span class="sxs-lookup"><span data-stu-id="f5a5c-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f5a5c-209">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="f5a5c-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f5a5c-210">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f5a5c-211">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="f5a5c-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f5a5c-212">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f5a5c-213">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="f5a5c-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f5a5c-214">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f5a5c-215">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="f5a5c-215">Actuals</span></span></th>
<th><span data-ttu-id="f5a5c-216">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-216">Transaction currency</span></span></th>
<th><span data-ttu-id="f5a5c-217">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-217">Fixed price</span></span></th>
<th><span data-ttu-id="f5a5c-218">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f5a5c-219">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f5a5c-220">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-221">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f5a5c-222">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f5a5c-223">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5a5c-224">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-224">Cost actual</span></span></td>
<td><span data-ttu-id="f5a5c-225">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f5a5c-226">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f5a5c-227">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f5a5c-228">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f5a5c-229">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-230">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="f5a5c-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f5a5c-231">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-232">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f5a5c-233">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-234">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f5a5c-235">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f5a5c-236">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5a5c-237">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-237">Cost actual</span></span></td>
<td><span data-ttu-id="f5a5c-238">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-239">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-240">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-241">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-242">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="f5a5c-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-243">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f5a5c-244">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-245">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f5a5c-246">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-247">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="f5a5c-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5a5c-248">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-249">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5a5c-250">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5a5c-251">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5a5c-252">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5a5c-253">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-254">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-255">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-256">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f5a5c-257">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-258">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-258">Billed sales</span></span></td>
<td><span data-ttu-id="f5a5c-259">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5a5c-260">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5a5c-261">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5a5c-262">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-263">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-264">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-265">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5a5c-266">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-267">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="f5a5c-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5a5c-268">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-269">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5a5c-270">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5a5c-271">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5a5c-272">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5a5c-273">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f5a5c-274">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f5a5c-275">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="f5a5c-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f5a5c-276">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-277">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f5a5c-278">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="f5a5c-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-279">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-279">Billed sales</span></span></td>
<td><span data-ttu-id="f5a5c-280">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5a5c-281">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5a5c-282">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="f5a5c-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5a5c-283">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-284">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="f5a5c-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f5a5c-285">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5a5c-286">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="f5a5c-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5a5c-287">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="f5a5c-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
