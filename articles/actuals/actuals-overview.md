---
title: Todelliset arvot
description: Tässä aiheessa on tietoja Microsoft Dynamics 365 Project Operationsin todellisten arvojen käsittelystä.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368607"
---
# <a name="actuals"></a><span data-ttu-id="b94cf-103">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="b94cf-103">Actuals</span></span> 

<span data-ttu-id="b94cf-104">_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="b94cf-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b94cf-105">Toteutuneet arvot edustavat projektin arvioitua ja hyväksyttyä taloudellista ja aikataulun edistymistä.</span><span class="sxs-lookup"><span data-stu-id="b94cf-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="b94cf-106">Ne luodaan ajan, kulujen, materiaalin käyttömerkintöjen, kirjausten ja laskujen hyväksynnän tuloksena.</span><span class="sxs-lookup"><span data-stu-id="b94cf-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="b94cf-107">Kirjauskansion rivit ja ajan lähetys</span><span class="sxs-lookup"><span data-stu-id="b94cf-107">Journal lines and time submission</span></span>

<span data-ttu-id="b94cf-108">Lisätietoja ajan syöttämisestä on ohjeaiheessa [Ajan syöttämisen yleiskatsaus](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b94cf-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b94cf-109">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="b94cf-109">Time and materials</span></span>

<span data-ttu-id="b94cf-110">Kun lähetetty ajankohta linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="b94cf-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b94cf-111">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="b94cf-111">Fixed price</span></span>

<span data-ttu-id="b94cf-112">Kun lähetetään sellaiseen projektiin linkitetty aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo kirjauskansion rivi kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="b94cf-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b94cf-113">Oletushinnoittelu</span><span class="sxs-lookup"><span data-stu-id="b94cf-113">Default pricing</span></span>

<span data-ttu-id="b94cf-114">Oletushintojen luonnin logiikka on kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="b94cf-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="b94cf-115">Aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="b94cf-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="b94cf-116">Nämä arvot sisältävät tapahtumapäivämäärän, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="b94cf-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="b94cf-117">Oletushintoihin vaikuttavia kenttiä, kuten **Rooli** ja **Organisaatioyksikkö** käytetään kirjauskansion rivin sopivan hinnan määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="b94cf-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="b94cf-118">Voit lisätä mukautetun kentän ajankohdalle.</span><span class="sxs-lookup"><span data-stu-id="b94cf-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="b94cf-119">Jos haluat, että kentän arvo välitettään toteutuneisiin arvoihin, luo kenttä **Toteutuneet**- ja **Kirjausrivi**-taulukoihin.</span><span class="sxs-lookup"><span data-stu-id="b94cf-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="b94cf-120">Käytä mukautettua koodia, kun haluat välittää valitun kentän arvon ajan syötöstä toteutuneisiin arvoihin kirjausrivin kautta käyttämällä tapahtumien alkuperää.</span><span class="sxs-lookup"><span data-stu-id="b94cf-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="b94cf-121">Lisätietoja tapahtumien alkuperästä ja yhteyksistä on ohjeaiheessa [Toteutuneidenarvojen linkittäminen alkuperäisiin tietueisiin](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="b94cf-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="b94cf-122">Kirjauskansiorivit ja peruskulujen lähettäminen</span><span class="sxs-lookup"><span data-stu-id="b94cf-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="b94cf-123">Lisätietoja kulun syöttämisestä on ohjeaiheessa [Kulujen syöttämisen yleiskatsaus](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b94cf-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b94cf-124">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="b94cf-124">Time and materials</span></span>

<span data-ttu-id="b94cf-125">Kun lähetetty perustukulumerkintä linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="b94cf-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b94cf-126">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="b94cf-126">Fixed price</span></span>

<span data-ttu-id="b94cf-127">Kun lähetetty peruskulumerkintä on linkitetty projektiin, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo yhden kirjauskansion rivin kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="b94cf-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b94cf-128">Oletushinnoittelu</span><span class="sxs-lookup"><span data-stu-id="b94cf-128">Default pricing</span></span>

<span data-ttu-id="b94cf-129">Kulujen oletushintojen syöttämiseen liittyvä logiikka perustuu kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="b94cf-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="b94cf-130">Sopivan hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="b94cf-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="b94cf-131">Oletushintoihin vaikuttavia kenttiä, kuten **Tapahtumaluokka** ja **Yksikkö** käytetään kirjauskansion rivin sopivan hinnan määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="b94cf-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="b94cf-132">Tämä toimii kuitenkin vain, jos hinnaston hinnoittelutapa on **Yksikköhinta**.</span><span class="sxs-lookup"><span data-stu-id="b94cf-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="b94cf-133">Jos hinnoittelutapa on **Kustannuksen arvo** tai **Hinnankorotus kustannukselle**, hintaa, joka syötetään, kun kulumerkintä luodaan, käytetään kustannukselle ja myyntikirjauskansion rivi lasketaan hinnoittelutavan perusteella.</span><span class="sxs-lookup"><span data-stu-id="b94cf-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="b94cf-134">Voit lisätä kulumerkintään mukautetun kentän.</span><span class="sxs-lookup"><span data-stu-id="b94cf-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="b94cf-135">Jos haluat, että kentän arvo välitettään toteutuneisiin arvoihin, luo kenttä **Toteutuneet**- ja **Kirjausrivi**-taulukoihin.</span><span class="sxs-lookup"><span data-stu-id="b94cf-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="b94cf-136">Käytä mukautettua koodia, kun haluat välittää valitun kentän arvon ajan syötöstä toteutuneisiin arvoihin kirjausrivin kautta käyttämällä tapahtumien alkuperää.</span><span class="sxs-lookup"><span data-stu-id="b94cf-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="b94cf-137">Lisätietoja tapahtumien alkuperästä ja yhteyksistä on ohjeaiheessa [Toteutuneidenarvojen linkittäminen alkuperäisiin tietueisiin](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="b94cf-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="b94cf-138">Kirjauskansion rivien ja materiaalin käyttölokien lähettäminen</span><span class="sxs-lookup"><span data-stu-id="b94cf-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="b94cf-139">Lisätietoja kulumerkinnästä on kohdassa [Materiaalin käyttöloki](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="b94cf-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b94cf-140">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="b94cf-140">Time and materials</span></span>

<span data-ttu-id="b94cf-141">Kun lähetetty materiaalin käyttölokin kirjaus linkitetään projektiin, joka on yhdistetty ajan ja materiaalien sopimusriviin, järjestelmä luo kaksi kirjauskansion riviä, yhden kustannuksille ja toisen laskuttamattomalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="b94cf-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b94cf-142">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="b94cf-142">Fixed price</span></span>

<span data-ttu-id="b94cf-143">Kun lähetetty materiaalin käyttölokin kirjaus on linkitetty projektiin, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo yhden kirjauskansion rivin kustannusta varten.</span><span class="sxs-lookup"><span data-stu-id="b94cf-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b94cf-144">Oletushinnoittelu</span><span class="sxs-lookup"><span data-stu-id="b94cf-144">Default pricing</span></span>

<span data-ttu-id="b94cf-145">Materiaalin oletushintojen syöttämisen logiikka perustuu tuotteen ja yksikön yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="b94cf-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="b94cf-146">Sopivan hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="b94cf-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="b94cf-147">Oletushintoihin vaikuttavia kenttiä, kuten **Tuotetunnus** ja **Yksikkö** käytetään kirjauskansion rivin sopivan hinnan määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="b94cf-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="b94cf-148">Tämä koskee kuitenkin vain luettelotuotteita.</span><span class="sxs-lookup"><span data-stu-id="b94cf-148">However, this only works for catalog products.</span></span> <span data-ttu-id="b94cf-149">Lisätyille tuotteille hintaa, joka syötetään, kun materiaalin käyttölokin kirjaus luodaan, käytetään kustannuksen ja myyntihinnan kirjauskansioriveillä.</span><span class="sxs-lookup"><span data-stu-id="b94cf-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="b94cf-150">Voit lisätä **materiaalin käyttölokin** kirjaukseen mukautetun kentän.</span><span class="sxs-lookup"><span data-stu-id="b94cf-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="b94cf-151">Jos haluat, että kentän arvo välitettään toteutuneisiin arvoihin, luo kenttä **Toteutuneet**- ja **Kirjausrivi**-taulukoihin.</span><span class="sxs-lookup"><span data-stu-id="b94cf-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="b94cf-152">Käytä mukautettua koodia, kun haluat välittää valitun kentän arvon ajan syötöstä toteutuneisiin arvoihin kirjausrivin kautta käyttämällä tapahtumien alkuperää.</span><span class="sxs-lookup"><span data-stu-id="b94cf-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="b94cf-153">Lisätietoja tapahtumien alkuperästä ja yhteyksistä on ohjeaiheessa [Toteutuneidenarvojen linkittäminen alkuperäisiin tietueisiin](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="b94cf-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="b94cf-154">Tapahtumakirjauskansioiden käyttö kustannusten tallentamiseen</span><span class="sxs-lookup"><span data-stu-id="b94cf-154">Use entry journals to record costs</span></span>

<span data-ttu-id="b94cf-155">Tapahtumakirjauskansioihin voit tallentaa kustannuksia tai tuottoja luokkiin materiaali, maksu, kulu ja verotapahtuma.</span><span class="sxs-lookup"><span data-stu-id="b94cf-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="b94cf-156">Kirjauskansioita voi käyttää seuraaviin tarkoituksiin:</span><span class="sxs-lookup"><span data-stu-id="b94cf-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="b94cf-157">Siirrä tapahtumien todelliset arvot toisesta järjestelmästä Microsoft Dynamics 365 Project Operations -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="b94cf-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="b94cf-158">Tallenna kustannukset, jotka tapahtuivat toisessa järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="b94cf-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="b94cf-159">Nämä kustannukset voivat sisältää hankinta- tai alihankintakustannuksia.</span><span class="sxs-lookup"><span data-stu-id="b94cf-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b94cf-160">Sovellus ei tarkista päiväkirjan rivin tyyppiä tai siihen liittyvää hinnoittelua, joka on syötetty päiväkirjan riville.</span><span class="sxs-lookup"><span data-stu-id="b94cf-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="b94cf-161">Siksi vain käyttäjä, joka on täysin tietoinen todellisten arvojen kirjanpidollisesta vaikutuksesta projekteihin, voi käyttää tapahtumakirjauskansioita todellisten arvojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="b94cf-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="b94cf-162">Tämän kirjauskansiotyypin vaikutuksen vuoksi sinun on valittava huolellisesti, kenellä on oikeus luoda tapahtumakirjauskansioita.</span><span class="sxs-lookup"><span data-stu-id="b94cf-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="b94cf-163">Todellisten arvojen tallentaminen projektitapahtumien perusteella</span><span class="sxs-lookup"><span data-stu-id="b94cf-163">Record actuals based on project events</span></span>

<span data-ttu-id="b94cf-164">Project Operations tallentaa projektin aikana esiintyvät taloudelliset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b94cf-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="b94cf-165">Nämä tapahtumat kirjataan muodossa Todelliset arvot.</span><span class="sxs-lookup"><span data-stu-id="b94cf-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="b94cf-166">Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.</span><span class="sxs-lookup"><span data-stu-id="b94cf-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="b94cf-167">Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö</span><span class="sxs-lookup"><span data-stu-id="b94cf-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b94cf-168">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="b94cf-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b94cf-169">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="b94cf-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b94cf-170">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="b94cf-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b94cf-171">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="b94cf-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b94cf-172">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="b94cf-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b94cf-173">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="b94cf-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b94cf-174">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="b94cf-174">Actuals</span></span></th>
<th><span data-ttu-id="b94cf-175">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-175">Transaction currency</span></span></th>
<th><span data-ttu-id="b94cf-176">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="b94cf-176">Fixed price</span></span></th>
<th><span data-ttu-id="b94cf-177">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b94cf-178">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="b94cf-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b94cf-179">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-180">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="b94cf-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b94cf-181">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b94cf-182">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="b94cf-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b94cf-183">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-183">Cost actual</span></span></td>
<td><span data-ttu-id="b94cf-184">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-185">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-186">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="b94cf-187">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-188">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-189">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="b94cf-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b94cf-190">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b94cf-191">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="b94cf-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b94cf-192">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-192">Cost actual</span></span></td>
<td><span data-ttu-id="b94cf-193">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-194">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-195">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-196">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-197">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-198">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="b94cf-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b94cf-199">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-200">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="b94cf-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b94cf-201">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b94cf-202">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="b94cf-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b94cf-203">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b94cf-204">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-205">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-206">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-207">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-208">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-209">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-209">Billed sales</span></span></td>
<td><span data-ttu-id="b94cf-210">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b94cf-211">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="b94cf-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b94cf-212">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b94cf-213">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-214">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-215">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-216">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-217">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-218">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="b94cf-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b94cf-219">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-220">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="b94cf-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b94cf-221">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b94cf-222">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="b94cf-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b94cf-223">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b94cf-224">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b94cf-225">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b94cf-226">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="b94cf-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b94cf-227">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-228">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-229">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-230">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-230">Billed sales</span></span></td>
<td><span data-ttu-id="b94cf-231">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b94cf-232">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="b94cf-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b94cf-233">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b94cf-234">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-235">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b94cf-236">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-237">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="b94cf-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b94cf-238">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="b94cf-239">Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön</span><span class="sxs-lookup"><span data-stu-id="b94cf-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b94cf-240">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="b94cf-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b94cf-241">Laskutettava tai myyty projekti</span><span class="sxs-lookup"><span data-stu-id="b94cf-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b94cf-242">Projekti myyntiä edeltävässä vaiheessa</span><span class="sxs-lookup"><span data-stu-id="b94cf-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b94cf-243">Sisäinen projekti</span><span class="sxs-lookup"><span data-stu-id="b94cf-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b94cf-244">Aika ja materiaalit</span><span class="sxs-lookup"><span data-stu-id="b94cf-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b94cf-245">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="b94cf-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b94cf-246">Todelliset arvot</span><span class="sxs-lookup"><span data-stu-id="b94cf-246">Actuals</span></span></th>
<th><span data-ttu-id="b94cf-247">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-247">Transaction currency</span></span></th>
<th><span data-ttu-id="b94cf-248">Kiinteähintainen</span><span class="sxs-lookup"><span data-stu-id="b94cf-248">Fixed price</span></span></th>
<th><span data-ttu-id="b94cf-249">Tapahtumavaluutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b94cf-250">Aikamerkintä luodaan.</span><span class="sxs-lookup"><span data-stu-id="b94cf-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b94cf-251">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-252">Aikamerkintä lähetetään.</span><span class="sxs-lookup"><span data-stu-id="b94cf-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b94cf-253">Ei toimintaa Todelliset arvot -entiteetissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b94cf-254">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="b94cf-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b94cf-255">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-255">Cost actual</span></span></td>
<td><span data-ttu-id="b94cf-256">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b94cf-257">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b94cf-258">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b94cf-259">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b94cf-260">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-261">Laskuttamattoman myynnin todellinen arvo – laskutettava</span><span class="sxs-lookup"><span data-stu-id="b94cf-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b94cf-262">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-263">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="b94cf-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b94cf-264">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-265">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b94cf-266">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b94cf-267">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</span><span class="sxs-lookup"><span data-stu-id="b94cf-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b94cf-268">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-268">Cost actual</span></span></td>
<td><span data-ttu-id="b94cf-269">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-270">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-271">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-272">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-273">Kulujen todellinen arvo</span><span class="sxs-lookup"><span data-stu-id="b94cf-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-274">Resursointiyksikön kustannus</span><span class="sxs-lookup"><span data-stu-id="b94cf-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b94cf-275">Resursointiyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-276">Organisaatioiden välinen myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b94cf-277">Sopimusyksikön valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-278">Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="b94cf-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b94cf-279">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-280">Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="b94cf-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b94cf-281">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b94cf-282">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</span><span class="sxs-lookup"><span data-stu-id="b94cf-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b94cf-283">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b94cf-284">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-285">Välitavoitteen laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-286">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-287">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b94cf-288">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-289">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-289">Billed sales</span></span></td>
<td><span data-ttu-id="b94cf-290">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b94cf-291">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</span><span class="sxs-lookup"><span data-stu-id="b94cf-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b94cf-292">Laskuttamattoman myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b94cf-293">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-294">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-295">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-296">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b94cf-297">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-298">Laskutettu myynti – laskutetaan uuden määrän perusteella</span><span class="sxs-lookup"><span data-stu-id="b94cf-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b94cf-299">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-300">Laskutettu myynti – erotusta ei laskuteta</span><span class="sxs-lookup"><span data-stu-id="b94cf-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b94cf-301">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b94cf-302">Laskua korjataan laskutettavan summan suurentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="b94cf-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b94cf-303">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b94cf-304">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b94cf-305">Välitavoitteen laskutetun myynnin palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b94cf-306">Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></span><span class="sxs-lookup"><span data-stu-id="b94cf-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b94cf-307">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-308">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b94cf-309">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="b94cf-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-310">Laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-310">Billed sales</span></span></td>
<td><span data-ttu-id="b94cf-311">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b94cf-312">Laskua korjataan laskutettavan summan pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="b94cf-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b94cf-313">Laskutettu myynti – palautus</span><span class="sxs-lookup"><span data-stu-id="b94cf-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b94cf-314">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-315">Uuden määrän laskutettu myynti</span><span class="sxs-lookup"><span data-stu-id="b94cf-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b94cf-316">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b94cf-317">Laskuttamaton myynti – erotus laskutetaan</span><span class="sxs-lookup"><span data-stu-id="b94cf-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b94cf-318">Projektisopimuksen valuutta</span><span class="sxs-lookup"><span data-stu-id="b94cf-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
