---
title: Projektipohjaisten tarjousrivien yleiskatsaus – lite
description: Tässä aiheessa on tietoja projektipohjaisten tarjousrivien käyttämisestä projektityöhön. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181088"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="3846d-104">Projektipohjaisten tarjousrivien yleiskatsaus – lite</span><span class="sxs-lookup"><span data-stu-id="3846d-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="3846d-105">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="3846d-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3846d-106">Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa.</span><span class="sxs-lookup"><span data-stu-id="3846d-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="3846d-107">Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:</span><span class="sxs-lookup"><span data-stu-id="3846d-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="3846d-108">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="3846d-108">Billing Method</span></span>
- <span data-ttu-id="3846d-109">Projektin ja tehtävän yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="3846d-109">Project and Task Mapping</span></span>
- <span data-ttu-id="3846d-110">Sisältyvät tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="3846d-110">Included Transaction classes</span></span>
- <span data-ttu-id="3846d-111">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="3846d-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="3846d-112">Veloitettavuusasetus</span><span class="sxs-lookup"><span data-stu-id="3846d-112">Chargeability setup</span></span>
- <span data-ttu-id="3846d-113">Arvio tarjousrivin tietojen avulla</span><span class="sxs-lookup"><span data-stu-id="3846d-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="3846d-114">Tarjousrivin asiakkaat</span><span class="sxs-lookup"><span data-stu-id="3846d-114">Quote line Customers</span></span>

<span data-ttu-id="3846d-115">Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset**-välilehden kentistä.</span><span class="sxs-lookup"><span data-stu-id="3846d-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="3846d-116">Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.</span><span class="sxs-lookup"><span data-stu-id="3846d-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="3846d-117">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="3846d-117">**Field**</span></span> | <span data-ttu-id="3846d-118">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="3846d-118">**Description**</span></span> | <span data-ttu-id="3846d-119">**Loppupään vaikutus**</span><span class="sxs-lookup"><span data-stu-id="3846d-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3846d-120">Nimi</span><span class="sxs-lookup"><span data-stu-id="3846d-120">Name</span></span> | <span data-ttu-id="3846d-121">Tarjousrivin nimi, jonka avulla voit määrittää arvioidun tarjouksen erillisen osan.</span><span class="sxs-lookup"><span data-stu-id="3846d-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="3846d-122">Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-123">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="3846d-123">Billing Method</span></span> | <span data-ttu-id="3846d-124">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä.</span><span class="sxs-lookup"><span data-stu-id="3846d-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="3846d-125">Tämä kenttä sisältää kaksi tärkeintä Dynamics 365 Project Operationsin tukemaa sopimusmallia:</span><span class="sxs-lookup"><span data-stu-id="3846d-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="3846d-126">– Kiinteä hinta</span><span class="sxs-lookup"><span data-stu-id="3846d-126">- Fixed price</span></span></br><span data-ttu-id="3846d-127">– Aika ja materiaali.</span><span class="sxs-lookup"><span data-stu-id="3846d-127">- Time and material.</span></span>| <span data-ttu-id="3846d-128">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-129">Project</span><span class="sxs-lookup"><span data-stu-id="3846d-129">Project</span></span> | <span data-ttu-id="3846d-130">Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="3846d-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="3846d-131">Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina.</span><span class="sxs-lookup"><span data-stu-id="3846d-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="3846d-132">Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto.</span><span class="sxs-lookup"><span data-stu-id="3846d-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="3846d-133">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="3846d-134">Sisällytettävät tehtävät</span><span class="sxs-lookup"><span data-stu-id="3846d-134">Included Tasks</span></span> | <span data-ttu-id="3846d-135">Ilmaisee, käytetäänkö tätä tarjousriviä valitussa projektissa kaikkiin projektitehtäviin vai vain joihinkin niistä.</span><span class="sxs-lookup"><span data-stu-id="3846d-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="3846d-136">Tällä kentällä on seuraavat mahdolliset arvot:</span><span class="sxs-lookup"><span data-stu-id="3846d-136">This field has the following possible values:</span></span></br><span data-ttu-id="3846d-137">– Kaikki projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="3846d-137">- All project tasks</span></span></br><span data-ttu-id="3846d-138">– Vain valitut projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="3846d-138">- Selected project tasks only</span></span></br><span data-ttu-id="3846d-139">Tässä kentässä oleva tyhjä arvo vastaa **Kaikki projektitehtävät** -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="3846d-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="3846d-140">Kun **Vain valitut projektitehtävät** valitaan projektisivulla, **Tehtävien laskutuksen asetukset** -välilehdessä voit valita tiettyjä tehtäviä, jotka liitetään tähän tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="3846d-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="3846d-141">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-142">Sisällytä aika</span><span class="sxs-lookup"><span data-stu-id="3846d-142">Include Time</span></span> | <span data-ttu-id="3846d-143">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin aikatapahtumat tai työvoimakustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="3846d-144">**Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="3846d-145">**Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="3846d-146">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-147">Sisällytä kulu</span><span class="sxs-lookup"><span data-stu-id="3846d-147">Include Expense</span></span> | <span data-ttu-id="3846d-148">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin kulujen kustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="3846d-149">**Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="3846d-150">**Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="3846d-151">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-152">Sisällytä maksu</span><span class="sxs-lookup"><span data-stu-id="3846d-152">Include Fee</span></span> | <span data-ttu-id="3846d-153">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin maksut sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="3846d-154">**Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="3846d-155">**Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="3846d-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="3846d-156">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-157">Tarjottu summa</span><span class="sxs-lookup"><span data-stu-id="3846d-157">Quoted Amount</span></span> | <span data-ttu-id="3846d-158">Tämä on summa, joka tarjotaan asiakkaalle kaikista tähän projektipohjaiseen tarjousriviin ennustetuista töistä.</span><span class="sxs-lookup"><span data-stu-id="3846d-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="3846d-159">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="3846d-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="3846d-160">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista.</span><span class="sxs-lookup"><span data-stu-id="3846d-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="3846d-161">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-162">Arvioitu vero</span><span class="sxs-lookup"><span data-stu-id="3846d-162">Estimated Tax</span></span> | <span data-ttu-id="3846d-163">Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="3846d-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="3846d-164">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista.</span><span class="sxs-lookup"><span data-stu-id="3846d-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="3846d-165">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-166">Tarjouksen summa veron jälkeen</span><span class="sxs-lookup"><span data-stu-id="3846d-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="3846d-167">Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="3846d-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="3846d-168">Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*.</span><span class="sxs-lookup"><span data-stu-id="3846d-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="3846d-169">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-170">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="3846d-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="3846d-171">Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="3846d-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="3846d-172">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="3846d-173">Asiakasbudjetti</span><span class="sxs-lookup"><span data-stu-id="3846d-173">Customer Budget</span></span> | <span data-ttu-id="3846d-174">Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="3846d-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="3846d-175">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="3846d-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="3846d-176">Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt</span><span class="sxs-lookup"><span data-stu-id="3846d-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="3846d-177">**Sääntö 1**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti sisällytetään tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="3846d-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="3846d-178">**Sääntö 2**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="3846d-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="3846d-179">**Sääntö 3**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Vain valitut projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää useille tarjouksen projektipohjaisille tarjousriveille.</span><span class="sxs-lookup"><span data-stu-id="3846d-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="3846d-180">**Sääntö 4**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.</span><span class="sxs-lookup"><span data-stu-id="3846d-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="3846d-181">**Sääntö 5**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="3846d-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="3846d-182">
                    <strong>Mahdollisuus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="3846d-183">
                    <strong>Tarjous</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="3846d-184">
                    <strong>Tarjousrivi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="3846d-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="3846d-186">
                    <strong>Sisällytettävät tehtävät</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="3846d-187">
                    <strong>Sisällytä aika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="3846d-188">
                    <strong>Sisällytä kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="3846d-189">
                    <strong>Sisällytä</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="3846d-190">
                    <strong>Maksu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="3846d-191">
                    <strong>Kelpaa / ei kelpaa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="3846d-192">
                    <strong>Syy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3846d-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-193">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-194">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-195">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-196">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-197">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-198">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-199">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-200">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-201">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="3846d-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-202">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="3846d-202">Violation of Rule #2.</span></span> <span data-ttu-id="3846d-203">P1-projektin aika, kulu ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="3846d-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-204">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-205">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-206">QL2</span><span class="sxs-lookup"><span data-stu-id="3846d-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-207">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-208">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-209">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-210">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-211">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="3846d-212">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-213">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-214">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-215">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-216">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-217">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-218">No</span><span class="sxs-lookup"><span data-stu-id="3846d-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-220">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="3846d-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-221">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="3846d-221">Violation of Rule #2.</span></span> <span data-ttu-id="3846d-222">P1-projektin aika ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="3846d-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-223">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-224">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-225">QL2</span><span class="sxs-lookup"><span data-stu-id="3846d-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-226">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-227">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-228">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-229">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-230">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-231">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-232">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-233">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-234">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-235">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-236">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-237">No</span><span class="sxs-lookup"><span data-stu-id="3846d-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-238">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-239">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="3846d-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="3846d-240">P1-projektin aika ja maksut sisältyvät riville QL1.</span><span class="sxs-lookup"><span data-stu-id="3846d-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="3846d-241">Kulu P1-projektissa sisältyy riville QL2.</span><span class="sxs-lookup"><span data-stu-id="3846d-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="3846d-242">Kullekin tarjousriville lisätyissä kohteissa ei ole päällekkäisyyttä, ja tämä on kelvollinen.</span><span class="sxs-lookup"><span data-stu-id="3846d-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-243">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-244">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-245">QL2</span><span class="sxs-lookup"><span data-stu-id="3846d-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-246">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-247">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-248">No</span><span class="sxs-lookup"><span data-stu-id="3846d-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-250">No</span><span class="sxs-lookup"><span data-stu-id="3846d-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="3846d-251">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-252">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-253">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-254">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-255">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="3846d-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-256">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-257">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-258">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-259">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="3846d-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-260">Säännön 2 rikkominen yllä</span><span class="sxs-lookup"><span data-stu-id="3846d-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="3846d-261">Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="3846d-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="3846d-262">QL2 sisältää koko projektin P1 ajan, kulut ja maksut, ja se on päällekkäinen riville Q1 sisällytettyjen kohteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="3846d-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-263">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-264">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-265">QL2</span><span class="sxs-lookup"><span data-stu-id="3846d-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-266">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-267">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-268">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-269">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-270">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-271">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-272">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-273">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-274">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-275">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="3846d-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-276">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-277">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-278">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-279">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="3846d-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-280">Edellä olevan säännön 3 mukaan</span><span class="sxs-lookup"><span data-stu-id="3846d-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="3846d-281">Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="3846d-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="3846d-282">QL2 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="3846d-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="3846d-283">Ainoa lisätarkistus on QL1-rivin tehtävien alijoukolle, joka eroaa QL2-rivin tehtävien alijoukosta.</span><span class="sxs-lookup"><span data-stu-id="3846d-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="3846d-284">Näin varmistetaan, että päällekkäisyyksiä ei ole.</span><span class="sxs-lookup"><span data-stu-id="3846d-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="3846d-285">Järjestelmä suorittaa tämän, kun tehtävät on liitetty.</span><span class="sxs-lookup"><span data-stu-id="3846d-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-286">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-287">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-288">QL2</span><span class="sxs-lookup"><span data-stu-id="3846d-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-289">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-290">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="3846d-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-291">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-292">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-293">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="3846d-294">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-295">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-296">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-297">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-298">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-299">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-300">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-301">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="3846d-302">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="3846d-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-303">Säännön 5 mukaan Q1 ja Q2 ovat saman mahdollisuuden kaksi tarjousta, joten ne voivat molemmat arvioida projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="3846d-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-304">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-305">VN2</span><span class="sxs-lookup"><span data-stu-id="3846d-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-306">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-307">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-308">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-309">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-310">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-311">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="3846d-312">O1</span><span class="sxs-lookup"><span data-stu-id="3846d-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-313">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-314">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-315">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-316">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-317">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-318">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-319">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="3846d-320">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="3846d-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3846d-321">Säännön 4 mukaan Q1 ja Q2 ovat eri mahdollisuuksien kaksi tarjousta, joten ne eivät voi arvioida saman projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="3846d-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="3846d-322">O2</span><span class="sxs-lookup"><span data-stu-id="3846d-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="3846d-323">VN1</span><span class="sxs-lookup"><span data-stu-id="3846d-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-324">QL1</span><span class="sxs-lookup"><span data-stu-id="3846d-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-325">K1</span><span class="sxs-lookup"><span data-stu-id="3846d-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="3846d-326">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="3846d-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-327">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3846d-328">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3846d-329">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3846d-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="3846d-330">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="3846d-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

