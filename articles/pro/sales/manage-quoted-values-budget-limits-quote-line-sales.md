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
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272969"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="e85e9-104">Projektipohjaisten tarjousrivien yleiskatsaus – lite</span><span class="sxs-lookup"><span data-stu-id="e85e9-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="e85e9-105">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="e85e9-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e85e9-106">Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa.</span><span class="sxs-lookup"><span data-stu-id="e85e9-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="e85e9-107">Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:</span><span class="sxs-lookup"><span data-stu-id="e85e9-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="e85e9-108">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="e85e9-108">Billing Method</span></span>
- <span data-ttu-id="e85e9-109">Projektin ja tehtävän yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="e85e9-109">Project and Task Mapping</span></span>
- <span data-ttu-id="e85e9-110">Sisältyvät tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="e85e9-110">Included Transaction classes</span></span>
- <span data-ttu-id="e85e9-111">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="e85e9-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="e85e9-112">Veloitettavuusasetus</span><span class="sxs-lookup"><span data-stu-id="e85e9-112">Chargeability setup</span></span>
- <span data-ttu-id="e85e9-113">Arvio tarjousrivin tietojen avulla</span><span class="sxs-lookup"><span data-stu-id="e85e9-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="e85e9-114">Tarjousrivin asiakkaat</span><span class="sxs-lookup"><span data-stu-id="e85e9-114">Quote line Customers</span></span>

<span data-ttu-id="e85e9-115">Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset**-välilehden kentistä.</span><span class="sxs-lookup"><span data-stu-id="e85e9-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="e85e9-116">Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.</span><span class="sxs-lookup"><span data-stu-id="e85e9-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="e85e9-117">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="e85e9-117">**Field**</span></span> | <span data-ttu-id="e85e9-118">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="e85e9-118">**Description**</span></span> | <span data-ttu-id="e85e9-119">**Loppupään vaikutus**</span><span class="sxs-lookup"><span data-stu-id="e85e9-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e85e9-120">Nimi</span><span class="sxs-lookup"><span data-stu-id="e85e9-120">Name</span></span> | <span data-ttu-id="e85e9-121">Tarjousrivin nimi, jonka avulla voit määrittää arvioidun tarjouksen erillisen osan.</span><span class="sxs-lookup"><span data-stu-id="e85e9-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="e85e9-122">Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-123">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="e85e9-123">Billing Method</span></span> | <span data-ttu-id="e85e9-124">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä.</span><span class="sxs-lookup"><span data-stu-id="e85e9-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="e85e9-125">Tässä kentässä on kaksi pääasiallista palvelusopimusmallia, joita Dynamics 365 Project Operationsissa tuetaan:</span><span class="sxs-lookup"><span data-stu-id="e85e9-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="e85e9-126">– Kiinteä hinta</span><span class="sxs-lookup"><span data-stu-id="e85e9-126">- Fixed price</span></span></br><span data-ttu-id="e85e9-127">– Aika ja materiaali.</span><span class="sxs-lookup"><span data-stu-id="e85e9-127">- Time and material.</span></span>| <span data-ttu-id="e85e9-128">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-129">Project</span><span class="sxs-lookup"><span data-stu-id="e85e9-129">Project</span></span> | <span data-ttu-id="e85e9-130">Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="e85e9-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="e85e9-131">Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina.</span><span class="sxs-lookup"><span data-stu-id="e85e9-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="e85e9-132">Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto.</span><span class="sxs-lookup"><span data-stu-id="e85e9-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="e85e9-133">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="e85e9-134">Sisällytettävät tehtävät</span><span class="sxs-lookup"><span data-stu-id="e85e9-134">Included Tasks</span></span> | <span data-ttu-id="e85e9-135">Ilmaisee, käytetäänkö tätä tarjousriviä valitussa projektissa kaikkiin projektitehtäviin vai vain joihinkin niistä.</span><span class="sxs-lookup"><span data-stu-id="e85e9-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="e85e9-136">Tällä kentällä on seuraavat mahdolliset arvot:</span><span class="sxs-lookup"><span data-stu-id="e85e9-136">This field has the following possible values:</span></span></br><span data-ttu-id="e85e9-137">– Kaikki projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="e85e9-137">- All project tasks</span></span></br><span data-ttu-id="e85e9-138">– Vain valitut projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="e85e9-138">- Selected project tasks only</span></span></br><span data-ttu-id="e85e9-139">Tässä kentässä oleva tyhjä arvo vastaa **Kaikki projektitehtävät** -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="e85e9-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="e85e9-140">Kun **Vain valitut projektitehtävät** valitaan projektisivulla, **Tehtävien laskutuksen asetukset** -välilehdessä voit valita tiettyjä tehtäviä, jotka liitetään tähän tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="e85e9-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="e85e9-141">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-142">Sisällytä aika</span><span class="sxs-lookup"><span data-stu-id="e85e9-142">Include Time</span></span> | <span data-ttu-id="e85e9-143">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin aikatapahtumat tai työvoimakustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e85e9-144">**Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e85e9-145">**Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e85e9-146">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-147">Sisällytä kulu</span><span class="sxs-lookup"><span data-stu-id="e85e9-147">Include Expense</span></span> | <span data-ttu-id="e85e9-148">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin kulujen kustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e85e9-149">**Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e85e9-150">**Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e85e9-151">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-152">Sisällytä maksu</span><span class="sxs-lookup"><span data-stu-id="e85e9-152">Include Fee</span></span> | <span data-ttu-id="e85e9-153">**Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin maksut sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e85e9-154">**Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e85e9-155">**Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="e85e9-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e85e9-156">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-157">Tarjottu summa</span><span class="sxs-lookup"><span data-stu-id="e85e9-157">Quoted Amount</span></span> | <span data-ttu-id="e85e9-158">Tämä on summa, joka tarjotaan asiakkaalle kaikista tähän projektipohjaiseen tarjousriviin ennustetuista töistä.</span><span class="sxs-lookup"><span data-stu-id="e85e9-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="e85e9-159">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="e85e9-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="e85e9-160">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista.</span><span class="sxs-lookup"><span data-stu-id="e85e9-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="e85e9-161">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-162">Arvioitu vero</span><span class="sxs-lookup"><span data-stu-id="e85e9-162">Estimated Tax</span></span> | <span data-ttu-id="e85e9-163">Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="e85e9-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="e85e9-164">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista.</span><span class="sxs-lookup"><span data-stu-id="e85e9-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="e85e9-165">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-166">Tarjouksen summa veron jälkeen</span><span class="sxs-lookup"><span data-stu-id="e85e9-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="e85e9-167">Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="e85e9-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="e85e9-168">Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*.</span><span class="sxs-lookup"><span data-stu-id="e85e9-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="e85e9-169">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-170">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="e85e9-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="e85e9-171">Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="e85e9-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="e85e9-172">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e85e9-173">Asiakasbudjetti</span><span class="sxs-lookup"><span data-stu-id="e85e9-173">Customer Budget</span></span> | <span data-ttu-id="e85e9-174">Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="e85e9-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="e85e9-175">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="e85e9-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="e85e9-176">Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt</span><span class="sxs-lookup"><span data-stu-id="e85e9-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="e85e9-177">**Sääntö 1**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti sisällytetään tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="e85e9-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="e85e9-178">**Sääntö 2**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="e85e9-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="e85e9-179">**Sääntö 3**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Vain valitut projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää useille tarjouksen projektipohjaisille tarjousriveille.</span><span class="sxs-lookup"><span data-stu-id="e85e9-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="e85e9-180">**Sääntö 4**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.</span><span class="sxs-lookup"><span data-stu-id="e85e9-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="e85e9-181">**Sääntö 5**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="e85e9-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="e85e9-182">
                    <strong>Mahdollisuus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e85e9-183">
                    <strong>Tarjous</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e85e9-184">
                    <strong>Tarjousrivi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e85e9-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="e85e9-186">
                    <strong>Sisällytettävät tehtävät</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e85e9-187">
                    <strong>Sisällytä aika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e85e9-188">
                    <strong>Sisällytä kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e85e9-189">
                    <strong>Sisällytä</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="e85e9-190">
                    <strong>Maksu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="e85e9-191">
                    <strong>Kelpaa / ei kelpaa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="e85e9-192">
                    <strong>Syy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e85e9-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-193">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-194">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-195">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-196">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-197">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-198">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-199">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-200">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-201">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="e85e9-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-202">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="e85e9-202">Violation of Rule #2.</span></span> <span data-ttu-id="e85e9-203">P1-projektin aika, kulu ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="e85e9-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-204">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-205">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-206">QL2</span><span class="sxs-lookup"><span data-stu-id="e85e9-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-207">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-208">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-209">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-210">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-211">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-211">Yes</span></span> </p>
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
<span data-ttu-id="e85e9-212">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-213">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-214">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-215">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-216">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-217">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-218">No</span><span class="sxs-lookup"><span data-stu-id="e85e9-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-220">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="e85e9-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-221">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="e85e9-221">Violation of Rule #2.</span></span> <span data-ttu-id="e85e9-222">P1-projektin aika ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="e85e9-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-223">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-224">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-225">QL2</span><span class="sxs-lookup"><span data-stu-id="e85e9-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-226">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-227">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-228">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-229">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-230">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-230">Yes</span></span> </p>
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
<span data-ttu-id="e85e9-231">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-232">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-233">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-234">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-235">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-236">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-237">No</span><span class="sxs-lookup"><span data-stu-id="e85e9-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-238">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-239">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="e85e9-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="e85e9-240">P1-projektin aika ja maksut sisältyvät riville QL1.</span><span class="sxs-lookup"><span data-stu-id="e85e9-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="e85e9-241">Kulu P1-projektissa sisältyy riville QL2.</span><span class="sxs-lookup"><span data-stu-id="e85e9-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="e85e9-242">Kullekin tarjousriville lisätyissä kohteissa ei ole päällekkäisyyttä, ja tämä on kelvollinen.</span><span class="sxs-lookup"><span data-stu-id="e85e9-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-243">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-244">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-245">QL2</span><span class="sxs-lookup"><span data-stu-id="e85e9-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-246">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-247">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-248">No</span><span class="sxs-lookup"><span data-stu-id="e85e9-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-250">No</span><span class="sxs-lookup"><span data-stu-id="e85e9-250">No</span></span> </p>
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
<span data-ttu-id="e85e9-251">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-252">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-253">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-254">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-255">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="e85e9-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-256">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-257">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-258">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-259">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="e85e9-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-260">Säännön 2 rikkominen yllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="e85e9-261">Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="e85e9-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e85e9-262">QL2 sisältää koko projektin P1 ajan, kulut ja maksut, ja se on päällekkäinen riville Q1 sisällytettyjen kohteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="e85e9-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-263">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-264">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-265">QL2</span><span class="sxs-lookup"><span data-stu-id="e85e9-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-266">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-267">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-268">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-269">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-270">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-270">Yes</span></span> </p>
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
<span data-ttu-id="e85e9-271">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-272">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-273">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-274">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-275">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="e85e9-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-276">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-277">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-278">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-279">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="e85e9-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-280">Edellä olevan säännön 3 mukaan</span><span class="sxs-lookup"><span data-stu-id="e85e9-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="e85e9-281">Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="e85e9-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e85e9-282">QL2 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="e85e9-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e85e9-283">Ainoa lisätarkistus on QL1-rivin tehtävien alijoukolle, joka eroaa QL2-rivin tehtävien alijoukosta.</span><span class="sxs-lookup"><span data-stu-id="e85e9-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="e85e9-284">Näin varmistetaan, että päällekkäisyyksiä ei ole.</span><span class="sxs-lookup"><span data-stu-id="e85e9-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="e85e9-285">Järjestelmä suorittaa tämän, kun tehtävät on liitetty.</span><span class="sxs-lookup"><span data-stu-id="e85e9-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-286">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-287">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-288">QL2</span><span class="sxs-lookup"><span data-stu-id="e85e9-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-289">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-290">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="e85e9-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-291">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-292">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-293">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-293">Yes</span></span> </p>
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
<span data-ttu-id="e85e9-294">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-295">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-296">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-297">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-298">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-299">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-300">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-301">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e85e9-302">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="e85e9-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-303">Säännön 5 mukaan Q1 ja Q2 ovat saman mahdollisuuden kaksi tarjousta, joten ne voivat molemmat arvioida projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="e85e9-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-304">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-305">VN2</span><span class="sxs-lookup"><span data-stu-id="e85e9-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-306">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-307">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-308">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-309">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-310">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-311">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-311">Yes</span></span> </p>
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
<span data-ttu-id="e85e9-312">O1</span><span class="sxs-lookup"><span data-stu-id="e85e9-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-313">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-314">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-315">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-316">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-317">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-318">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-319">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e85e9-320">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="e85e9-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e85e9-321">Säännön 4 mukaan Q1 ja Q2 ovat eri mahdollisuuksien kaksi tarjousta, joten ne eivät voi arvioida saman projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="e85e9-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e85e9-322">O2</span><span class="sxs-lookup"><span data-stu-id="e85e9-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e85e9-323">VN1</span><span class="sxs-lookup"><span data-stu-id="e85e9-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-324">QL1</span><span class="sxs-lookup"><span data-stu-id="e85e9-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-325">K1</span><span class="sxs-lookup"><span data-stu-id="e85e9-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e85e9-326">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="e85e9-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-327">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e85e9-328">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e85e9-329">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e85e9-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e85e9-330">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="e85e9-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]