---
title: Projektipohjaisten tarjousrivien yleiskatsaus
description: Tässä aiheessa on tietoja projektipohjaisten tarjousrivien käyttämisestä projektityöhön.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277784"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="384df-103">Projektipohjaisten tarjousrivien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="384df-103">Project-based quote lines overview</span></span>

<span data-ttu-id="384df-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="384df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="384df-105">Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa.</span><span class="sxs-lookup"><span data-stu-id="384df-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="384df-106">Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:</span><span class="sxs-lookup"><span data-stu-id="384df-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="384df-107">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="384df-107">Billing Method</span></span>
- <span data-ttu-id="384df-108">Projektin yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="384df-108">Project Mapping</span></span>
- <span data-ttu-id="384df-109">Sisältyvät tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="384df-109">Included Transaction classes</span></span>
- <span data-ttu-id="384df-110">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="384df-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="384df-111">Veloitettavuusasetus</span><span class="sxs-lookup"><span data-stu-id="384df-111">Chargeability setup</span></span>
- <span data-ttu-id="384df-112">Arvio tarjousrivin tietojen avulla</span><span class="sxs-lookup"><span data-stu-id="384df-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="384df-113">Tarjousrivin asiakkaat</span><span class="sxs-lookup"><span data-stu-id="384df-113">Quote line Customers</span></span>

<span data-ttu-id="384df-114">Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset**-välilehden kentistä.</span><span class="sxs-lookup"><span data-stu-id="384df-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="384df-115">Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.</span><span class="sxs-lookup"><span data-stu-id="384df-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="384df-116">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="384df-116">**Field**</span></span> | <span data-ttu-id="384df-117">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="384df-117">**Description**</span></span> | <span data-ttu-id="384df-118">**Loppupään vaikutus**</span><span class="sxs-lookup"><span data-stu-id="384df-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="384df-119">Nimi</span><span class="sxs-lookup"><span data-stu-id="384df-119">Name</span></span> | <span data-ttu-id="384df-120">Tarjousrivin nimi, jonka avulla voit määrittää arvioidun tarjouksen erillisen osan.</span><span class="sxs-lookup"><span data-stu-id="384df-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="384df-121">Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-122">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="384df-122">Billing Method</span></span> | <span data-ttu-id="384df-123">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä.</span><span class="sxs-lookup"><span data-stu-id="384df-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="384df-124">Tässä kentässä on kaksi pääasiallista palvelusopimusmallia, joita Dynamics 365 Project Operationsissa tuetaan:</span><span class="sxs-lookup"><span data-stu-id="384df-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="384df-125">– Kiinteä hinta</span><span class="sxs-lookup"><span data-stu-id="384df-125">- Fixed price</span></span></br><span data-ttu-id="384df-126">– Aika ja materiaali.</span><span class="sxs-lookup"><span data-stu-id="384df-126">- Time and material.</span></span>| <span data-ttu-id="384df-127">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-128">Project</span><span class="sxs-lookup"><span data-stu-id="384df-128">Project</span></span> | <span data-ttu-id="384df-129">Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="384df-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="384df-130">Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina.</span><span class="sxs-lookup"><span data-stu-id="384df-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="384df-131">Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto.</span><span class="sxs-lookup"><span data-stu-id="384df-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="384df-132">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-133">Sisällytä aika</span><span class="sxs-lookup"><span data-stu-id="384df-133">Include Time</span></span> | <span data-ttu-id="384df-134">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin aikatapahtumat tai työvoimakustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="384df-135">**Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="384df-136">**Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="384df-137">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-138">Sisällytä kulu</span><span class="sxs-lookup"><span data-stu-id="384df-138">Include Expense</span></span> | <span data-ttu-id="384df-139">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin kulujen kustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="384df-140">**Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="384df-141">**Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="384df-142">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-143">Sisällytä maksu</span><span class="sxs-lookup"><span data-stu-id="384df-143">Include Fee</span></span> | <span data-ttu-id="384df-144">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin maksut sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="384df-145">**Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="384df-146">**Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="384df-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="384df-147">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-148">Tarjottu summa</span><span class="sxs-lookup"><span data-stu-id="384df-148">Quoted Amount</span></span> | <span data-ttu-id="384df-149">Tämä on summa, joka tarjotaan asiakkaalle kaikista tähän projektipohjaiseen tarjousriviin ennustetuista töistä.</span><span class="sxs-lookup"><span data-stu-id="384df-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="384df-150">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="384df-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="384df-151">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista.</span><span class="sxs-lookup"><span data-stu-id="384df-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="384df-152">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-153">Arvioitu vero</span><span class="sxs-lookup"><span data-stu-id="384df-153">Estimated Tax</span></span> | <span data-ttu-id="384df-154">Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="384df-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="384df-155">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista.</span><span class="sxs-lookup"><span data-stu-id="384df-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="384df-156">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-157">Tarjouksen summa veron jälkeen</span><span class="sxs-lookup"><span data-stu-id="384df-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="384df-158">Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="384df-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="384df-159">Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*.</span><span class="sxs-lookup"><span data-stu-id="384df-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="384df-160">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-161">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="384df-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="384df-162">Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="384df-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="384df-163">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="384df-164">Asiakasbudjetti</span><span class="sxs-lookup"><span data-stu-id="384df-164">Customer Budget</span></span> | <span data-ttu-id="384df-165">Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="384df-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="384df-166">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="384df-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="384df-167">Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt</span><span class="sxs-lookup"><span data-stu-id="384df-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="384df-168">**Sääntö 1**: Valitun projektin tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="384df-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="384df-169">**Sääntö 2**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.</span><span class="sxs-lookup"><span data-stu-id="384df-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="384df-170">**Sääntö 3**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="384df-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="384df-171">
                    <strong>Mahdollisuus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="384df-172">
                    <strong>Tarjous</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="384df-173">
                    <strong>Tarjousrivi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="384df-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="384df-175">
                    <strong>Sisällytä aika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="384df-176">
                    <strong>Sisällytä kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="384df-177">
                    <strong>Sisällytä</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="384df-178">
                    <strong>maksu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="384df-179">
                    <strong>Kelpaa / ei kelpaa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="384df-180">
                    <strong>Syy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="384df-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-181">O1</span><span class="sxs-lookup"><span data-stu-id="384df-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-182">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-183">QL1</span><span class="sxs-lookup"><span data-stu-id="384df-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-184">K1</span><span class="sxs-lookup"><span data-stu-id="384df-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-185">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-186">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-187">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-188">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="384df-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-189">Säännön 1 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="384df-189">Violation of Rule #1.</span></span> <span data-ttu-id="384df-190">P1-projektin aika, kulu ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="384df-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-191">O1</span><span class="sxs-lookup"><span data-stu-id="384df-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-192">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-193">QL2</span><span class="sxs-lookup"><span data-stu-id="384df-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-194">K1</span><span class="sxs-lookup"><span data-stu-id="384df-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-195">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-196">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-197">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-198">O1</span><span class="sxs-lookup"><span data-stu-id="384df-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-199">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-200">QL1</span><span class="sxs-lookup"><span data-stu-id="384df-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-201">K1</span><span class="sxs-lookup"><span data-stu-id="384df-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-202">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-203">No</span><span class="sxs-lookup"><span data-stu-id="384df-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-204">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-205">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="384df-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-206">Säännön 1 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="384df-206">Violation of Rule #1.</span></span> <span data-ttu-id="384df-207">P1-projektin aika ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="384df-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-208">O1</span><span class="sxs-lookup"><span data-stu-id="384df-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-209">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-210">QL2</span><span class="sxs-lookup"><span data-stu-id="384df-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-211">K1</span><span class="sxs-lookup"><span data-stu-id="384df-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-212">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-213">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-214">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-215">O1</span><span class="sxs-lookup"><span data-stu-id="384df-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-216">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-217">QL1</span><span class="sxs-lookup"><span data-stu-id="384df-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-218">K1</span><span class="sxs-lookup"><span data-stu-id="384df-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-220">No</span><span class="sxs-lookup"><span data-stu-id="384df-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-221">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-222">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="384df-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="384df-223">P1-projektin aika ja maksut sisältyvät riville QL1.</span><span class="sxs-lookup"><span data-stu-id="384df-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="384df-224">Kulu P1-projektissa sisältyy riville QL2.</span><span class="sxs-lookup"><span data-stu-id="384df-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="384df-225">Kullekin tarjousriville lisätyissä kohteissa ei ole päällekkäisyyttä, joten tämä on kelvollinen.</span><span class="sxs-lookup"><span data-stu-id="384df-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-226">O1</span><span class="sxs-lookup"><span data-stu-id="384df-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-227">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-228">QL2</span><span class="sxs-lookup"><span data-stu-id="384df-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-229">K1</span><span class="sxs-lookup"><span data-stu-id="384df-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-230">No</span><span class="sxs-lookup"><span data-stu-id="384df-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-231">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-232">No</span><span class="sxs-lookup"><span data-stu-id="384df-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-233">O1</span><span class="sxs-lookup"><span data-stu-id="384df-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-234">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-235">QL1</span><span class="sxs-lookup"><span data-stu-id="384df-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-236">K1</span><span class="sxs-lookup"><span data-stu-id="384df-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-237">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-238">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-239">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-240">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="384df-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-241">Säännön 1 rikkominen yllä</span><span class="sxs-lookup"><span data-stu-id="384df-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="384df-242">Q1 sisältää koko P1-projektin ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="384df-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="384df-243">QL2 sisältää koko projektin P1 ajan, kulut ja maksut, ja se on päällekkäinen riville Q1 sisällytettyjen kohteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="384df-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-244">O1</span><span class="sxs-lookup"><span data-stu-id="384df-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-245">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-246">QL2</span><span class="sxs-lookup"><span data-stu-id="384df-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-247">K1</span><span class="sxs-lookup"><span data-stu-id="384df-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-248">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-250">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-251">O1</span><span class="sxs-lookup"><span data-stu-id="384df-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-252">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-253">QL1</span><span class="sxs-lookup"><span data-stu-id="384df-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-254">K1</span><span class="sxs-lookup"><span data-stu-id="384df-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-255">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-256">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-257">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="384df-258">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="384df-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-259">Säännön 2 mukaan Q1 ja Q2 ovat saman mahdollisuuden kaksi tarjousta, joten ne voivat molemmat arvioida projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="384df-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-260">O1</span><span class="sxs-lookup"><span data-stu-id="384df-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-261">VN2</span><span class="sxs-lookup"><span data-stu-id="384df-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-262">QL1 kohteessa Q2</span><span class="sxs-lookup"><span data-stu-id="384df-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-263">K1</span><span class="sxs-lookup"><span data-stu-id="384df-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-264">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-265">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-266">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-267">O1</span><span class="sxs-lookup"><span data-stu-id="384df-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-268">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-269">QL1</span><span class="sxs-lookup"><span data-stu-id="384df-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-270">K1</span><span class="sxs-lookup"><span data-stu-id="384df-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-271">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-272">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-273">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="384df-274">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="384df-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="384df-275">Säännön 3 mukaan Q1 ja Q2 ovat eri mahdollisuuksien kaksi tarjousta, joten ne eivät voi arvioida saman projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="384df-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="384df-276">O2</span><span class="sxs-lookup"><span data-stu-id="384df-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="384df-277">VN1</span><span class="sxs-lookup"><span data-stu-id="384df-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-278">QL1</span><span class="sxs-lookup"><span data-stu-id="384df-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-279">K1</span><span class="sxs-lookup"><span data-stu-id="384df-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-280">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="384df-281">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="384df-282">Kyllä</span><span class="sxs-lookup"><span data-stu-id="384df-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="384df-283">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="384df-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]