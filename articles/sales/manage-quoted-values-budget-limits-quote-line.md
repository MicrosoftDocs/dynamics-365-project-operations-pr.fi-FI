---
title: Projektipohjaiset tarjousrivit
description: Tässä aiheessa on tietoja projektipohjaisten tarjousrivien käyttämisestä projektityöhön.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906147"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="956e7-103">Projektipohjaiset tarjousrivit</span><span class="sxs-lookup"><span data-stu-id="956e7-103">Project-based quote lines</span></span>

<span data-ttu-id="956e7-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="956e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="956e7-105">Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa.</span><span class="sxs-lookup"><span data-stu-id="956e7-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="956e7-106">Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:</span><span class="sxs-lookup"><span data-stu-id="956e7-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="956e7-107">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="956e7-107">Billing Method</span></span>
- <span data-ttu-id="956e7-108">Projektin yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="956e7-108">Project Mapping</span></span>
- <span data-ttu-id="956e7-109">Sisältyvät tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="956e7-109">Included Transaction classes</span></span>
- <span data-ttu-id="956e7-110">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="956e7-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="956e7-111">Veloitettavuusasetus</span><span class="sxs-lookup"><span data-stu-id="956e7-111">Chargeability setup</span></span>
- <span data-ttu-id="956e7-112">Arvio tarjousrivin tietojen avulla</span><span class="sxs-lookup"><span data-stu-id="956e7-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="956e7-113">Tarjousrivin asiakkaat</span><span class="sxs-lookup"><span data-stu-id="956e7-113">Quote line Customers</span></span>

<span data-ttu-id="956e7-114">Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset**-välilehden kentistä.</span><span class="sxs-lookup"><span data-stu-id="956e7-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="956e7-115">Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.</span><span class="sxs-lookup"><span data-stu-id="956e7-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="956e7-116">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="956e7-116">**Field**</span></span> | <span data-ttu-id="956e7-117">**Relevanssi, tarkoitus ja opastus**</span><span class="sxs-lookup"><span data-stu-id="956e7-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="956e7-118">**Loppupään vaikutus**</span><span class="sxs-lookup"><span data-stu-id="956e7-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="956e7-119">Nimi</span><span class="sxs-lookup"><span data-stu-id="956e7-119">Name</span></span> | <span data-ttu-id="956e7-120">Tarjousrivin nimi, jonka avulla voit määrittää arvioidun tarjouksen erillisen osan.</span><span class="sxs-lookup"><span data-stu-id="956e7-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="956e7-121">Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-122">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="956e7-122">Billing Method</span></span> | <span data-ttu-id="956e7-123">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä.</span><span class="sxs-lookup"><span data-stu-id="956e7-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="956e7-124">Tämä kenttä sisältää kaksi tärkeintä Dynamics 365 Project Operationsin tukemaa sopimusmallia:</span><span class="sxs-lookup"><span data-stu-id="956e7-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="956e7-125">– Kiinteä hinta</span><span class="sxs-lookup"><span data-stu-id="956e7-125">- Fixed price</span></span></br><span data-ttu-id="956e7-126">– Aika ja materiaali.</span><span class="sxs-lookup"><span data-stu-id="956e7-126">- Time and material.</span></span>| <span data-ttu-id="956e7-127">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-128">Project</span><span class="sxs-lookup"><span data-stu-id="956e7-128">Project</span></span> | <span data-ttu-id="956e7-129">Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="956e7-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="956e7-130">Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina.</span><span class="sxs-lookup"><span data-stu-id="956e7-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="956e7-131">Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto.</span><span class="sxs-lookup"><span data-stu-id="956e7-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="956e7-132">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-133">Sisällytä aika</span><span class="sxs-lookup"><span data-stu-id="956e7-133">Include Time</span></span> | <span data-ttu-id="956e7-134">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin aikatapahtumat tai työvoimakustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="956e7-135">**Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="956e7-136">**Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="956e7-137">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-138">Sisällytä kulu</span><span class="sxs-lookup"><span data-stu-id="956e7-138">Include Expense</span></span> | <span data-ttu-id="956e7-139">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin kulujen kustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="956e7-140">**Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="956e7-141">**Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="956e7-142">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-143">Sisällytä maksu</span><span class="sxs-lookup"><span data-stu-id="956e7-143">Include Fee</span></span> | <span data-ttu-id="956e7-144">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin maksut sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="956e7-145">**Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="956e7-146">**Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="956e7-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="956e7-147">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-148">Tarjottu summa</span><span class="sxs-lookup"><span data-stu-id="956e7-148">Quoted Amount</span></span> | <span data-ttu-id="956e7-149">Tämä on summa, joka tarjotaan asiakkaalle kaikista tähän projektipohjaiseen tarjousriviin ennustetuista töistä.</span><span class="sxs-lookup"><span data-stu-id="956e7-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="956e7-150">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="956e7-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="956e7-151">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista.</span><span class="sxs-lookup"><span data-stu-id="956e7-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="956e7-152">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-153">Arvioitu vero</span><span class="sxs-lookup"><span data-stu-id="956e7-153">Estimated Tax</span></span> | <span data-ttu-id="956e7-154">Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="956e7-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="956e7-155">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista.</span><span class="sxs-lookup"><span data-stu-id="956e7-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="956e7-156">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-157">Tarjouksen summa veron jälkeen</span><span class="sxs-lookup"><span data-stu-id="956e7-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="956e7-158">Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="956e7-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="956e7-159">Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*.</span><span class="sxs-lookup"><span data-stu-id="956e7-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="956e7-160">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-161">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="956e7-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="956e7-162">Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="956e7-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="956e7-163">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="956e7-164">Asiakasbudjetti</span><span class="sxs-lookup"><span data-stu-id="956e7-164">Customer Budget</span></span> | <span data-ttu-id="956e7-165">Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="956e7-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="956e7-166">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="956e7-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="956e7-167">Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt</span><span class="sxs-lookup"><span data-stu-id="956e7-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="956e7-168">**Sääntö 1**: Valitun projektin tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="956e7-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="956e7-169">**Sääntö 2**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.</span><span class="sxs-lookup"><span data-stu-id="956e7-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="956e7-170">**Sääntö 3**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="956e7-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="956e7-171">
                    <strong>Mahdollisuus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="956e7-172">
                    <strong>Tarjous</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="956e7-173">
                    <strong>Tarjousrivi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="956e7-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="956e7-175">
                    <strong>Sisällytä aika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="956e7-176">
                    <strong>Sisällytä kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="956e7-177">
                    <strong>Sisällytä</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="956e7-178">
                    <strong>maksu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="956e7-179">
                    <strong>Kelpaa / ei kelpaa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="956e7-180">
                    <strong>Syy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="956e7-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="956e7-181">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-182">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-183">QL1</span><span class="sxs-lookup"><span data-stu-id="956e7-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-184">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-185">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-186">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-187">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-188">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="956e7-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-189">Säännön 1 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="956e7-189">Violation of Rule #1.</span></span> <span data-ttu-id="956e7-190">P1-projektin aika, kulu ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="956e7-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="956e7-191">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-192">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-193">QL2</span><span class="sxs-lookup"><span data-stu-id="956e7-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-194">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-195">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-196">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-197">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-197">Yes</span></span> </p>
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
<span data-ttu-id="956e7-198">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-199">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-200">QL1</span><span class="sxs-lookup"><span data-stu-id="956e7-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-201">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-202">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-203">No</span><span class="sxs-lookup"><span data-stu-id="956e7-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-204">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-205">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="956e7-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-206">Säännön 1 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="956e7-206">Violation of Rule #1.</span></span> <span data-ttu-id="956e7-207">P1-projektin aika ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="956e7-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="956e7-208">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-209">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-210">QL2</span><span class="sxs-lookup"><span data-stu-id="956e7-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-211">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-212">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-213">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-214">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-214">Yes</span></span> </p>
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
<span data-ttu-id="956e7-215">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-216">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-217">QL1</span><span class="sxs-lookup"><span data-stu-id="956e7-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-218">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-220">No</span><span class="sxs-lookup"><span data-stu-id="956e7-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-221">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-222">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="956e7-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="956e7-223">P1-projektin aika ja maksut sisältyvät riville QL1.</span><span class="sxs-lookup"><span data-stu-id="956e7-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="956e7-224">Kulu P1-projektissa sisältyy riville QL2.</span><span class="sxs-lookup"><span data-stu-id="956e7-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="956e7-225">Kullekin tarjousriville lisätyissä kohteissa ei ole päällekkäisyyttä, joten tämä on kelvollinen.</span><span class="sxs-lookup"><span data-stu-id="956e7-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="956e7-226">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-227">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-228">QL2</span><span class="sxs-lookup"><span data-stu-id="956e7-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-229">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-230">No</span><span class="sxs-lookup"><span data-stu-id="956e7-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-231">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-232">No</span><span class="sxs-lookup"><span data-stu-id="956e7-232">No</span></span> </p>
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
<span data-ttu-id="956e7-233">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-234">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-235">QL1</span><span class="sxs-lookup"><span data-stu-id="956e7-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-236">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-237">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-238">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-239">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-240">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="956e7-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-241">Säännön 1 rikkominen yllä</span><span class="sxs-lookup"><span data-stu-id="956e7-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="956e7-242">Q1 sisältää koko P1-projektin ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="956e7-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="956e7-243">QL2 sisältää koko projektin P1 ajan, kulut ja maksut, ja se on päällekkäinen riville Q1 sisällytettyjen kohteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="956e7-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="956e7-244">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-245">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-246">QL2</span><span class="sxs-lookup"><span data-stu-id="956e7-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-247">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-248">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-250">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-250">Yes</span></span> </p>
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
<span data-ttu-id="956e7-251">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-252">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-253">QL1</span><span class="sxs-lookup"><span data-stu-id="956e7-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-254">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-255">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-256">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-257">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="956e7-258">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="956e7-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-259">Säännön 2 mukaan Q1 ja Q2 ovat saman mahdollisuuden kaksi tarjousta, joten ne voivat molemmat arvioida projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="956e7-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="956e7-260">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-261">VN2</span><span class="sxs-lookup"><span data-stu-id="956e7-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-262">QL1 kohteessa Q2</span><span class="sxs-lookup"><span data-stu-id="956e7-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-263">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-264">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-265">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-266">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-266">Yes</span></span> </p>
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
<span data-ttu-id="956e7-267">O1</span><span class="sxs-lookup"><span data-stu-id="956e7-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-268">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-269">QL1</span><span class="sxs-lookup"><span data-stu-id="956e7-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-270">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-271">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-272">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-273">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="956e7-274">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="956e7-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="956e7-275">Säännön 3 mukaan Q1 ja Q2 ovat eri mahdollisuuksien kaksi tarjousta, joten ne eivät voi arvioida saman projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="956e7-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="956e7-276">O2</span><span class="sxs-lookup"><span data-stu-id="956e7-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="956e7-277">VN1</span><span class="sxs-lookup"><span data-stu-id="956e7-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-278">QL1</span><span class="sxs-lookup"><span data-stu-id="956e7-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-279">K1</span><span class="sxs-lookup"><span data-stu-id="956e7-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-280">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="956e7-281">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="956e7-282">Kyllä</span><span class="sxs-lookup"><span data-stu-id="956e7-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="956e7-283">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="956e7-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

