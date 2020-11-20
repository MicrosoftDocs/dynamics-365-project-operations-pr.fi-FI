---
title: Todelliset arvot
description: Tämä aihe tarjoaa tietoja todellisten arvojen käsittelemisestä Microsoft Dynamics 365 Project Operationsissa.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126299"
---
# <a name="actuals"></a><span data-ttu-id="681bf-103">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="681bf-103">Actuals</span></span> 

<span data-ttu-id="681bf-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="681bf-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="681bf-105">Todelliset arvot vastaavat työmäärää, joka projektissa on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="681bf-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="681bf-106">Ne luodaan aika- ja kulutapahtumien sekä päiväkirjakirjausten ja laskujen tuloksena.</span><span class="sxs-lookup"><span data-stu-id="681bf-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="681bf-107">Kirjauskansion rivit ja ajan lähetys</span><span class="sxs-lookup"><span data-stu-id="681bf-107">Journal lines and time submission</span></span>

<span data-ttu-id="681bf-108">Lisätietoja ajan syöttämisestä on ohjeaiheessa [Ajan syöttämisen yleiskatsaus](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="681bf-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="681bf-109">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="681bf-109">Time and materials</span></span>

<span data-ttu-id="681bf-110">Kun lähetetty ajankohta linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="681bf-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="681bf-111">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="681bf-111">Fixed price</span></span>

<span data-ttu-id="681bf-112">Kun lähetetään sellaiseen projektiin linkitetty aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo kirjauskansion rivi kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="681bf-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="681bf-113">Oletushinnoittelu</span><span class="sxs-lookup"><span data-stu-id="681bf-113">Default pricing</span></span>

<span data-ttu-id="681bf-114">Oletushintojen luonnin logiikka on kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="681bf-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="681bf-115">Aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="681bf-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="681bf-116">Nämä arvot sisältävät tapahtumapäivämäärän, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="681bf-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="681bf-117">Oletushinnoitteluun vaikuttavia kenttiä, kuten **Rooli** ja **Organisaatioyksiköt**, käytetään määrittämään asianmukainen hinta kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="681bf-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="681bf-118">Voit lisätä mukautetun kentän ajankohdalle.</span><span class="sxs-lookup"><span data-stu-id="681bf-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="681bf-119">Jos haluat, että kentän arvo välitetään todellisiin arvoihin, luo kenttä Todelliset arvot -entiteettiin ja käytä kenttien yhdistämistä kopioidaksesi kentän aikamerkinnästä todelliseen arvoon.</span><span class="sxs-lookup"><span data-stu-id="681bf-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="681bf-120">Kirjauskansiorivit ja peruskulujen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="681bf-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="681bf-121">Lisätietoja kulun syöttämisestä on ohjeaiheessa [Kulujen syöttämisen yleiskatsaus](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="681bf-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="681bf-122">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="681bf-122">Time and materials</span></span>

<span data-ttu-id="681bf-123">Kun lähetetty perustukulumerkintä linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="681bf-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="681bf-124">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="681bf-124">Fixed price</span></span>

<span data-ttu-id="681bf-125">Kun lähetetään sellaiseen projektiin linkitetty peruskulumerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo kirjauskansion rivi kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="681bf-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="681bf-126">Oletushinnoittelu</span><span class="sxs-lookup"><span data-stu-id="681bf-126">Default pricing</span></span>

<span data-ttu-id="681bf-127">Kulujen oletushintojen syöttämiseen liittyvä logiikka perustuu kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="681bf-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="681bf-128">Oikean hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="681bf-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="681bf-129">Itse hinnan osalta syötetty summa asetetaan oletusarvoisesti suoraan siihen liittyvien kulujen kirjauskansion kustannus- ja myyntirivien arvoksi.</span><span class="sxs-lookup"><span data-stu-id="681bf-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="681bf-130">Luokkaperusteista merkintää yksikkökohtaisista kulumerkintöjen oletushinnoista ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="681bf-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="681bf-131">Tapahtumakirjauskansioiden käyttö kustannusten tallentamiseen</span><span class="sxs-lookup"><span data-stu-id="681bf-131">Use entry journals to record costs</span></span>

<span data-ttu-id="681bf-132">Tapahtumakirjauskansioihin voit tallentaa kustannuksia tai tuottoja luokkiin materiaali, maksu, kulu ja verotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="681bf-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="681bf-133">Kirjauskansioita voi käyttää seuraaviin tarkoituksiin:</span><span class="sxs-lookup"><span data-stu-id="681bf-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="681bf-134">Tallenna projektin materiaalien todelliset kustannukset ja myynti.</span><span class="sxs-lookup"><span data-stu-id="681bf-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="681bf-135">Siirrä tapahtumien todellisia arvoja toisesta järjestelmästä Microsoft Dynamics 365 Project Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="681bf-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="681bf-136">Tallenna kustannukset, jotka tapahtuivat toisessa järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="681bf-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="681bf-137">Nämä kustannukset voivat sisältää hankinta- tai alihankintakustannuksia.</span><span class="sxs-lookup"><span data-stu-id="681bf-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="681bf-138">Sovellus ei tarkista päiväkirjan rivin tyyppiä tai siihen liittyvää hinnoittelua, joka on syötetty päiväkirjan riville.</span><span class="sxs-lookup"><span data-stu-id="681bf-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="681bf-139">Siksi vain käyttäjä, joka on täysin tietoinen todellisten arvojen kirjanpidollisesta vaikutuksesta projekteihin, voi käyttää tapahtumakirjauskansioita todellisten arvojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="681bf-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="681bf-140">Tämän kirjauskansiotyypin vaikutuksen vuoksi sinun on valittava huolellisesti, kenellä on oikeus luoda tapahtumakirjauskansioita.</span><span class="sxs-lookup"><span data-stu-id="681bf-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="681bf-141">Todellisten arvojen tallentaminen projektitapahtumien perusteella</span><span class="sxs-lookup"><span data-stu-id="681bf-141">Record actuals based on project events</span></span>

<span data-ttu-id="681bf-142">Project Operations tallentaa projektin aikana esiintyvät taloudelliset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="681bf-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="681bf-143">Nämä tapahtumat kirjataan muodossa Todelliset arvot.</span><span class="sxs-lookup"><span data-stu-id="681bf-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="681bf-144">Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.</span><span class="sxs-lookup"><span data-stu-id="681bf-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="681bf-145">Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö</span><span class="sxs-lookup"><span data-stu-id="681bf-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="681bf-146">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="681bf-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="681bf-147">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="681bf-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="681bf-148">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="681bf-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="681bf-149">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="681bf-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="681bf-150">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="681bf-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="681bf-151">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="681bf-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="681bf-152">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="681bf-152">Actuals</span></span></th>
<th><span data-ttu-id="681bf-153">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="681bf-153">Transaction currency</span></span></th>
<th><span data-ttu-id="681bf-154">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="681bf-154">Fixed price</span></span></th>
<th><span data-ttu-id="681bf-155">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="681bf-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="681bf-156">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="681bf-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="681bf-157">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="681bf-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-158">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="681bf-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="681bf-159">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="681bf-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="681bf-160">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="681bf-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="681bf-161">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-161">Cost actual</span></span></td>
<td><span data-ttu-id="681bf-162">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-163">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-164">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="681bf-165">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-166">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-167">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="681bf-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="681bf-168">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="681bf-169">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="681bf-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="681bf-170">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-170">Cost actual</span></span></td>
<td><span data-ttu-id="681bf-171">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-172">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-173">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-174">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-175">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-176">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="681bf-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="681bf-177">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-178">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="681bf-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="681bf-179">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="681bf-180">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="681bf-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="681bf-181">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="681bf-182">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-183">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-184">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-185">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-187">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-187">Billed sales</span></span></td>
<td><span data-ttu-id="681bf-188">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="681bf-189">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="681bf-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="681bf-190">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="681bf-191">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-192">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-193">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-194">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-195">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-196">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="681bf-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="681bf-197">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-198">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="681bf-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="681bf-199">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="681bf-200">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="681bf-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="681bf-201">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="681bf-202">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="681bf-203">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="681bf-204">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="681bf-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="681bf-205">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-206">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-207">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-208">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-208">Billed sales</span></span></td>
<td><span data-ttu-id="681bf-209">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="681bf-210">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="681bf-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="681bf-211">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="681bf-212">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-213">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="681bf-214">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-215">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="681bf-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="681bf-216">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="681bf-217">Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön</span><span class="sxs-lookup"><span data-stu-id="681bf-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="681bf-218">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="681bf-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="681bf-219">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="681bf-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="681bf-220">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="681bf-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="681bf-221">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="681bf-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="681bf-222">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="681bf-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="681bf-223">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="681bf-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="681bf-224">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="681bf-224">Actuals</span></span></th>
<th><span data-ttu-id="681bf-225">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="681bf-225">Transaction currency</span></span></th>
<th><span data-ttu-id="681bf-226">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="681bf-226">Fixed price</span></span></th>
<th><span data-ttu-id="681bf-227">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="681bf-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="681bf-228">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="681bf-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="681bf-229">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="681bf-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-230">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="681bf-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="681bf-231">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="681bf-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="681bf-232">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="681bf-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="681bf-233">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-233">Cost actual</span></span></td>
<td><span data-ttu-id="681bf-234">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="681bf-235">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="681bf-236">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="681bf-237">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="681bf-238">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-239">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="681bf-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="681bf-240">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-241">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="681bf-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="681bf-242">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-243">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="681bf-244">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="681bf-245">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="681bf-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="681bf-246">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-246">Cost actual</span></span></td>
<td><span data-ttu-id="681bf-247">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-248">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-249">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-250">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-251">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="681bf-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-252">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="681bf-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="681bf-253">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-254">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="681bf-255">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-256">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="681bf-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="681bf-257">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-258">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="681bf-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="681bf-259">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="681bf-260">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="681bf-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="681bf-261">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="681bf-262">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-263">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-264">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-265">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="681bf-266">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-267">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-267">Billed sales</span></span></td>
<td><span data-ttu-id="681bf-268">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="681bf-269">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="681bf-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="681bf-270">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="681bf-271">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-272">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-273">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-274">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="681bf-275">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-276">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="681bf-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="681bf-277">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-278">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="681bf-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="681bf-279">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="681bf-280">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="681bf-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="681bf-281">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="681bf-282">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="681bf-283">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="681bf-284">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="681bf-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="681bf-285">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-286">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="681bf-287">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="681bf-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-288">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-288">Billed sales</span></span></td>
<td><span data-ttu-id="681bf-289">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="681bf-290">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="681bf-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="681bf-291">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="681bf-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="681bf-292">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-293">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="681bf-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="681bf-294">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="681bf-295">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="681bf-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="681bf-296">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="681bf-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
