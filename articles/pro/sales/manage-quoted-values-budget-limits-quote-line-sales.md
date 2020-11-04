---
title: Projektipohjaiset tarjousrivit (Pro)
description: Tässä aiheessa on tietoja projektipohjaisten tarjousrivien käyttämisestä projektityöhön. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075278"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="99ad4-104">Projektipohjaiset tarjousrivit (Pro)</span><span class="sxs-lookup"><span data-stu-id="99ad4-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="99ad4-105">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="99ad4-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="99ad4-106">Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa.</span><span class="sxs-lookup"><span data-stu-id="99ad4-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="99ad4-107">Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:</span><span class="sxs-lookup"><span data-stu-id="99ad4-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="99ad4-108">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="99ad4-108">Billing Method</span></span>
- <span data-ttu-id="99ad4-109">Projektin ja tehtävän yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="99ad4-109">Project and Task Mapping</span></span>
- <span data-ttu-id="99ad4-110">Sisältyvät tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="99ad4-110">Included Transaction classes</span></span>
- <span data-ttu-id="99ad4-111">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="99ad4-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="99ad4-112">Veloitettavuusasetus</span><span class="sxs-lookup"><span data-stu-id="99ad4-112">Chargeability setup</span></span>
- <span data-ttu-id="99ad4-113">Arvio tarjousrivin tietojen avulla</span><span class="sxs-lookup"><span data-stu-id="99ad4-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="99ad4-114">Tarjousrivin asiakkaat</span><span class="sxs-lookup"><span data-stu-id="99ad4-114">Quote line Customers</span></span>

<span data-ttu-id="99ad4-115">Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset** -välilehden kentistä.</span><span class="sxs-lookup"><span data-stu-id="99ad4-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="99ad4-116">Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.</span><span class="sxs-lookup"><span data-stu-id="99ad4-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="99ad4-117">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="99ad4-117">**Field**</span></span> | <span data-ttu-id="99ad4-118">**Relevanssi, tarkoitus ja opastus**</span><span class="sxs-lookup"><span data-stu-id="99ad4-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="99ad4-119">**Loppupään vaikutus**</span><span class="sxs-lookup"><span data-stu-id="99ad4-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="99ad4-120">Nimi</span><span class="sxs-lookup"><span data-stu-id="99ad4-120">Name</span></span> | <span data-ttu-id="99ad4-121">Tarjousrivin nimi, jonka avulla voit määrittää arvioidun tarjouksen erillisen osan.</span><span class="sxs-lookup"><span data-stu-id="99ad4-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="99ad4-122">Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-123">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="99ad4-123">Billing Method</span></span> | <span data-ttu-id="99ad4-124">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä.</span><span class="sxs-lookup"><span data-stu-id="99ad4-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="99ad4-125">Tämä kenttä sisältää kaksi tärkeintä Dynamics 365 Project Operationsin tukemaa sopimusmallia:</span><span class="sxs-lookup"><span data-stu-id="99ad4-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="99ad4-126">– Kiinteä hinta</span><span class="sxs-lookup"><span data-stu-id="99ad4-126">- Fixed price</span></span></br><span data-ttu-id="99ad4-127">– Aika ja materiaali.</span><span class="sxs-lookup"><span data-stu-id="99ad4-127">- Time and material.</span></span>| <span data-ttu-id="99ad4-128">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-129">Project</span><span class="sxs-lookup"><span data-stu-id="99ad4-129">Project</span></span> | <span data-ttu-id="99ad4-130">Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="99ad4-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="99ad4-131">Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina.</span><span class="sxs-lookup"><span data-stu-id="99ad4-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="99ad4-132">Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto.</span><span class="sxs-lookup"><span data-stu-id="99ad4-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="99ad4-133">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="99ad4-134">Sisällytettävät tehtävät</span><span class="sxs-lookup"><span data-stu-id="99ad4-134">Included Tasks</span></span> | <span data-ttu-id="99ad4-135">Ilmaisee, käytetäänkö tätä tarjousriviä valitussa projektissa kaikkiin projektitehtäviin vai vain joihinkin niistä.</span><span class="sxs-lookup"><span data-stu-id="99ad4-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="99ad4-136">Tällä kentällä on seuraavat mahdolliset arvot:</span><span class="sxs-lookup"><span data-stu-id="99ad4-136">This field has the following possible values:</span></span></br><span data-ttu-id="99ad4-137">– Kaikki projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="99ad4-137">- All project tasks</span></span></br><span data-ttu-id="99ad4-138">– Vain valitut projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="99ad4-138">- Selected project tasks only</span></span></br><span data-ttu-id="99ad4-139">Tässä kentässä oleva tyhjä arvo vastaa **Kaikki projektitehtävät** -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="99ad4-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="99ad4-140">Kun **Vain valitut projektitehtävät** valitaan projektisivulla, **Tehtävien laskutuksen asetukset** -välilehdessä voit valita tiettyjä tehtäviä, jotka liitetään tähän tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="99ad4-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="99ad4-141">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-142">Sisällytä aika</span><span class="sxs-lookup"><span data-stu-id="99ad4-142">Include Time</span></span> | <span data-ttu-id="99ad4-143">**Kyllä**/**Ei** -merkintä osoittaa, onko valitun projektin aikatapahtumat tai työvoimakustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="99ad4-144">**Ei** -arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="99ad4-145">**Kyllä** -arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="99ad4-146">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-147">Sisällytä kulu</span><span class="sxs-lookup"><span data-stu-id="99ad4-147">Include Expense</span></span> | <span data-ttu-id="99ad4-148">**Kyllä**/**Ei** -merkintä osoittaa, onko valitun projektin kulujen kustannukset sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="99ad4-149">**Ei** -arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="99ad4-150">**Kyllä** -arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="99ad4-151">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-152">Sisällytä maksu</span><span class="sxs-lookup"><span data-stu-id="99ad4-152">Include Fee</span></span> | <span data-ttu-id="99ad4-153">**Kyllä**/**Ei** -merkintä osoittaa, onko valitun projektin maksut sisällytettävä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="99ad4-154">**Ei** -arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="99ad4-155">**Kyllä** -arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="99ad4-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="99ad4-156">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-157">Tarjottu summa</span><span class="sxs-lookup"><span data-stu-id="99ad4-157">Quoted Amount</span></span> | <span data-ttu-id="99ad4-158">Tämä on summa, joka tarjotaan asiakkaalle kaikista tähän projektipohjaiseen tarjousriviin ennustetuista töistä.</span><span class="sxs-lookup"><span data-stu-id="99ad4-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="99ad4-159">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="99ad4-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="99ad4-160">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista.</span><span class="sxs-lookup"><span data-stu-id="99ad4-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="99ad4-161">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-162">Arvioitu vero</span><span class="sxs-lookup"><span data-stu-id="99ad4-162">Estimated Tax</span></span> | <span data-ttu-id="99ad4-163">Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="99ad4-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="99ad4-164">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista.</span><span class="sxs-lookup"><span data-stu-id="99ad4-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="99ad4-165">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-166">Tarjouksen summa veron jälkeen</span><span class="sxs-lookup"><span data-stu-id="99ad4-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="99ad4-167">Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="99ad4-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="99ad4-168">Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*.</span><span class="sxs-lookup"><span data-stu-id="99ad4-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="99ad4-169">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-170">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="99ad4-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="99ad4-171">Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="99ad4-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="99ad4-172">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="99ad4-173">Asiakasbudjetti</span><span class="sxs-lookup"><span data-stu-id="99ad4-173">Customer Budget</span></span> | <span data-ttu-id="99ad4-174">Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="99ad4-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="99ad4-175">Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="99ad4-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="99ad4-176">Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt</span><span class="sxs-lookup"><span data-stu-id="99ad4-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="99ad4-177">**Sääntö 1** : Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät** , projekti sisällytetään tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="99ad4-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="99ad4-178">**Sääntö 2** : Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät** , projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="99ad4-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="99ad4-179">**Sääntö 3** : Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Vain valitut projektitehtävät** , projekti ja tietty tapahtumaluokka voidaan sisällyttää useille tarjouksen projektipohjaisille tarjousriveille.</span><span class="sxs-lookup"><span data-stu-id="99ad4-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="99ad4-180">**Sääntö 4** : Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.</span><span class="sxs-lookup"><span data-stu-id="99ad4-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="99ad4-181">**Sääntö 5** : Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="99ad4-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="99ad4-182">
                    <strong>Mahdollisuus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="99ad4-183">
                    <strong>Tarjous</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="99ad4-184">
                    <strong>Tarjousrivi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="99ad4-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="99ad4-186">
                    <strong>Sisällytettävät tehtävät</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="99ad4-187">
                    <strong>Sisällytä aika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="99ad4-188">
                    <strong>Sisällytä kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="99ad4-189">
                    <strong>Sisällytä</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="99ad4-190">
                    <strong>Maksu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="99ad4-191">
                    <strong>Kelpaa / ei kelpaa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="99ad4-192">
                    <strong>Syy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="99ad4-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-193">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-194">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-195">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-196">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-197">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-198">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-199">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-200">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-201">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="99ad4-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-202">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="99ad4-202">Violation of Rule #2.</span></span> <span data-ttu-id="99ad4-203">P1-projektin aika, kulu ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="99ad4-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-204">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-205">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-206">QL2</span><span class="sxs-lookup"><span data-stu-id="99ad4-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-207">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-208">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-209">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-210">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-211">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-211">Yes</span></span> </p>
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
<span data-ttu-id="99ad4-212">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-213">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-214">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-215">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-216">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-217">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-218">No</span><span class="sxs-lookup"><span data-stu-id="99ad4-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-220">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="99ad4-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-221">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="99ad4-221">Violation of Rule #2.</span></span> <span data-ttu-id="99ad4-222">P1-projektin aika ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).</span><span class="sxs-lookup"><span data-stu-id="99ad4-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-223">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-224">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-225">QL2</span><span class="sxs-lookup"><span data-stu-id="99ad4-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-226">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-227">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-228">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-229">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-230">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-230">Yes</span></span> </p>
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
<span data-ttu-id="99ad4-231">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-232">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-233">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-234">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-235">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-236">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-237">No</span><span class="sxs-lookup"><span data-stu-id="99ad4-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-238">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-239">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="99ad4-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="99ad4-240">P1-projektin aika ja maksut sisältyvät riville QL1.</span><span class="sxs-lookup"><span data-stu-id="99ad4-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="99ad4-241">Kulu P1-projektissa sisältyy riville QL2.</span><span class="sxs-lookup"><span data-stu-id="99ad4-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="99ad4-242">Kullekin tarjousriville lisätyissä kohteissa ei ole päällekkäisyyttä, ja tämä on kelvollinen.</span><span class="sxs-lookup"><span data-stu-id="99ad4-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-243">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-244">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-245">QL2</span><span class="sxs-lookup"><span data-stu-id="99ad4-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-246">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-247">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-248">No</span><span class="sxs-lookup"><span data-stu-id="99ad4-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-249">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-250">No</span><span class="sxs-lookup"><span data-stu-id="99ad4-250">No</span></span> </p>
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
<span data-ttu-id="99ad4-251">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-252">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-253">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-254">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-255">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="99ad4-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-256">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-257">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-258">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-259">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="99ad4-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-260">Säännön 2 rikkominen yllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="99ad4-261">Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="99ad4-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="99ad4-262">QL2 sisältää koko projektin P1 ajan, kulut ja maksut, ja se on päällekkäinen riville Q1 sisällytettyjen kohteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="99ad4-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-263">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-264">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-265">QL2</span><span class="sxs-lookup"><span data-stu-id="99ad4-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-266">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-267">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-268">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-269">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-270">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-270">Yes</span></span> </p>
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
<span data-ttu-id="99ad4-271">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-272">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-273">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-274">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-275">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="99ad4-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-276">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-277">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-278">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-279">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="99ad4-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-280">Edellä olevan säännön 3 mukaan</span><span class="sxs-lookup"><span data-stu-id="99ad4-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="99ad4-281">Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="99ad4-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="99ad4-282">QL2 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="99ad4-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="99ad4-283">Ainoa lisätarkistus on QL1-rivin tehtävien alijoukolle, joka eroaa QL2-rivin tehtävien alijoukosta.</span><span class="sxs-lookup"><span data-stu-id="99ad4-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="99ad4-284">Näin varmistetaan, että päällekkäisyyksiä ei ole.</span><span class="sxs-lookup"><span data-stu-id="99ad4-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="99ad4-285">Järjestelmä suorittaa tämän, kun tehtävät on liitetty.</span><span class="sxs-lookup"><span data-stu-id="99ad4-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-286">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-287">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-288">QL2</span><span class="sxs-lookup"><span data-stu-id="99ad4-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-289">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-290">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="99ad4-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-291">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-292">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-293">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-293">Yes</span></span> </p>
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
<span data-ttu-id="99ad4-294">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-295">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-296">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-297">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-298">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-299">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-300">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-301">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="99ad4-302">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="99ad4-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-303">Säännön 5 mukaan Q1 ja Q2 ovat saman mahdollisuuden kaksi tarjousta, joten ne voivat molemmat arvioida projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="99ad4-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-304">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-305">VN2</span><span class="sxs-lookup"><span data-stu-id="99ad4-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-306">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-307">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-308">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-309">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-310">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-311">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-311">Yes</span></span> </p>
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
<span data-ttu-id="99ad4-312">O1</span><span class="sxs-lookup"><span data-stu-id="99ad4-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-313">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-314">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-315">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-316">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-317">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-318">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-319">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="99ad4-320">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="99ad4-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="99ad4-321">Säännön 4 mukaan Q1 ja Q2 ovat eri mahdollisuuksien kaksi tarjousta, joten ne eivät voi arvioida saman projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="99ad4-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="99ad4-322">O2</span><span class="sxs-lookup"><span data-stu-id="99ad4-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="99ad4-323">VN1</span><span class="sxs-lookup"><span data-stu-id="99ad4-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-324">QL1</span><span class="sxs-lookup"><span data-stu-id="99ad4-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-325">K1</span><span class="sxs-lookup"><span data-stu-id="99ad4-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="99ad4-326">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="99ad4-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-327">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="99ad4-328">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="99ad4-329">Kyllä</span><span class="sxs-lookup"><span data-stu-id="99ad4-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="99ad4-330">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="99ad4-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

