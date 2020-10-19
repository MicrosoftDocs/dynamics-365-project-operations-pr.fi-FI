---
title: Toteutuneiden aloitussivu
description: Tämä aihe tarjoaa tietoja todellisten arvojen käsittelemisestä Microsoft Dynamics 365 Project Operationsissa.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907314"
---
# <a name="actuals"></a><span data-ttu-id="01e86-103">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="01e86-103">Actuals</span></span>

<span data-ttu-id="01e86-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="01e86-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="01e86-105">Todelliset arvot vastaavat työmäärää, joka projektissa on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="01e86-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="01e86-106">Ne luodaan aika- ja kulutapahtumien sekä päiväkirjakirjausten ja laskujen tuloksena.</span><span class="sxs-lookup"><span data-stu-id="01e86-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="01e86-107">Kirjauskansion rivit ja ajan lähetys</span><span class="sxs-lookup"><span data-stu-id="01e86-107">Journal lines and time submission</span></span>

<span data-ttu-id="01e86-108">Lisätietoja ajan syöttämisestä on ohjeaiheessa [Ajan syöttämisen yleiskatsaus](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="01e86-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="01e86-109">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="01e86-109">Time and materials</span></span>

<span data-ttu-id="01e86-110">Kun lähetetty ajankohta linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="01e86-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="01e86-111">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="01e86-111">Fixed price</span></span>

<span data-ttu-id="01e86-112">Kun lähetetään sellaiseen projektiin linkitetty aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo kirjauskansion rivi kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="01e86-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="01e86-113">Oletushinnoittelu</span><span class="sxs-lookup"><span data-stu-id="01e86-113">Default pricing</span></span>

<span data-ttu-id="01e86-114">Oletushintojen luonnin logiikka on kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="01e86-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="01e86-115">Aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="01e86-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="01e86-116">Nämä arvot sisältävät tapahtumapäivämäärän, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="01e86-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="01e86-117">Oletushinnoitteluun vaikuttavia kenttiä, kuten **Rooli** ja **Organisaatioyksiköt**, käytetään määrittämään asianmukainen hinta kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="01e86-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="01e86-118">Voit lisätä mukautetun kentän ajankohdalle.</span><span class="sxs-lookup"><span data-stu-id="01e86-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="01e86-119">Jos haluat, että kentän arvo välitetään todellisiin arvoihin, luo kenttä Todelliset arvot -entiteettiin ja käytä kenttien yhdistämistä kopioidaksesi kentän aikamerkinnästä todelliseen arvoon.</span><span class="sxs-lookup"><span data-stu-id="01e86-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="01e86-120">Kirjauskansiorivit ja peruskulujen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="01e86-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="01e86-121">Lisätietoja kulun syöttämisestä on ohjeaiheessa [Kulujen syöttämisen yleiskatsaus](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="01e86-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="01e86-122">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="01e86-122">Time and materials</span></span>

<span data-ttu-id="01e86-123">Kun lähetetty perustukulumerkintä linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="01e86-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="01e86-124">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="01e86-124">Fixed price</span></span>

<span data-ttu-id="01e86-125">Kun lähetetään sellaiseen projektiin linkitetty peruskulumerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo kirjauskansion rivi kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="01e86-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="01e86-126">Oletushinnoittelu</span><span class="sxs-lookup"><span data-stu-id="01e86-126">Default pricing</span></span>

<span data-ttu-id="01e86-127">Kulujen oletushintojen syöttämiseen liittyvä logiikka perustuu kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="01e86-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="01e86-128">Oikean hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="01e86-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="01e86-129">Itse hinnan osalta syötetty summa asetetaan oletusarvoisesti suoraan siihen liittyvien kulujen kirjauskansion kustannus- ja myyntirivien arvoksi.</span><span class="sxs-lookup"><span data-stu-id="01e86-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="01e86-130">Luokkaperusteista merkintää yksikkökohtaisista kulumerkintöjen oletushinnoista ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="01e86-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="01e86-131">Tapahtumakirjauskansioiden käyttö kustannusten tallentamiseen</span><span class="sxs-lookup"><span data-stu-id="01e86-131">Use entry journals to record costs</span></span>

<span data-ttu-id="01e86-132">Tapahtumakirjauskansioihin voit tallentaa kustannuksia tai tuottoja luokkiin materiaali, maksu, kulu ja verotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="01e86-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="01e86-133">Kirjauskansioita voi käyttää seuraaviin tarkoituksiin:</span><span class="sxs-lookup"><span data-stu-id="01e86-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="01e86-134">Tallenna projektin materiaalien todelliset kustannukset ja myynti.</span><span class="sxs-lookup"><span data-stu-id="01e86-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="01e86-135">Siirrä tapahtumien todellisia arvoja toisesta järjestelmästä Microsoft Dynamics 365 Project Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="01e86-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="01e86-136">Tallenna kustannukset, jotka tapahtuivat toisessa järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="01e86-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="01e86-137">Nämä kustannukset voivat sisältää hankinta- tai alihankintakustannuksia.</span><span class="sxs-lookup"><span data-stu-id="01e86-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01e86-138">Sovellus ei tarkista päiväkirjan rivin tyyppiä tai siihen liittyvää hinnoittelua, joka on syötetty päiväkirjan riville.</span><span class="sxs-lookup"><span data-stu-id="01e86-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="01e86-139">Siksi vain käyttäjä, joka on täysin tietoinen todellisten arvojen kirjanpidollisesta vaikutuksesta projekteihin, voi käyttää tapahtumakirjauskansioita todellisten arvojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="01e86-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="01e86-140">Tämän kirjauskansiotyypin vaikutuksen vuoksi sinun on valittava huolellisesti, kenellä on oikeus luoda tapahtumakirjauskansioita.</span><span class="sxs-lookup"><span data-stu-id="01e86-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="01e86-141">Todellisten arvojen tallentaminen projektitapahtumien perusteella</span><span class="sxs-lookup"><span data-stu-id="01e86-141">Record actuals based on project events</span></span>

<span data-ttu-id="01e86-142">Project Operations tallentaa projektin aikana esiintyvät taloudelliset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="01e86-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="01e86-143">Nämä tapahtumat kirjataan muodossa Todelliset arvot.</span><span class="sxs-lookup"><span data-stu-id="01e86-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="01e86-144">Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.</span><span class="sxs-lookup"><span data-stu-id="01e86-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="01e86-145">Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö</span><span class="sxs-lookup"><span data-stu-id="01e86-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="01e86-146">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="01e86-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="01e86-147">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="01e86-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="01e86-148">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="01e86-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="01e86-149">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="01e86-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="01e86-150">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="01e86-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="01e86-151">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="01e86-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="01e86-152">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="01e86-152">Actuals</span></span></th>
<th><span data-ttu-id="01e86-153">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="01e86-153">Transaction currency</span></span></th>
<th><span data-ttu-id="01e86-154">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="01e86-154">Fixed price</span></span></th>
<th><span data-ttu-id="01e86-155">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="01e86-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="01e86-156">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="01e86-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="01e86-157">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="01e86-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-158">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="01e86-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="01e86-159">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="01e86-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01e86-160">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="01e86-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01e86-161">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-161">Cost actual</span></span></td>
<td><span data-ttu-id="01e86-162">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-163">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-164">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="01e86-165">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-166">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-167">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="01e86-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="01e86-168">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01e86-169">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="01e86-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01e86-170">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-170">Cost actual</span></span></td>
<td><span data-ttu-id="01e86-171">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-172">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-173">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-174">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-175">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-176">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="01e86-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01e86-177">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-178">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="01e86-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01e86-179">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01e86-180">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="01e86-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01e86-181">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01e86-182">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-183">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-184">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-185">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-186">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-187">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-187">Billed sales</span></span></td>
<td><span data-ttu-id="01e86-188">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01e86-189">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="01e86-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01e86-190">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01e86-191">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-192">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-193">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-194">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-195">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-196">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="01e86-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01e86-197">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-198">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="01e86-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01e86-199">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01e86-200">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="01e86-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01e86-201">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01e86-202">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="01e86-203">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="01e86-204">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="01e86-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="01e86-205">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-206">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-207">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-208">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-208">Billed sales</span></span></td>
<td><span data-ttu-id="01e86-209">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01e86-210">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="01e86-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01e86-211">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01e86-212">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-213">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="01e86-214">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-215">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="01e86-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="01e86-216">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="01e86-217">Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön</span><span class="sxs-lookup"><span data-stu-id="01e86-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="01e86-218">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="01e86-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="01e86-219">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="01e86-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="01e86-220">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="01e86-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="01e86-221">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="01e86-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="01e86-222">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="01e86-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="01e86-223">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="01e86-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="01e86-224">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="01e86-224">Actuals</span></span></th>
<th><span data-ttu-id="01e86-225">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="01e86-225">Transaction currency</span></span></th>
<th><span data-ttu-id="01e86-226">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="01e86-226">Fixed price</span></span></th>
<th><span data-ttu-id="01e86-227">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="01e86-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="01e86-228">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="01e86-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="01e86-229">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="01e86-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-230">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="01e86-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="01e86-231">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="01e86-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="01e86-232">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="01e86-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01e86-233">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-233">Cost actual</span></span></td>
<td><span data-ttu-id="01e86-234">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="01e86-235">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="01e86-236">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="01e86-237">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="01e86-238">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-239">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="01e86-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="01e86-240">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-241">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="01e86-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="01e86-242">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-243">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="01e86-244">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="01e86-245">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="01e86-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01e86-246">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-246">Cost actual</span></span></td>
<td><span data-ttu-id="01e86-247">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-248">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-249">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-250">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-251">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="01e86-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-252">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="01e86-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="01e86-253">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-254">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="01e86-255">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-256">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="01e86-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01e86-257">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-258">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="01e86-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01e86-259">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01e86-260">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="01e86-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01e86-261">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01e86-262">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-263">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-264">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-265">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="01e86-266">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-267">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-267">Billed sales</span></span></td>
<td><span data-ttu-id="01e86-268">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01e86-269">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="01e86-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01e86-270">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01e86-271">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-272">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-273">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-274">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01e86-275">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-276">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="01e86-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01e86-277">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-278">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="01e86-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01e86-279">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01e86-280">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="01e86-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01e86-281">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01e86-282">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="01e86-283">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="01e86-284">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="01e86-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="01e86-285">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-286">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="01e86-287">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="01e86-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-288">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-288">Billed sales</span></span></td>
<td><span data-ttu-id="01e86-289">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01e86-290">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="01e86-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01e86-291">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="01e86-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01e86-292">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-293">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="01e86-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="01e86-294">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01e86-295">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="01e86-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="01e86-296">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="01e86-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
