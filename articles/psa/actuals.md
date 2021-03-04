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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146119"
---
# <a name="actuals-overview"></a><span data-ttu-id="d9ce9-103">Toteutuneiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d9ce9-104">Todelliset arvot vastaavat työmäärää, joka projektissa on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d9ce9-105">Projektin todelliset arvot voidaan jäljittää lähdeasiakirjoihinsa.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="d9ce9-106">Lähdeasiakirjoja ovat aika, kulu, kirjauskansioviennit ja myös laskut.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Projektin todellisten arvojen jäljittäminen lähdeasiakirjoihin](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="d9ce9-108">Aikamerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="d9ce9-108">Submitting a time entry</span></span>

<span data-ttu-id="d9ce9-109">Kun PSA:ssa lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d9ce9-110">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d9ce9-111">Kun lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="d9ce9-112">Oletushintojen antamisen logiikka on kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="d9ce9-113">Kaikkien aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="d9ce9-114">Nämä kentät sisältävät tapahtuman päiväyksen, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="d9ce9-115">Oletushintoihin vaikuttavat kentät, kuten **Rooli** ja **Organisaatioyksiköt** varmistavat, että kirjauskansion riville täytetään oletusarvoisesti asianmukainen hinta.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="d9ce9-116">Jos lisäät aikamerkintään muokatun kentän ja haluat, että kentän arvo välitetään todellisiin arvoihin, luo kenttä Todelliset arvot -entiteettiin ja käytä kenttien yhdistämistä kopioidaksesi kentän aikamerkinnästä todelliseen arvoon.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="d9ce9-117">Kulumerkinnän lähettäminen</span><span class="sxs-lookup"><span data-stu-id="d9ce9-117">Submitting an expense entry</span></span>

<span data-ttu-id="d9ce9-118">Kun PSA:ssa lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d9ce9-119">Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d9ce9-120">Kun lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="d9ce9-121">Kulujen oletushintojen antamisen logiikka perustuu kululuokkaan, joka valitaan **Kulumerkintä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="d9ce9-122">Oikean hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d9ce9-123">Itse hinnan osalta käyttäjän antama summa asetetaan oletusarvoisesti suoraan siihen liittyvien kulujen kirjauskansion kustannus- ja myyntirivien arvoksi.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="d9ce9-124">Nykyisessä PSA:n versiossa, luokkaperusteista merkintää yksikkökohtaisista kulumerkintöjen oletushinnoista ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="d9ce9-125">Kirjauskansioiden käyttö kustannusten tallentamiseen</span><span class="sxs-lookup"><span data-stu-id="d9ce9-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="d9ce9-126">PSA:ssa kirjauskansioihin voi tallentaa kustannuksia tai tuottoja materiaali-, maksu-, aika-, kulu- ja verotapahtumaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d9ce9-127">Kirjauskansiossa on otsikko, rivejä ja **Vahvista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="d9ce9-128">Seuraavassa on skenaarioita, joissa saatetaan käyttää kirjauskansiota:</span><span class="sxs-lookup"><span data-stu-id="d9ce9-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="d9ce9-129">Sinun on tallennettava projektin materiaalien todellisia kustannuksia ja myyntejä.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="d9ce9-130">Sinun on siirrettävä tapahtumien todellisia arvoja toisesta järjestelmästä PSA:han.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="d9ce9-131">Sinun on tallennettava toisessa järjestelmässä aiheutuneita kustannuksia, kuten hankinta- tai alihankintakustannuksia.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9ce9-132">Toteutuneiden luonti kirjauskansioiden avulla sopii vain sellaiselle käyttäjälle, joka on täysin tietoinen siitä, mikä kirjanpitovaikutus toteutuneilla on projektiin.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="d9ce9-133">Syynä on se, että sovellus ei tarkista kirjauskansion rivityyppiä tai kirjauskansion rivillä annettua liittyvää hinnoittelua.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d9ce9-134">Tämän kirjauskansiotyypin vaikutuksen vuoksi onkin harkittava riittävän tarkasti, kenelle tämän kirjauskansion luontioikeus annetaan.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="d9ce9-135">Todellisten arvojen tallentaminen projektitapahtumien perusteella</span><span class="sxs-lookup"><span data-stu-id="d9ce9-135">Recording actuals based on project events</span></span>

<span data-ttu-id="d9ce9-136">PSA tallentaa projektin aikana esiintyvät taloudelliset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d9ce9-137">Nämä tapahtumat kirjataan muodossa **Todelliset arvot**.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="d9ce9-138">Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="d9ce9-139">**Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö**</span><span class="sxs-lookup"><span data-stu-id="d9ce9-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d9ce9-140">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="d9ce9-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d9ce9-141">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d9ce9-142">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="d9ce9-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d9ce9-143">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d9ce9-144">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="d9ce9-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d9ce9-145">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="d9ce9-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d9ce9-146">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="d9ce9-146">Actuals</span></span></th>
<th><span data-ttu-id="d9ce9-147">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-147">Transaction currency</span></span></th>
<th><span data-ttu-id="d9ce9-148">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="d9ce9-148">Fixed price</span></span></th>
<th><span data-ttu-id="d9ce9-149">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9ce9-150">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d9ce9-151">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-152">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d9ce9-153">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d9ce9-154">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d9ce9-155">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-155">Cost actual</span></span></td>
<td><span data-ttu-id="d9ce9-156">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-157">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-158">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d9ce9-159">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-160">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-161">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="d9ce9-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d9ce9-162">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d9ce9-163">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d9ce9-164">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-164">Cost actual</span></span></td>
<td><span data-ttu-id="d9ce9-165">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-166">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-167">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-168">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-169">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-170">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="d9ce9-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d9ce9-171">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-172">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d9ce9-173">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d9ce9-174">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d9ce9-175">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d9ce9-176">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-177">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-178">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-179">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-180">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-181">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-181">Billed sales</span></span></td>
<td><span data-ttu-id="d9ce9-182">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d9ce9-183">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d9ce9-184">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d9ce9-185">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-187">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-188">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-189">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-190">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="d9ce9-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d9ce9-191">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-192">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d9ce9-193">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d9ce9-194">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d9ce9-195">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d9ce9-196">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d9ce9-197">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d9ce9-198">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="d9ce9-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d9ce9-199">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-200">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-201">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-202">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-202">Billed sales</span></span></td>
<td><span data-ttu-id="d9ce9-203">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d9ce9-204">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d9ce9-205">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d9ce9-206">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-207">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d9ce9-208">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-209">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="d9ce9-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d9ce9-210">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9ce9-211">**Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön**</span><span class="sxs-lookup"><span data-stu-id="d9ce9-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d9ce9-212">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="d9ce9-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d9ce9-213">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d9ce9-214">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="d9ce9-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d9ce9-215">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d9ce9-216">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="d9ce9-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d9ce9-217">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="d9ce9-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d9ce9-218">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="d9ce9-218">Actuals</span></span></th>
<th><span data-ttu-id="d9ce9-219">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-219">Transaction currency</span></span></th>
<th><span data-ttu-id="d9ce9-220">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="d9ce9-220">Fixed price</span></span></th>
<th><span data-ttu-id="d9ce9-221">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9ce9-222">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d9ce9-223">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-224">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d9ce9-225">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d9ce9-226">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d9ce9-227">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-227">Cost actual</span></span></td>
<td><span data-ttu-id="d9ce9-228">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d9ce9-229">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d9ce9-230">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d9ce9-231">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d9ce9-232">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-233">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="d9ce9-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d9ce9-234">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-235">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d9ce9-236">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-237">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d9ce9-238">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d9ce9-239">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d9ce9-240">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-240">Cost actual</span></span></td>
<td><span data-ttu-id="d9ce9-241">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-242">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-243">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-244">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-245">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="d9ce9-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-246">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d9ce9-247">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-248">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d9ce9-249">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-250">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="d9ce9-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d9ce9-251">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-252">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d9ce9-253">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d9ce9-254">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d9ce9-255">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d9ce9-256">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-257">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-258">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-259">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d9ce9-260">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-261">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-261">Billed sales</span></span></td>
<td><span data-ttu-id="d9ce9-262">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d9ce9-263">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d9ce9-264">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d9ce9-265">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-266">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-267">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-268">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d9ce9-269">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-270">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="d9ce9-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d9ce9-271">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-272">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d9ce9-273">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d9ce9-274">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d9ce9-275">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d9ce9-276">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d9ce9-277">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d9ce9-278">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="d9ce9-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d9ce9-279">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-280">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d9ce9-281">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="d9ce9-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-282">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-282">Billed sales</span></span></td>
<td><span data-ttu-id="d9ce9-283">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d9ce9-284">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d9ce9-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d9ce9-285">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="d9ce9-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d9ce9-286">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-287">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="d9ce9-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d9ce9-288">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9ce9-289">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="d9ce9-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d9ce9-290">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="d9ce9-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
