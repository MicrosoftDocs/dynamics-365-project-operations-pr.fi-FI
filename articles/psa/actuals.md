---
title: Toteutuneiden yleiskatsaus
description: Tässä aiheessa on tietoja projektin todellisista arvoista.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129764"
---
# <a name="actuals-overview"></a><span data-ttu-id="33539-103">Toteutuneiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="33539-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="33539-104">Todelliset arvot vastaavat työmäärää, joka projektissa on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="33539-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="33539-105">Projektin todelliset arvot voidaan jäljittää lähdeasiakirjoihinsa.</span><span class="sxs-lookup"><span data-stu-id="33539-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="33539-106">Lähdeasiakirjoja ovat aika, kulu, kirjauskansioviennit ja myös laskut.</span><span class="sxs-lookup"><span data-stu-id="33539-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Projektin todellisten arvojen jäljittäminen lähdeasiakirjoihin](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="33539-108">Aikamerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="33539-108">Submitting a time entry</span></span>

<span data-ttu-id="33539-109">Kun PSA:ssa lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="33539-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="33539-110">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="33539-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="33539-111">Kun lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="33539-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="33539-112">Oletushintojen antamisen logiikka on kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="33539-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="33539-113">Kaikkien aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="33539-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="33539-114">Nämä kentät sisältävät tapahtuman päiväyksen, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="33539-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="33539-115">Oletushintoihin vaikuttavat kentät, kuten **Rooli** ja **Organisaatioyksiköt** varmistavat, että kirjauskansion riville täytetään oletusarvoisesti asianmukainen hinta.</span><span class="sxs-lookup"><span data-stu-id="33539-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="33539-116">Jos lisäät aikamerkintään muokatun kentän ja haluat, että kentän arvo välitetään todellisiin arvoihin, luo kenttä Todelliset arvot -entiteettiin ja käytä kenttien yhdistämistä kopioidaksesi kentän aikamerkinnästä todelliseen arvoon.</span><span class="sxs-lookup"><span data-stu-id="33539-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="33539-117">Kulumerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="33539-117">Submitting an expense entry</span></span>

<span data-ttu-id="33539-118">Kun PSA:ssa lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="33539-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="33539-119">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="33539-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="33539-120">Kun lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="33539-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="33539-121">Kulujen oletushintojen antamisen logiikka perustuu kululuokkaan, joka valitaan **Kulumerkintä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="33539-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="33539-122">Oikean hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="33539-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="33539-123">Itse hinnan osalta käyttäjän antama summa asetetaan oletusarvoisesti suoraan siihen liittyvien kulujen kirjauskansion kustannus- ja myyntirivien arvoksi.</span><span class="sxs-lookup"><span data-stu-id="33539-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="33539-124">Nykyisessä PSA:n versiossa, luokkaperusteista merkintää yksikkökohtaisista kulumerkintöjen oletushinnoista ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="33539-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="33539-125">Kirjauskansioiden käyttö kustannusten tallentamiseen</span><span class="sxs-lookup"><span data-stu-id="33539-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="33539-126">PSA:ssa kirjauskansioihin voi tallentaa kustannuksia tai tuottoja materiaali-, maksu-, aika-, kulu- ja verotapahtumaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="33539-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="33539-127">Kirjauskansiossa on otsikko, rivejä ja **Vahvista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="33539-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="33539-128">Seuraavassa on skenaarioita, joissa saatetaan käyttää kirjauskansiota:</span><span class="sxs-lookup"><span data-stu-id="33539-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="33539-129">Sinun on tallennettava projektin materiaalien todellisia kustannuksia ja myyntejä.</span><span class="sxs-lookup"><span data-stu-id="33539-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="33539-130">Sinun on siirrettävä tapahtumien todellisia arvoja toisesta järjestelmästä PSA:han.</span><span class="sxs-lookup"><span data-stu-id="33539-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="33539-131">Sinun on tallennettava toisessa järjestelmässä aiheutuneita kustannuksia, kuten hankinta- tai alihankintakustannuksia.</span><span class="sxs-lookup"><span data-stu-id="33539-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33539-132">Toteutuneiden luonti kirjauskansioiden avulla sopii vain sellaiselle käyttäjälle, joka on täysin tietoinen siitä, mikä kirjanpitovaikutus toteutuneilla on projektiin.</span><span class="sxs-lookup"><span data-stu-id="33539-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="33539-133">Syynä on se, että sovellus ei tarkista kirjauskansion rivityyppiä tai kirjauskansion rivillä annettua liittyvää hinnoittelua.</span><span class="sxs-lookup"><span data-stu-id="33539-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="33539-134">Tämän kirjauskansiotyypin vaikutuksen vuoksi onkin harkittava riittävän tarkasti, kenelle tämän kirjauskansion luontioikeus annetaan.</span><span class="sxs-lookup"><span data-stu-id="33539-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="33539-135">Todellisten arvojen tallentaminen projektitapahtumien perusteella</span><span class="sxs-lookup"><span data-stu-id="33539-135">Recording actuals based on project events</span></span>

<span data-ttu-id="33539-136">PSA tallentaa projektin aikana esiintyvät taloudelliset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="33539-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="33539-137">Nämä tapahtumat kirjataan muodossa **Todelliset arvot**.</span><span class="sxs-lookup"><span data-stu-id="33539-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="33539-138">Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.</span><span class="sxs-lookup"><span data-stu-id="33539-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="33539-139">**Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö**</span><span class="sxs-lookup"><span data-stu-id="33539-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="33539-140">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="33539-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="33539-141">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="33539-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="33539-142">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="33539-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="33539-143">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="33539-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="33539-144">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="33539-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="33539-145">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="33539-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="33539-146">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="33539-146">Actuals</span></span></th>
<th><span data-ttu-id="33539-147">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="33539-147">Transaction currency</span></span></th>
<th><span data-ttu-id="33539-148">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="33539-148">Fixed price</span></span></th>
<th><span data-ttu-id="33539-149">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="33539-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33539-150">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="33539-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="33539-151">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="33539-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-152">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="33539-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="33539-153">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="33539-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33539-154">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="33539-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33539-155">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-155">Cost actual</span></span></td>
<td><span data-ttu-id="33539-156">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-157">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-158">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="33539-159">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-160">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-161">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="33539-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="33539-162">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33539-163">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="33539-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33539-164">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-164">Cost actual</span></span></td>
<td><span data-ttu-id="33539-165">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-166">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-167">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-168">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-169">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-170">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="33539-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33539-171">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-172">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="33539-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33539-173">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33539-174">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="33539-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33539-175">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="33539-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33539-176">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-177">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-178">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-179">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-180">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-181">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-181">Billed sales</span></span></td>
<td><span data-ttu-id="33539-182">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33539-183">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="33539-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33539-184">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="33539-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33539-185">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-187">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-188">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-189">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-190">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="33539-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33539-191">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-192">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="33539-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33539-193">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33539-194">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="33539-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33539-195">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="33539-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33539-196">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="33539-197">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="33539-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="33539-198">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="33539-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="33539-199">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-200">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-201">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-202">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-202">Billed sales</span></span></td>
<td><span data-ttu-id="33539-203">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33539-204">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="33539-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33539-205">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="33539-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33539-206">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-207">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="33539-208">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-209">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="33539-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="33539-210">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33539-211">**Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön**</span><span class="sxs-lookup"><span data-stu-id="33539-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="33539-212">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="33539-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="33539-213">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="33539-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="33539-214">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="33539-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="33539-215">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="33539-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="33539-216">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="33539-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="33539-217">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="33539-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="33539-218">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="33539-218">Actuals</span></span></th>
<th><span data-ttu-id="33539-219">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="33539-219">Transaction currency</span></span></th>
<th><span data-ttu-id="33539-220">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="33539-220">Fixed price</span></span></th>
<th><span data-ttu-id="33539-221">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="33539-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33539-222">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="33539-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="33539-223">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="33539-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-224">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="33539-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="33539-225">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="33539-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="33539-226">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="33539-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33539-227">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-227">Cost actual</span></span></td>
<td><span data-ttu-id="33539-228">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="33539-229">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="33539-230">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="33539-231">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="33539-232">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-233">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="33539-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="33539-234">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-235">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="33539-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="33539-236">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-237">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="33539-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="33539-238">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="33539-239">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="33539-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33539-240">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-240">Cost actual</span></span></td>
<td><span data-ttu-id="33539-241">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-242">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-243">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-244">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-245">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="33539-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-246">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="33539-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="33539-247">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-248">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="33539-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="33539-249">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-250">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="33539-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33539-251">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-252">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="33539-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33539-253">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33539-254">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="33539-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33539-255">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="33539-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33539-256">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-257">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-258">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-259">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="33539-260">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-261">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-261">Billed sales</span></span></td>
<td><span data-ttu-id="33539-262">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33539-263">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="33539-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33539-264">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="33539-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33539-265">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-266">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-267">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-268">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33539-269">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-270">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="33539-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33539-271">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-272">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="33539-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33539-273">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33539-274">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="33539-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33539-275">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="33539-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33539-276">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="33539-277">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="33539-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="33539-278">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="33539-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="33539-279">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-280">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="33539-281">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="33539-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-282">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-282">Billed sales</span></span></td>
<td><span data-ttu-id="33539-283">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33539-284">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="33539-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33539-285">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="33539-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33539-286">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-287">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="33539-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="33539-288">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33539-289">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="33539-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="33539-290">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="33539-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
