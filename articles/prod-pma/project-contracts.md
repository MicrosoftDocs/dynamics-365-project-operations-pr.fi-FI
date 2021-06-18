---
title: Projektisopimukset
description: Tässä aiheessa on esimerkkejä projektisopimuksista, joita voi luoda erityyppisille projekteille ja rahoituslähteille, sekä siitä, miten voit hallita palvelusopimuksia ja laskuttaa projektiasiakkaita.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999757"
---
# <a name="project-contracts"></a><span data-ttu-id="b4b67-103">Projektisopimukset</span><span class="sxs-lookup"><span data-stu-id="b4b67-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4b67-104">Tässä artikkelissa on esimerkkejä projektisopimuksista, joita voi luoda erityyppisille projekteille ja rahoituslähteille, sekä siitä, miten voit hallita palvelusopimuksia ja laskuttaa projektiasiakkaita.</span><span class="sxs-lookup"><span data-stu-id="b4b67-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="b4b67-105">Projektisopimukselle luotavan projektin tyyppi määrittää menetelmän, jota käytetään projektiasiakkaiden laskutukseen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="b4b67-106">Voit muuttaa projektisopimusta ja siihen liittyvää projektia, mutta et voi muuttaa projektityyppiä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="b4b67-107">Projektisopimuksen avulla voit laskuttaa yhtä tai useampaa projektia samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="b4b67-108">Projektisopimus auttaa myös takaamaan yhdenmukaisen laskutusmenettelyn jokaiselle projektirakenteen aliprojektille.</span><span class="sxs-lookup"><span data-stu-id="b4b67-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="b4b67-109">Kaikki laskutettavat projektit on liitettävä projektisopimukseen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="b4b67-110">Projektisopimuksen asetukset koskevat kaikkia kyseiseen projektisopimukseen liittyviä projekteja ja aliprojekteja.</span><span class="sxs-lookup"><span data-stu-id="b4b67-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="b4b67-111">Projektisopimuksessa voi määrittää yhden tai useamman rahoituslähteen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="b4b67-112">Siksi voit jakaa laskutuksen useiden rahoittajien kesken, määrittää rahoitusrajat siten, että rahoituslähteitä ei laskuteta enempää kuin määritetty summa, ja määrittää kulujen maksujen rahoitussäännöt.</span><span class="sxs-lookup"><span data-stu-id="b4b67-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="b4b67-113">Projektisopimusten rahoitus</span><span class="sxs-lookup"><span data-stu-id="b4b67-113">Funding for project contracts</span></span>
<span data-ttu-id="b4b67-114">Jotkin projektisopimukset määrittävät, että useat osapuolet jakavat vastuun projektikustannusten rahoittamisesta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="b4b67-115">Seuraavassa on joitakin esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-115">Here are some examples:</span></span>

-   <span data-ttu-id="b4b67-116">Suuri asiakas, jolla on useita osastoja, pyytää, että projektin rahoittaminen jaetaan osaston mukaan.</span><span class="sxs-lookup"><span data-stu-id="b4b67-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="b4b67-117">Yritys jakaa suuren projektin kustannukset ulkoisen organisaation kanssa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="b4b67-118">Tiehanketta rahoittaa kaksi kuntaa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="b4b67-119">Siltaprojektia rahoittaa julkinen avustus ja yksityinen yritys.</span><span class="sxs-lookup"><span data-stu-id="b4b67-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="b4b67-120">Dynamics 365 Financessa voit jakaa yksittäisen tapahtuman tai koko projektin laskutuksen useiden asiakkaiden, apurahojen tai organisaatioiden kesken.</span><span class="sxs-lookup"><span data-stu-id="b4b67-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="b4b67-121">Projekteissa, joissa on useita rahoittajia, kaikkia edistyneen rahoitusprojektin rahoittamiseen osallistuvia osapuolia kutsutaan rahoituslähteiksi.</span><span class="sxs-lookup"><span data-stu-id="b4b67-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="b4b67-122">Kun asiakas, organisaatio tai apuraha on määritetty rahoituslähteeksi, se voidaan delegoida yhteen tai useampaan rahoitussääntöön.</span><span class="sxs-lookup"><span data-stu-id="b4b67-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="b4b67-123">Rahoitussäännöt sisältävät ehdot, jotka määrittävät, miten maksut kohdistetaan projektin eri rahoituslähteisiin.</span><span class="sxs-lookup"><span data-stu-id="b4b67-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="b4b67-124">Koska esimerkiksi ostoehdotuksissa ja ostotilauksissa näkyviä varastonimikkeitä ei voi jakaa, kustannusten määrää ei voi jakaa useiden rahoituslähteiden kesken jakelun aikana.</span><span class="sxs-lookup"><span data-stu-id="b4b67-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="b4b67-125">Tämän vuoksi rahoituslähteen arvo on 0 (nolla), kunnes varasto-ongelma on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="b4b67-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="b4b67-126">Kun varastokysymys kirjataan, kustannusten summa jaetaan projektin tilin jakelusääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b4b67-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="b4b67-127">Seuraavassa on joitakin vaiheita, joilla voit helpottaa laskutuksen jakamista useiden rahoituslähteiden kesken:</span><span class="sxs-lookup"><span data-stu-id="b4b67-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="b4b67-128">Määritä, että kaikki projektiin lisätyt tapahtumat käyttävät samaa myyntivaluuttaa kuin projektisopimus.</span><span class="sxs-lookup"><span data-stu-id="b4b67-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="b4b67-129">Määritä rahoitusrajat, jotta rahoituslähdettä ei laskuteta enempää kuin määritetty summa projektia kohti.</span><span class="sxs-lookup"><span data-stu-id="b4b67-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="b4b67-130">Määritä rahoitussäännöt ja rahoitusrajat kullekin työntekijälle, nimikkeelle, luokalle, luokkaryhmälle ja tapahtumatyypille (tai kaikille tapahtumatyypeille).</span><span class="sxs-lookup"><span data-stu-id="b4b67-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="b4b67-131">Valitse valinnaiset alkamis- ja päättymispäivämäärät, kun haluat määrittää ajanjakson, jolloin kukin rahoitussääntö on voimassa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="b4b67-132">Määritä prosenttiosuus, josta kukin rahoituslähde on vastuussa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="b4b67-133">Määritä, mikä rahoituslähde on vastuussa rahoituksen kohdistuslaskelmien aiheuttamista pyöristyseroista.</span><span class="sxs-lookup"><span data-stu-id="b4b67-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="b4b67-134">Määritä säännöt, jotka määrittävät, miten projektin kustannukset laskutetaan ulkoisilta asiakkailta ja veloitetaan sisäisistä organisaatioista.</span><span class="sxs-lookup"><span data-stu-id="b4b67-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="b4b67-135">Voit kirjata tapahtumia pidossa olevaan rahoitustiliin, kunnes saat lisärahoitusta tai päätät maksaa kustannukset sisäisesti.</span><span class="sxs-lookup"><span data-stu-id="b4b67-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="b4b67-136">Voit määrittää tapahtumaan liitettävän veroryhmän, kun projektia haetaan veroryhmämääritykseksi.</span><span class="sxs-lookup"><span data-stu-id="b4b67-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="b4b67-137">Jos veroryhmämääritystä ei ole tehty projektitasolla, projektisopimusta haetaan.</span><span class="sxs-lookup"><span data-stu-id="b4b67-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="b4b67-138">Esimerkki: useita rahoituslähteitä (yksinkertainen)</span><span class="sxs-lookup"><span data-stu-id="b4b67-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="b4b67-139">Seuraavassa taulukossa on esitetty skenaarioita, joissa hallitaan rahoituksen jakamista useiden rahoituslähteiden kesken.</span><span class="sxs-lookup"><span data-stu-id="b4b67-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="b4b67-140">Nämä skenaariot perustuvat seuraaviin oletuksiin:</span><span class="sxs-lookup"><span data-stu-id="b4b67-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="b4b67-141">Prioriteettiasetukset otetaan huomioon varojen kohdentamisessa, ennen kuin muita rahoitussäännön ehtoja käytetään.</span><span class="sxs-lookup"><span data-stu-id="b4b67-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="b4b67-142">Kauden d määrittämiseen ei ole määritetty päivämääräaluetta, kun rahoitussääntö on voimassa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4b67-143"><strong>Skenaario</strong></span><span class="sxs-lookup"><span data-stu-id="b4b67-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="b4b67-144"><strong>Rahoituslähde</strong></span><span class="sxs-lookup"><span data-stu-id="b4b67-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="b4b67-145"><strong>Kohdistusprosentti</strong></span><span class="sxs-lookup"><span data-stu-id="b4b67-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="b4b67-146"><strong>Kohdistuksen prioriteetti</strong></span><span class="sxs-lookup"><span data-stu-id="b4b67-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b67-147">Jos haluat kohdistaa kustannukset yhteen rahoituslähteeseen, kunnes sen varat ovat loppuneet, kohdista kustannukset toiseen rahoituslähteeseen, kunnes sen varat ovat loppuneet, ja varaa lopuksi loput kustannukset kolmannelle rahoituslähteelle.</span><span class="sxs-lookup"><span data-stu-id="b4b67-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4b67-148">Rahoituslähde　1</span><span class="sxs-lookup"><span data-stu-id="b4b67-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4b67-149">Rahoituslähde　2</span><span class="sxs-lookup"><span data-stu-id="b4b67-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="b4b67-150">Rahoituslähde　3</span><span class="sxs-lookup"><span data-stu-id="b4b67-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-151">100%</span><span class="sxs-lookup"><span data-stu-id="b4b67-151">100%</span></span></li>
<li><span data-ttu-id="b4b67-152">100%</span><span class="sxs-lookup"><span data-stu-id="b4b67-152">100%</span></span></li>
<li><span data-ttu-id="b4b67-153">100%</span><span class="sxs-lookup"><span data-stu-id="b4b67-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-154">1</span><span class="sxs-lookup"><span data-stu-id="b4b67-154">1</span></span></li>
<li><span data-ttu-id="b4b67-155">2</span><span class="sxs-lookup"><span data-stu-id="b4b67-155">2</span></span></li>
<li><span data-ttu-id="b4b67-156">3</span><span class="sxs-lookup"><span data-stu-id="b4b67-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4b67-157">Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b4b67-158">Kun jompikumpi näistä rahoituslähteistä on täyttynyt, haluat maksaa jäljellä olevat kustannukset kolmannesta rahoituslähteestä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4b67-159">Rahoituslähde　1</span><span class="sxs-lookup"><span data-stu-id="b4b67-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4b67-160">Rahoituslähde　2</span><span class="sxs-lookup"><span data-stu-id="b4b67-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="b4b67-161">Rahoituslähde　3</span><span class="sxs-lookup"><span data-stu-id="b4b67-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-162">75 %</span><span class="sxs-lookup"><span data-stu-id="b4b67-162">75%</span></span></li>
<li><span data-ttu-id="b4b67-163">25 %</span><span class="sxs-lookup"><span data-stu-id="b4b67-163">25%</span></span></li>
<li><span data-ttu-id="b4b67-164">100%</span><span class="sxs-lookup"><span data-stu-id="b4b67-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-165">1</span><span class="sxs-lookup"><span data-stu-id="b4b67-165">1</span></span></li>
<li><span data-ttu-id="b4b67-166">1</span><span class="sxs-lookup"><span data-stu-id="b4b67-166">1</span></span></li>
<li><span data-ttu-id="b4b67-167">2</span><span class="sxs-lookup"><span data-stu-id="b4b67-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b67-168">Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b4b67-169">Kun jompikumpi näistä rahoituslähteistä on täyttynyt, haluat jakaa jäljellä olevat kustannukset kolmannen rahoituslähteen ja neljännen rahoituslähteen välillä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4b67-170">Rahoituslähde　1</span><span class="sxs-lookup"><span data-stu-id="b4b67-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4b67-171">Rahoituslähde　2</span><span class="sxs-lookup"><span data-stu-id="b4b67-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="b4b67-172">Rahoituslähde　3</span><span class="sxs-lookup"><span data-stu-id="b4b67-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="b4b67-173">Rahoituslähde　4</span><span class="sxs-lookup"><span data-stu-id="b4b67-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-174">75 %</span><span class="sxs-lookup"><span data-stu-id="b4b67-174">75%</span></span></li>
<li><span data-ttu-id="b4b67-175">25 %</span><span class="sxs-lookup"><span data-stu-id="b4b67-175">25%</span></span></li>
<li><span data-ttu-id="b4b67-176">50 %</span><span class="sxs-lookup"><span data-stu-id="b4b67-176">50%</span></span></li>
<li><span data-ttu-id="b4b67-177">50 %</span><span class="sxs-lookup"><span data-stu-id="b4b67-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-178">1</span><span class="sxs-lookup"><span data-stu-id="b4b67-178">1</span></span></li>
<li><span data-ttu-id="b4b67-179">1</span><span class="sxs-lookup"><span data-stu-id="b4b67-179">1</span></span></li>
<li><span data-ttu-id="b4b67-180">2</span><span class="sxs-lookup"><span data-stu-id="b4b67-180">2</span></span></li>
<li><span data-ttu-id="b4b67-181">2</span><span class="sxs-lookup"><span data-stu-id="b4b67-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4b67-182">Haluat kohdistaa ensimmäiset 25 prosenttia kustannuksista yhteen rahoituslähteeseen ja loput toiseen rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4b67-183">Rahoituslähde　1</span><span class="sxs-lookup"><span data-stu-id="b4b67-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4b67-184">Rahoituslähde　2</span><span class="sxs-lookup"><span data-stu-id="b4b67-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-185">25 %</span><span class="sxs-lookup"><span data-stu-id="b4b67-185">25%</span></span></li>
<li><span data-ttu-id="b4b67-186">100%</span><span class="sxs-lookup"><span data-stu-id="b4b67-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4b67-187">1</span><span class="sxs-lookup"><span data-stu-id="b4b67-187">1</span></span></li>
<li><span data-ttu-id="b4b67-188">2</span><span class="sxs-lookup"><span data-stu-id="b4b67-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="b4b67-189">Esimerkki: useita rahoituslähteitä (monimutkainen)</span><span class="sxs-lookup"><span data-stu-id="b4b67-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="b4b67-190">Käytössäsi on kolme rahoituslähdettä, joita haluat käyttää seuraavassa tilauksessa:</span><span class="sxs-lookup"><span data-stu-id="b4b67-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="b4b67-191">Käytä rahoituslähdettä 2 ja rahoituslähdettä 3 samalla tavalla, kunnes rahoituslähde 2 on täyttynyt.</span><span class="sxs-lookup"><span data-stu-id="b4b67-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="b4b67-192">Käytä edelleen rahoituslähdettä 3, kunnes se on käytetty loppuun.</span><span class="sxs-lookup"><span data-stu-id="b4b67-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="b4b67-193">Käytä rahoituslähdettä 1, kun rahoituslähde 3 on täyttynyt.</span><span class="sxs-lookup"><span data-stu-id="b4b67-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="b4b67-194">Tämän tavoitteen saavuttamiseksi sinun on toimittava seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b4b67-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="b4b67-195">Määritä rahoituslähteen 2 ja rahoituslähteen 3 rahoitusrajat niiden summien osalta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="b4b67-196">Luo seuraavat rahoitussäännöt:</span><span class="sxs-lookup"><span data-stu-id="b4b67-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="b4b67-197">Sääntö 1 (prioriteetti 1): kohdistaa 50 prosenttia tapahtumista rahoituslähteeseen 2 ja 50 prosenttia rahoituslähteeseen 3.</span><span class="sxs-lookup"><span data-stu-id="b4b67-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="b4b67-198">Sääntö 2 (prioriteetti 2): Varaa 100 prosenttia tapahtumista, jotka rahoitetaan lähteestä 3.</span><span class="sxs-lookup"><span data-stu-id="b4b67-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="b4b67-199">Sääntö 3 (prioriteetti 3): Varaa 100 prosenttia tapahtumista, jotka rahoitetaan lähteestä 1.</span><span class="sxs-lookup"><span data-stu-id="b4b67-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="b4b67-200">Tämä asetus toimii, koska tapahtumia verrataan sääntöihin ja rajoituksiin ja määritetään, koskeeko jokin niistä tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="b4b67-201">Jos tapahtumalle ei ole erityisiä sääntöjä tai rajoituksia, käytetään Kaikki tapahtumat -sääntöä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="b4b67-202">Kaikki tapahtumat -sääntö vastaa kaikkia tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="b4b67-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="b4b67-203">Jos löytyi sääntö, joka vastaa jotakin tapahtumaa, säännössä määritettyä prosenttiosuutta käytetään ensin, mutta vasta kun vastaavat arvot on tarkistettu.</span><span class="sxs-lookup"><span data-stu-id="b4b67-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="b4b67-204">Jos rajoitus on täyttynyt ja rahoituslähteen varat ovat loppuneet, rahoitusrajaan liittyvä rahoitussääntö jätetään huomiotta ja ohjelma tarkistaa seuraavan säännön.</span><span class="sxs-lookup"><span data-stu-id="b4b67-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="b4b67-205">Joissakin tapauksissa vain osa tapahtumasta voidaan kohdistaa sääntöön.</span><span class="sxs-lookup"><span data-stu-id="b4b67-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="b4b67-206">Tämä voi johtua siitä, että tapahtuman kohdistuksena saavutetaan raja.</span><span class="sxs-lookup"><span data-stu-id="b4b67-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="b4b67-207">Tässä tapauksessa vain tietty summa kohdistetaan kyseisen säännön mukaan, kuten 50 prosenttia kuhunkin rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="b4b67-208">Tämä koskee sääntöä 1, joka on kuvattu aiemmin tässä osassa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="b4b67-209">Loppuosa kohdistetaan järjestyksessä seuraavan säännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="b4b67-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="b4b67-210">Seuraavassa taulukossa tutkitaan yksityiskohtaisesti skenaariota.</span><span class="sxs-lookup"><span data-stu-id="b4b67-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4b67-211"><strong>Kohdistus</strong></span><span class="sxs-lookup"><span data-stu-id="b4b67-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="b4b67-212"><strong>Tiedot</strong></span><span class="sxs-lookup"><span data-stu-id="b4b67-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b67-213">Rahoitussäännöt</span><span class="sxs-lookup"><span data-stu-id="b4b67-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="b4b67-214">Sääntö 1 (prioriteetti 1): kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b4b67-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="b4b67-215">Kohdista rahoituslähteelle 2 50 % ja rahoituslähteelle 3 50 %.</span><span class="sxs-lookup"><span data-stu-id="b4b67-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="b4b67-216">Sääntö 2 (prioriteetti 2): kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b4b67-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="b4b67-217">Kohdista rahoituslähteelle 3 100 %.</span><span class="sxs-lookup"><span data-stu-id="b4b67-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="b4b67-218">Sääntö 3 (prioriteetti 2): kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b4b67-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="b4b67-219">Kohdista rahoituslähteelle 1 100 %.</span><span class="sxs-lookup"><span data-stu-id="b4b67-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4b67-220">Rahoitusrajat</span><span class="sxs-lookup"><span data-stu-id="b4b67-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="b4b67-221">Rahoituslähde 1 raja = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="b4b67-222">Rahoituslähde 2 raja = 500,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="b4b67-223">Rahoituslähde 3 raja = 750,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b67-224">Tapahtuma 1</span><span class="sxs-lookup"><span data-stu-id="b4b67-224">Transaction 1</span></span></td>
<td><span data-ttu-id="b4b67-225"><strong>Tapahtumamäärä:</strong> 100,00<strong>Rahoitus:</strong> Tapahtuma maksetaan vain säännön 1 mukaisesti, koska tapahtuma on kokonaan maksettu sen jälkeen, kun sääntö 1 on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b4b67-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="b4b67-226">Tapahtuma rahoitetaan tasapuolisesti rahoituslähteen 2 ja rahoituslähteen 3 välillä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="b4b67-227">Rahoituslähde 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="b4b67-228">Rahoituslähde 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4b67-229">Tapahtuma 2</span><span class="sxs-lookup"><span data-stu-id="b4b67-229">Transaction 2</span></span></td>
<td><span data-ttu-id="b4b67-230"><strong>Tapahtumamäärä:</strong>5 000,00<strong>Rahoitus:</strong> Tapahtuma maksetaan kaikkien kolmen säännön mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b4b67-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="b4b67-231"><strong>Sääntö 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="b4b67-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="b4b67-232">Rahoituslähde 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="b4b67-233">Rahoituslähde 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="b4b67-234">
<strong>Sääntö 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="b4b67-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="b4b67-235">Rahoituslähde 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="b4b67-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="b4b67-236">
<strong>Sääntö 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="b4b67-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="b4b67-237">Rahoituslähde1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="b4b67-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b67-238">Kullekin rahoituslähteelle jaetut varat yhteensä</span><span class="sxs-lookup"><span data-stu-id="b4b67-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="b4b67-239">Rahoituslähde 1: 3 850,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="b4b67-240">Rahoituslähde 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="b4b67-241">Rahoituslähde 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="b4b67-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="b4b67-242">Laskutussäännöt</span><span class="sxs-lookup"><span data-stu-id="b4b67-242">Billing rules</span></span>
<span data-ttu-id="b4b67-243">Kun neuvottelemme projektisopimuksesta asiakkaan kanssa, voit määrittää, miten ja milloin voit laskuttaa asiakasta projektin töistä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="b4b67-244">Kun olet määrittänyt projektisopimuksen ja projektin, voit määrittää projektille laskutussäännöt.</span><span class="sxs-lookup"><span data-stu-id="b4b67-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="b4b67-245">Laskutussäännöt perustuvat projektisopimuksessa määritettyihin projektin ehtoihin.</span><span class="sxs-lookup"><span data-stu-id="b4b67-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="b4b67-246">Luotettavat laskutussäännöt määräytyvät sen mukaan, mitkä projektisopimuksen ehdot ja projektityyppi, kuten aika ja materiaali tai kiinteämääräinen hinta, liitetään laskutussääntöön.</span><span class="sxs-lookup"><span data-stu-id="b4b67-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="b4b67-247">Voit luoda projektisopimukselle useamman kuin yhden laskutussäännön.</span><span class="sxs-lookup"><span data-stu-id="b4b67-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="b4b67-248">Voit myös delegoida laskutussäännön useisiin projekteihin, jotka liittyvät samaan projektisopimukseen ja joilla on samankaltaiset laskutusehdot.</span><span class="sxs-lookup"><span data-stu-id="b4b67-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="b4b67-249">Voit määrittää seuraavan tyyppisiä laskutussääntöjä:</span><span class="sxs-lookup"><span data-stu-id="b4b67-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="b4b67-250">**Toimitusyksikkö** – Laskuta asiakasta, kun toimitusyksikkö on valmis.</span><span class="sxs-lookup"><span data-stu-id="b4b67-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="b4b67-251">Palvelusopimuksessa määritetään toimitusyksiköt.</span><span class="sxs-lookup"><span data-stu-id="b4b67-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="b4b67-252">**Edistyminen** – Laskuta asiakasta, kun olet suorittanut määritetyn prosenttiosuuden projektista.</span><span class="sxs-lookup"><span data-stu-id="b4b67-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="b4b67-253">Voit määrittää laskutussäännön, joka laskee automaattisesti valmiin työn prosenttiosuuden, tai voit laskea valmiin työn prosenttimäärän ja asiakkaan laskutettavan summan manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="b4b67-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="b4b67-254">**Välitavoite** – Laskuta asiakasta projektin välitavoitteen koko määrästä, kun välitavoite saavutetaan.</span><span class="sxs-lookup"><span data-stu-id="b4b67-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="b4b67-255">**Maksu**: Laskuta palveluistasi asiakas- ja hallinnointipalkkio, joka on yleensä prosenttiosuus palvelujen kustannuksista.</span><span class="sxs-lookup"><span data-stu-id="b4b67-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="b4b67-256">**Aika ja materiaali** – Laskuta asiakasta projektissa käytettävän ajan ja materiaalin arvosta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="b4b67-257">Voit määrittää kaikentyyppisille laskutussäännöille säilytysprosentin, joka vähennetään asiakaslaskuista, kunnes projekti saavuttaa sovitun vaiheen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="b4b67-258">Maksun säilytysprosentti määritetään projektisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="b4b67-259">Summa lasketaan myyntilaskun rivien yhteisarvon perusteella ja vähennetään siitä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="b4b67-260">**Ajan ja materiaalin** sekä **Edistymisen** laskutussääntöjen avulla voit määrittää laskutettavia luokkia.</span><span class="sxs-lookup"><span data-stu-id="b4b67-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="b4b67-261">Laskutettavat luokat ilmaisevat tapahtumat, jotka tulisi sisällyttää myyntilaskuihin.</span><span class="sxs-lookup"><span data-stu-id="b4b67-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="b4b67-262">Kun olet valmis laskuttamaan asiakasta, projektin laskutettava summa lasketaan laskutussääntöjen perusteella, ja projektin laskuehdotus luodaan.</span><span class="sxs-lookup"><span data-stu-id="b4b67-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="b4b67-263">Seuraavissa osissa on esimerkkejä siitä, miten projektin laskutussääntöjä määritetään ja hallitaan.</span><span class="sxs-lookup"><span data-stu-id="b4b67-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="b4b67-264">Esimerkki: Luo laskutussääntö, joka perustuu toimitettujen yksiköiden määrään</span><span class="sxs-lookup"><span data-stu-id="b4b67-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="b4b67-265">Organisaatiosi tekee sopimuksen, jonka mukaan asiakkaan työntekijöillä on yhteensä viisi koulutustilaisuutta, joiden kustannus on 10 000 per koulutusjakso.</span><span class="sxs-lookup"><span data-stu-id="b4b67-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="b4b67-266">Laskutat asiakasta jokaisen koulutusjakson jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b4b67-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="b4b67-267">Kun määrität palvelusopimuksen laskutussäännöt, käytä seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="b4b67-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="b4b67-268">Toimitusyksikkö on yksi koulutusjakso.</span><span class="sxs-lookup"><span data-stu-id="b4b67-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="b4b67-269">Yksikköhinta on 10 000 koulutusjaksoa kohti.</span><span class="sxs-lookup"><span data-stu-id="b4b67-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="b4b67-270">Yksiköiden kokonaismäärä on viisi koulutustilaisuutta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="b4b67-271">Kun olet suorittanut yhden koulutusjakson, voit luoda 10 000 laskun ensimmäisestä toimitetusta yksiköstä ja lähettää laskun asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="b4b67-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="b4b67-272">Esimerkki: sellaisen laskutussäännön luominen, joka perustuu tiettyyn prosenttiosuuteen projektin valmistumisesta (manuaalisesta laskennasta)</span><span class="sxs-lookup"><span data-stu-id="b4b67-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="b4b67-273">Organisaatiosi, ohjelmistokonsultointiyritys, tekee asiakkaan kanssa sopimuksen, joka kehittää tuotteen osan, jota asiakas kehittää.</span><span class="sxs-lookup"><span data-stu-id="b4b67-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="b4b67-274">Organisaatiosi suostuu toimittamaan ohjelmistokoodin kuuden kuukauden aikana.</span><span class="sxs-lookup"><span data-stu-id="b4b67-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="b4b67-275">Asiakas sitoutuu maksamaan organisaatiollesi yhteensä 100 000 työn hinnasta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="b4b67-276">Voit luoda laskutussäännön, joka laskuttaa asiakasta sopimuksessa määritetyn työn valmistumisprosentin perusteella.</span><span class="sxs-lookup"><span data-stu-id="b4b67-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="b4b67-277">Ensimmäisen kuukauden lopussa asiakkaan on selvitettävä valmiin työn prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="b4b67-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="b4b67-278">Kun asiakas on tarkistanut projektin, hän päättää, että projektista on 15 prosenttia valmis.</span><span class="sxs-lookup"><span data-stu-id="b4b67-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="b4b67-279">Voit luoda laskun, jonka summa on 15 000 (15 prosenttia 100 000:sta) ja lähettää sen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="b4b67-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="b4b67-280">Esimerkki: sellaisen laskutussäännön luominen, joka perustuu tiettyyn prosenttiosuuteen projektin valmistumisesta (automaattisesta laskennasta)</span><span class="sxs-lookup"><span data-stu-id="b4b67-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="b4b67-281">Organisaatiosi, ohjelmistokehitysyritys, sitoutuu kehittämään asiakkaalle 30 000 palkanlaskentapaketin.</span><span class="sxs-lookup"><span data-stu-id="b4b67-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="b4b67-282">Asiakas sitoutuu maksamaan organisaatiollesi suoritettujen töiden prosenttiosuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="b4b67-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="b4b67-283">Arvioit, että projektin kustannukset ovat 20 000.</span><span class="sxs-lookup"><span data-stu-id="b4b67-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="b4b67-284">Projektisopimus määrittää työluokat, joita käytät laskutusprosessissa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="b4b67-285">Voit määrittää laskutussäännöt, jotka laskevat automaattisesti kullekin luokalle valmiin työn prosenttimäärän laskusummat.</span><span class="sxs-lookup"><span data-stu-id="b4b67-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="b4b67-286">Kullekin luokalle määritetään budjetti:</span><span class="sxs-lookup"><span data-stu-id="b4b67-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="b4b67-287">**Kehitys** – Kustannukset 15 000 ja liikevaihto 20 000</span><span class="sxs-lookup"><span data-stu-id="b4b67-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="b4b67-288">**Asennus** – Kustannukset 5 000 ja liikevaihto 10 000</span><span class="sxs-lookup"><span data-stu-id="b4b67-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="b4b67-289">Kun luot myyntilaskun ensimmäisen kerran, laskun summa lasketaan automaattisesti seuraavien tietojen perusteella:</span><span class="sxs-lookup"><span data-stu-id="b4b67-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="b4b67-290">Kuukauden kuluttua projektin työntekijä lähettää projektiraportin.</span><span class="sxs-lookup"><span data-stu-id="b4b67-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="b4b67-291">Työntekijän tuntien kustannukset ovat 5 000 kehityksen ja 1 000 asennuksen osalta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="b4b67-292">Kehitystyöt ovat 33 prosenttisesti valmiina (5 000 todelliset kustannukset/15 000 budjettikustannukset), ja asennustyöt ovat 20 prosenttisesti valmiina (1 000 toteutuneet kustannukset/5 000 budjettikustannukset).</span><span class="sxs-lookup"><span data-stu-id="b4b67-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="b4b67-293">Laskun summa 8 667 lasketaan automaattisesti (33 prosenttia 20 000 + 20 prosenttia 10 000).</span><span class="sxs-lookup"><span data-stu-id="b4b67-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="b4b67-294">Voit luoda laskun, jonka summa on 8 667 ja lähettää sen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="b4b67-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="b4b67-295">Esimerkki: sellaisen laskutussäännön luominen, joka perustuu sovittuihin välitavoitteisiin</span><span class="sxs-lookup"><span data-stu-id="b4b67-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="b4b67-296">Organisaatiosi, liikkeenjohdon konsultointiyritys, sitoutuu tekemään markkinatutkimusta kuluttajatuotteesta, jota asiakas suunnittelee myyvänsä.</span><span class="sxs-lookup"><span data-stu-id="b4b67-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="b4b67-297">Asiakas sitoutuu käyttämään palvelujasi kolmen kuukauden ajan maaliskuun alusta ja sitoutuu maksamaan organisaatiollesi 50 000.</span><span class="sxs-lookup"><span data-stu-id="b4b67-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="b4b67-298">Projektissa on kolme virstanpylvästä:</span><span class="sxs-lookup"><span data-stu-id="b4b67-298">The project has three milestones:</span></span>

-   <span data-ttu-id="b4b67-299">Välitavoite 1: Kuluttajatietojen kerääminen – 31. maaliskuuta</span><span class="sxs-lookup"><span data-stu-id="b4b67-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="b4b67-300">Välitavoite 2: Kuluttajatietojen analysointi – 30. huhtikuuta</span><span class="sxs-lookup"><span data-stu-id="b4b67-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="b4b67-301">Välitavoite 3: Tuotteen kannattavuusehdotuksen esittäminen – 31. toukokuuta</span><span class="sxs-lookup"><span data-stu-id="b4b67-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="b4b67-302">Asiakas sitoutuu maksamaan organisaatiollesi 10 000 ensimmäisen välitavoitteen, 20 000 toisen välitavoitteen ja 20 000 kolmannen välitavoitteen osalta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="b4b67-303">Kun määrität projektisopimuksen, sitoudut laskuttamaan asiakasta valmiiden välitavoitteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="b4b67-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="b4b67-304">Laskutussäännön asetuksissa on seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="b4b67-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="b4b67-305">Määritä projektin välitavoitteet.</span><span class="sxs-lookup"><span data-stu-id="b4b67-305">Define the project milestones.</span></span>
-   <span data-ttu-id="b4b67-306">Määritä summa, joka asiakkaalta laskutetaan, kun kukin välitavoite on valmis.</span><span class="sxs-lookup"><span data-stu-id="b4b67-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="b4b67-307">Kun ensimmäinen välitavoite on valmis maaliskuun 31., merkitse välitavoite valmiiksi ja luo sitten lasku, jonka summa on 10 000 ja lähetä se asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="b4b67-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="b4b67-308">Välitavoitteille ei voi luoda laskua, ennen kuin olet merkinnyt välitavoitteen valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="b4b67-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="b4b67-309">Esimerkki: Luo palveluihin perustuva laskutussääntö ja hallinnointipalkkio</span><span class="sxs-lookup"><span data-stu-id="b4b67-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="b4b67-310">Organisaatiosi, liikkeenjohdon konsultointiyritys, sitoutuu tekemään markkinatutkimusta arvioidakseen asiakkaan, vähittäiskaupan yrityksen kehittämän tuotteen kannattavuutta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="b4b67-311">Sopimuksen ehdoissa täsmennetään, että tarjoat kolmen johtavan konsulttisi palveluja, jotka suorittavat tutkimuksen ajan ja materiaalien perusteella.</span><span class="sxs-lookup"><span data-stu-id="b4b67-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="b4b67-312">Asiakas sitoutuu maksamaan 100 tunnissa, johon lisätään 10 prosentin hallinnointipalkkio projektille veloitettavista konsultointitunneista.</span><span class="sxs-lookup"><span data-stu-id="b4b67-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b4b67-313">Kun määrität projektisopimuksen, luo laskutussääntö, joka lisää 10 prosentin hallinnointipalkkion projektista veloitettavien konsultointituntien osalta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b4b67-314">Kun luot asiakkaalle laskun, asiakkaalta laskutetaan 10 prosentin hallinnointipalkkio sekä konsultointiajan kustannukset.</span><span class="sxs-lookup"><span data-stu-id="b4b67-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="b4b67-315">Jos esimerkiksi kolme konsulttia työskenteli projektissa yhteensä 200 tuntia, järjestelmä luo laskun, jonka summa on 22 000 seuraavan laskelman perusteella:</span><span class="sxs-lookup"><span data-stu-id="b4b67-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="b4b67-316">200 tuntia 100 tunnilta = 20 000</span><span class="sxs-lookup"><span data-stu-id="b4b67-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="b4b67-317">10 prosentin hallinnointimaksu = 2 000</span><span class="sxs-lookup"><span data-stu-id="b4b67-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="b4b67-318">Laskun kokonaismäärä = 22 000</span><span class="sxs-lookup"><span data-stu-id="b4b67-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="b4b67-319">Jos maksut verotetaan asiakkaalle ja valitset arvonlisäveroryhmän projektisopimuksessa, arvonlisäveroryhmä syötetään automaattisesti maksujen laskutussääntöön.</span><span class="sxs-lookup"><span data-stu-id="b4b67-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="b4b67-320">Esimerkki: laskutussäännön luominen ajan ja materiaalien arvolle</span><span class="sxs-lookup"><span data-stu-id="b4b67-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="b4b67-321">Organisaatiosi, ohjelmistokonsultointiyritys, suostuu toimittamaan asiakkaalle ohjelmistokehitysprojektia varten viisi teknistä konsulttia seuraavan kuuden kuukauden ajaksi.</span><span class="sxs-lookup"><span data-stu-id="b4b67-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="b4b67-322">Asiakas sitoutuu maksamaan 150 jokaisesta konsultointitunnista sekä toimistotarvikkeiden kustannuksista.</span><span class="sxs-lookup"><span data-stu-id="b4b67-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="b4b67-323">Organisaatiosi lähettää laskun asiakkaalle kunkin kuukauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="b4b67-324">Kun määrität projektisopimuksen, sitoudut laskuttamaan asiakasta kuukausittain projektin ajan ja materiaalin perusteella.</span><span class="sxs-lookup"><span data-stu-id="b4b67-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="b4b67-325">Voit luoda laskutussäännön, joka sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="b4b67-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="b4b67-326">Sopimuskausi on kuusi kuukautta.</span><span class="sxs-lookup"><span data-stu-id="b4b67-326">The contract period is six months.</span></span>
-   <span data-ttu-id="b4b67-327">Konsultointiajan hinnaksi lasketaan 150 tunnissa.</span><span class="sxs-lookup"><span data-stu-id="b4b67-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="b4b67-328">Toimistotarvikkeet laskutetaan kustannustasolla, ja projektin kokonaiskustannukset eivät saa ylittää 10 000.</span><span class="sxs-lookup"><span data-stu-id="b4b67-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="b4b67-329">Luot asiakaslaskun kunkin kalenterikuukauden lopussa projektin aikana.</span><span class="sxs-lookup"><span data-stu-id="b4b67-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="b4b67-330">Ensimmäisen kuukauden aikana konsultit kirjaavat projektille yhteensä 800 tuntia.</span><span class="sxs-lookup"><span data-stu-id="b4b67-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="b4b67-331">Projektista veloitettavien toimistotarvikkeiden kustannukset ovat 2 000.</span><span class="sxs-lookup"><span data-stu-id="b4b67-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="b4b67-332">Tämän vuoksi voit kuukauden lopussa luoda laskun, jonka summa on 122 000. Siihen on laskettu 800 tuntia á 150, sekä 2 000 toimistotarvikkeista.</span><span class="sxs-lookup"><span data-stu-id="b4b67-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]