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
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285614"
---
# <a name="actuals-overview"></a><span data-ttu-id="8269c-103">Toteutuneiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8269c-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8269c-104">Todelliset arvot vastaavat työmäärää, joka projektissa on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="8269c-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="8269c-105">Projektin todelliset arvot voidaan jäljittää lähdeasiakirjoihinsa.</span><span class="sxs-lookup"><span data-stu-id="8269c-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="8269c-106">Lähdeasiakirjoja ovat aika, kulu, kirjauskansioviennit ja myös laskut.</span><span class="sxs-lookup"><span data-stu-id="8269c-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Projektin todellisten arvojen jäljittäminen lähdeasiakirjoihin](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="8269c-108">Aikamerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="8269c-108">Submitting a time entry</span></span>

<span data-ttu-id="8269c-109">Kun PSA:ssa lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="8269c-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="8269c-110">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="8269c-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="8269c-111">Kun lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="8269c-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="8269c-112">Oletushintojen antamisen logiikka on kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="8269c-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="8269c-113">Kaikkien aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="8269c-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="8269c-114">Nämä kentät sisältävät tapahtuman päiväyksen, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="8269c-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="8269c-115">Oletushintoihin vaikuttavat kentät, kuten **Rooli** ja **Organisaatioyksiköt** varmistavat, että kirjauskansion riville täytetään oletusarvoisesti asianmukainen hinta.</span><span class="sxs-lookup"><span data-stu-id="8269c-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="8269c-116">Jos lisäät aikamerkintään muokatun kentän ja haluat, että kentän arvo välitetään todellisiin arvoihin, luo kenttä Todelliset arvot -entiteettiin ja käytä kenttien yhdistämistä kopioidaksesi kentän aikamerkinnästä todelliseen arvoon.</span><span class="sxs-lookup"><span data-stu-id="8269c-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="8269c-117">Kulumerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="8269c-117">Submitting an expense entry</span></span>

<span data-ttu-id="8269c-118">Kun PSA:ssa lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="8269c-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="8269c-119">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="8269c-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="8269c-120">Kun lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="8269c-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="8269c-121">Kulujen oletushintojen antamisen logiikka perustuu kululuokkaan, joka valitaan **Kulumerkintä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8269c-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="8269c-122">Oikean hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="8269c-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="8269c-123">Itse hinnan osalta käyttäjän antama summa asetetaan oletusarvoisesti suoraan siihen liittyvien kulujen kirjauskansion kustannus- ja myyntirivien arvoksi.</span><span class="sxs-lookup"><span data-stu-id="8269c-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="8269c-124">Nykyisessä PSA:n versiossa, luokkaperusteista merkintää yksikkökohtaisista kulumerkintöjen oletushinnoista ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="8269c-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="8269c-125">Kirjauskansioiden käyttö kustannusten tallentamiseen</span><span class="sxs-lookup"><span data-stu-id="8269c-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="8269c-126">PSA:ssa kirjauskansioihin voi tallentaa kustannuksia tai tuottoja materiaali-, maksu-, aika-, kulu- ja verotapahtumaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="8269c-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="8269c-127">Kirjauskansiossa on otsikko, rivejä ja **Vahvista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="8269c-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="8269c-128">Seuraavassa on skenaarioita, joissa saatetaan käyttää kirjauskansiota:</span><span class="sxs-lookup"><span data-stu-id="8269c-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="8269c-129">Sinun on tallennettava projektin materiaalien todellisia kustannuksia ja myyntejä.</span><span class="sxs-lookup"><span data-stu-id="8269c-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="8269c-130">Sinun on siirrettävä tapahtumien todellisia arvoja toisesta järjestelmästä PSA:han.</span><span class="sxs-lookup"><span data-stu-id="8269c-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="8269c-131">Sinun on tallennettava toisessa järjestelmässä aiheutuneita kustannuksia, kuten hankinta- tai alihankintakustannuksia.</span><span class="sxs-lookup"><span data-stu-id="8269c-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8269c-132">Toteutuneiden luonti kirjauskansioiden avulla sopii vain sellaiselle käyttäjälle, joka on täysin tietoinen siitä, mikä kirjanpitovaikutus toteutuneilla on projektiin.</span><span class="sxs-lookup"><span data-stu-id="8269c-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="8269c-133">Syynä on se, että sovellus ei tarkista kirjauskansion rivityyppiä tai kirjauskansion rivillä annettua liittyvää hinnoittelua.</span><span class="sxs-lookup"><span data-stu-id="8269c-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="8269c-134">Tämän kirjauskansiotyypin vaikutuksen vuoksi onkin harkittava riittävän tarkasti, kenelle tämän kirjauskansion luontioikeus annetaan.</span><span class="sxs-lookup"><span data-stu-id="8269c-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="8269c-135">Todellisten arvojen tallentaminen projektitapahtumien perusteella</span><span class="sxs-lookup"><span data-stu-id="8269c-135">Recording actuals based on project events</span></span>

<span data-ttu-id="8269c-136">PSA tallentaa projektin aikana esiintyvät taloudelliset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="8269c-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="8269c-137">Nämä tapahtumat kirjataan muodossa **Todelliset arvot**.</span><span class="sxs-lookup"><span data-stu-id="8269c-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="8269c-138">Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.</span><span class="sxs-lookup"><span data-stu-id="8269c-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="8269c-139">**Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö**</span><span class="sxs-lookup"><span data-stu-id="8269c-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8269c-140">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="8269c-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8269c-141">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="8269c-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8269c-142">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="8269c-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8269c-143">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="8269c-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8269c-144">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="8269c-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8269c-145">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="8269c-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8269c-146">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="8269c-146">Actuals</span></span></th>
<th><span data-ttu-id="8269c-147">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="8269c-147">Transaction currency</span></span></th>
<th><span data-ttu-id="8269c-148">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="8269c-148">Fixed price</span></span></th>
<th><span data-ttu-id="8269c-149">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="8269c-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8269c-150">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="8269c-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8269c-151">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="8269c-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-152">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="8269c-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8269c-153">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="8269c-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8269c-154">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="8269c-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8269c-155">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-155">Cost actual</span></span></td>
<td><span data-ttu-id="8269c-156">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-157">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-158">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="8269c-159">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-160">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-161">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="8269c-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8269c-162">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8269c-163">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="8269c-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8269c-164">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-164">Cost actual</span></span></td>
<td><span data-ttu-id="8269c-165">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-166">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-167">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-168">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-169">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-170">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="8269c-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8269c-171">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-172">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="8269c-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8269c-173">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8269c-174">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="8269c-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8269c-175">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8269c-176">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-177">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-178">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-179">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-180">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-181">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-181">Billed sales</span></span></td>
<td><span data-ttu-id="8269c-182">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8269c-183">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="8269c-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8269c-184">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8269c-185">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-187">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-188">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-189">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-190">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="8269c-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8269c-191">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-192">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="8269c-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8269c-193">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8269c-194">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="8269c-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8269c-195">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8269c-196">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8269c-197">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8269c-198">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="8269c-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8269c-199">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-200">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-201">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-202">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-202">Billed sales</span></span></td>
<td><span data-ttu-id="8269c-203">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8269c-204">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="8269c-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8269c-205">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8269c-206">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-207">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8269c-208">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-209">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="8269c-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8269c-210">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8269c-211">**Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön**</span><span class="sxs-lookup"><span data-stu-id="8269c-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8269c-212">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="8269c-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8269c-213">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="8269c-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8269c-214">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="8269c-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8269c-215">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="8269c-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8269c-216">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="8269c-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8269c-217">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="8269c-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8269c-218">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="8269c-218">Actuals</span></span></th>
<th><span data-ttu-id="8269c-219">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="8269c-219">Transaction currency</span></span></th>
<th><span data-ttu-id="8269c-220">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="8269c-220">Fixed price</span></span></th>
<th><span data-ttu-id="8269c-221">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="8269c-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8269c-222">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="8269c-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8269c-223">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="8269c-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-224">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="8269c-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8269c-225">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="8269c-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="8269c-226">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="8269c-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8269c-227">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-227">Cost actual</span></span></td>
<td><span data-ttu-id="8269c-228">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8269c-229">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8269c-230">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8269c-231">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8269c-232">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-233">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="8269c-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8269c-234">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-235">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="8269c-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8269c-236">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-237">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8269c-238">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8269c-239">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="8269c-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8269c-240">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-240">Cost actual</span></span></td>
<td><span data-ttu-id="8269c-241">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-242">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-243">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-244">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-245">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="8269c-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-246">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="8269c-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8269c-247">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-248">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8269c-249">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-250">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="8269c-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8269c-251">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-252">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="8269c-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8269c-253">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8269c-254">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="8269c-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8269c-255">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8269c-256">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-257">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-258">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-259">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8269c-260">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-261">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-261">Billed sales</span></span></td>
<td><span data-ttu-id="8269c-262">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8269c-263">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="8269c-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8269c-264">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8269c-265">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-266">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-267">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-268">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8269c-269">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-270">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="8269c-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8269c-271">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-272">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="8269c-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8269c-273">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8269c-274">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="8269c-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8269c-275">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8269c-276">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8269c-277">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8269c-278">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="8269c-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8269c-279">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-280">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8269c-281">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8269c-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-282">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-282">Billed sales</span></span></td>
<td><span data-ttu-id="8269c-283">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8269c-284">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="8269c-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8269c-285">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="8269c-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8269c-286">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-287">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="8269c-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8269c-288">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8269c-289">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="8269c-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8269c-290">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="8269c-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]