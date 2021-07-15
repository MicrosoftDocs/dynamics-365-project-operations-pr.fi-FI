---
title: Projektipohjaisten tarjousrivien yleiskatsaus
description: Tässä aiheessa on tietoja projektipohjaisten tarjousrivien käyttämisestä projektityöhön.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369867"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="23b8a-103">Projektipohjaisten tarjousrivien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="23b8a-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="23b8a-104">_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_</span><span class="sxs-lookup"><span data-stu-id="23b8a-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="23b8a-105">Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa.</span><span class="sxs-lookup"><span data-stu-id="23b8a-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="23b8a-106">Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:</span><span class="sxs-lookup"><span data-stu-id="23b8a-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="23b8a-107">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="23b8a-107">Billing Method</span></span>
- <span data-ttu-id="23b8a-108">Projektin ja tehtävän yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="23b8a-108">Project and Task Mapping</span></span>
- <span data-ttu-id="23b8a-109">Sisältyvät tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="23b8a-109">Included Transaction classes</span></span>
- <span data-ttu-id="23b8a-110">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="23b8a-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="23b8a-111">Veloitettavuusasetus</span><span class="sxs-lookup"><span data-stu-id="23b8a-111">Chargeability setup</span></span>
- <span data-ttu-id="23b8a-112">Arvio tarjousrivin tietojen avulla</span><span class="sxs-lookup"><span data-stu-id="23b8a-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="23b8a-113">Tarjousrivin asiakkaat</span><span class="sxs-lookup"><span data-stu-id="23b8a-113">Quote line Customers</span></span>

<span data-ttu-id="23b8a-114">Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset**-välilehden kentistä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="23b8a-115">Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.</span><span class="sxs-lookup"><span data-stu-id="23b8a-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="23b8a-116">**Kenttä**</span><span class="sxs-lookup"><span data-stu-id="23b8a-116">**Field**</span></span> | <span data-ttu-id="23b8a-117">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="23b8a-117">**Description**</span></span> | <span data-ttu-id="23b8a-118">**Loppupään vaikutus**</span><span class="sxs-lookup"><span data-stu-id="23b8a-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="23b8a-119">Nimi</span><span class="sxs-lookup"><span data-stu-id="23b8a-119">Name</span></span> | <span data-ttu-id="23b8a-120">Sen tarjousrivin nimi, joka auttaa tunnistamaan arvioitavan tarjouksen erillisen osan.</span><span class="sxs-lookup"><span data-stu-id="23b8a-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="23b8a-121">Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-122">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="23b8a-122">Billing Method</span></span> | <span data-ttu-id="23b8a-123">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="23b8a-124">Tässä kentässä on kaksi pääasiallista palvelusopimusmallia, joita Dynamics 365 Project Operationsissa tuetaan:</span><span class="sxs-lookup"><span data-stu-id="23b8a-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="23b8a-125">– Kiinteä hinta</span><span class="sxs-lookup"><span data-stu-id="23b8a-125">- Fixed price</span></span></br><span data-ttu-id="23b8a-126">– Aika ja materiaali.</span><span class="sxs-lookup"><span data-stu-id="23b8a-126">- Time and material.</span></span>| <span data-ttu-id="23b8a-127">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-128">Project</span><span class="sxs-lookup"><span data-stu-id="23b8a-128">Project</span></span> | <span data-ttu-id="23b8a-129">Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="23b8a-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="23b8a-130">Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina.</span><span class="sxs-lookup"><span data-stu-id="23b8a-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="23b8a-131">Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto.</span><span class="sxs-lookup"><span data-stu-id="23b8a-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="23b8a-132">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="23b8a-133">Sisällytettävät tehtävät</span><span class="sxs-lookup"><span data-stu-id="23b8a-133">Included Tasks</span></span> | <span data-ttu-id="23b8a-134">Ilmaisee, käytetäänkö tätä tarjousriviä valitussa projektissa kaikkiin projektitehtäviin vai vain joihinkin niistä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="23b8a-135">Tällä kentällä on seuraavat mahdolliset arvot:</span><span class="sxs-lookup"><span data-stu-id="23b8a-135">This field has the following possible values:</span></span></br><span data-ttu-id="23b8a-136">– Kaikki projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="23b8a-136">- All project tasks</span></span></br><span data-ttu-id="23b8a-137">– Vain valitut projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="23b8a-137">- Selected project tasks only</span></span></br><span data-ttu-id="23b8a-138">Tässä kentässä oleva tyhjä arvo vastaa **Kaikki projektitehtävät** -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="23b8a-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="23b8a-139">Kun projektisivulla valitaan **Vain valitut projektitehtävät**, **Tehtävän laskutuksen asetukset** -välilehdessä voidaan valita tiettyjä tehtäviä, jotka liitetään tähän tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="23b8a-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="23b8a-140">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-141">Sisällytä aika</span><span class="sxs-lookup"><span data-stu-id="23b8a-141">Include Time</span></span> | <span data-ttu-id="23b8a-142">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin aikatapahtumat tai työvoimakustannukset arvioon tällä tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-143">**Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="23b8a-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-144">**Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="23b8a-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="23b8a-145">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-146">Sisällytä kulu</span><span class="sxs-lookup"><span data-stu-id="23b8a-146">Include Expense</span></span> | <span data-ttu-id="23b8a-147">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin kulukustannukset arvioon tällä tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-148">**Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="23b8a-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-149">**Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="23b8a-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="23b8a-150">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-151">Sisällytä materiaali</span><span class="sxs-lookup"><span data-stu-id="23b8a-151">Include Material</span></span> | <span data-ttu-id="23b8a-152">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin materiaalikustannukset arvioon tällä tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-153">**Ei**-arvo ilmaisee, että materiaalikustannuksia ei sisällytetä arvioon tällä tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-154">**Kyllä**-arvo ilmaisee, että materiaalikustannukset sisällytetään arvioon tällä tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="23b8a-155">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-156">Sisällytä maksu</span><span class="sxs-lookup"><span data-stu-id="23b8a-156">Include Fee</span></span> | <span data-ttu-id="23b8a-157">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin maksut arvioon tällä tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-158">**Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="23b8a-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="23b8a-159">**Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon.</span><span class="sxs-lookup"><span data-stu-id="23b8a-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="23b8a-160">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-161">Tarjottu summa</span><span class="sxs-lookup"><span data-stu-id="23b8a-161">Quoted Amount</span></span> | <span data-ttu-id="23b8a-162">Tämä on summa, joka annetaan tarjouksena asiakkaalle projektipohjaisella tarjousrivillä ennustetusta työstä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="23b8a-163">Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="23b8a-164">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista.</span><span class="sxs-lookup"><span data-stu-id="23b8a-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="23b8a-165">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-166">Arvioitu vero</span><span class="sxs-lookup"><span data-stu-id="23b8a-166">Estimated Tax</span></span> | <span data-ttu-id="23b8a-167">Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="23b8a-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="23b8a-168">Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista.</span><span class="sxs-lookup"><span data-stu-id="23b8a-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="23b8a-169">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-170">Tarjouksen summa veron jälkeen</span><span class="sxs-lookup"><span data-stu-id="23b8a-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="23b8a-171">Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="23b8a-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="23b8a-172">Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*.</span><span class="sxs-lookup"><span data-stu-id="23b8a-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="23b8a-173">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-174">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="23b8a-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="23b8a-175">Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="23b8a-176">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23b8a-177">Asiakasbudjetti</span><span class="sxs-lookup"><span data-stu-id="23b8a-177">Customer Budget</span></span> | <span data-ttu-id="23b8a-178">Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="23b8a-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="23b8a-179">Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="23b8a-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="23b8a-180">Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt</span><span class="sxs-lookup"><span data-stu-id="23b8a-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="23b8a-181">**Sääntö 1**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti sisällytetään tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="23b8a-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="23b8a-182">**Sääntö 2**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="23b8a-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="23b8a-183">**Sääntö 3**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Vain valitut projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää useille tarjouksen projektipohjaisille tarjousriveille.</span><span class="sxs-lookup"><span data-stu-id="23b8a-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="23b8a-184">**Sääntö 4**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.</span><span class="sxs-lookup"><span data-stu-id="23b8a-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="23b8a-185">**Sääntö 5**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="23b8a-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="23b8a-186">
                    <strong>Mahdollisuus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="23b8a-187">
                    <strong>Tarjous</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="23b8a-188">
                    <strong>Tarjousrivi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="23b8a-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="23b8a-190">
                    <strong>Sisällytettävät tehtävät</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="23b8a-191">
                    <strong>Sisällytä aika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="23b8a-192">
                    <strong>Sisällytä kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="23b8a-193">
                    <strong>Sisällytä materiaali</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="23b8a-194">
                    <strong>Sisällytä</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="23b8a-195">
                    <strong>Maksu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="23b8a-196">
                    <strong>Kelpaa / ei kelpaa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="23b8a-197">
                    <strong>Syy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23b8a-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-198">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-199">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-200">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-201">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-202">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-203">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-204">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-205">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-206">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-207">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="23b8a-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-208">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="23b8a-208">Violation of Rule #2.</span></span> <span data-ttu-id="23b8a-209">P1-projektin aika, kulu ja maksut sisältyvät tarjousriveille QL1 ja QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-210">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-211">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-212">QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-213">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-214">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-215">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-216">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-217">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-218">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-219">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-220">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-221">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-222">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-223">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-224">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-225">No</span><span class="sxs-lookup"><span data-stu-id="23b8a-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-226">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-227">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-228">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="23b8a-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-229">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="23b8a-229">Violation of Rule #2.</span></span> <span data-ttu-id="23b8a-230">P1-projektin aika, materiaali ja maksut sisältyvät tarjousriveille QL1 ja QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-231">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-232">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-233">QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-234">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-235">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-236">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-237">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-238">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-239">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-240">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-241">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-242">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-243">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-244">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-245">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-246">No</span><span class="sxs-lookup"><span data-stu-id="23b8a-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-247">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-248">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-249">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="23b8a-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-250">P1-projektin aika, materiaali ja maksut sisältyvät QL1:een.</span><span class="sxs-lookup"><span data-stu-id="23b8a-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="23b8a-251">Kulu P1-projektissa sisältyy riville QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="23b8a-252">Tarjousriveillä ei ole päällekkäisyyksiä, joten ne ovat kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="23b8a-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-253">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-254">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-255">QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-256">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-257">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-258">No</span><span class="sxs-lookup"><span data-stu-id="23b8a-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-259">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-260">No</span><span class="sxs-lookup"><span data-stu-id="23b8a-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-261">No</span><span class="sxs-lookup"><span data-stu-id="23b8a-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-262">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-263">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-264">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-265">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-266">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="23b8a-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-267">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-268">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-269">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-270">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-271">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="23b8a-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-272">Rikkoo sääntöä 2</span><span class="sxs-lookup"><span data-stu-id="23b8a-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="23b8a-273">Q1 sisältää projektin P1 tehtävien alijoukon ajan, materiaalin, kulut ja maksut</span><span class="sxs-lookup"><span data-stu-id="23b8a-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="23b8a-274">QL2 sisältää koko projektin P1 ajan, kulut ja maksut, joten se on päällekkäinen Q1:n sisällön kanssa.</span><span class="sxs-lookup"><span data-stu-id="23b8a-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-275">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-276">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-277">QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-278">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-279">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-280">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-281">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-282">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-283">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-284">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-285">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-286">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-287">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-288">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="23b8a-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-289">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-290">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-291">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-292">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-293">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="23b8a-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-294">Säännön 3 perusteella,</span><span class="sxs-lookup"><span data-stu-id="23b8a-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="23b8a-295">Q1 sisältää projektin P1 tehtävien alijoukon ajan, materiaalin, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="23b8a-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="23b8a-296">QL2 sisältää projektin P1 tehtävien alijoukon ajan, materiaalin, kulut, ja maksut.</span><span class="sxs-lookup"><span data-stu-id="23b8a-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="23b8a-297">Ainoa lisätarkistus koskee QL1-tehtävien alijoukkoa, joka eroaa QL2:n tehtävien alijoukosta. Näin voidaan varmistaa, että QL2-tehtävissä ei ole päällekkäisyyksiä.</span><span class="sxs-lookup"><span data-stu-id="23b8a-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="23b8a-298">Järjestelmä suorittaa tämän, kun tehtävät on liitetty.</span><span class="sxs-lookup"><span data-stu-id="23b8a-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-299">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-300">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-301">QL2</span><span class="sxs-lookup"><span data-stu-id="23b8a-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-302">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-303">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="23b8a-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-304">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-305">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-306">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-307">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-308">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-309">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-310">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-311">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-312">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-313">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-314">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-315">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-316">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-317">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="23b8a-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-318">Säännön 5 mukaan Q1 ja Q2 ovat kaksi tarjousta samalle mahdollisuudelle, joten ne voivat arvioida samoja projektin osia.</span><span class="sxs-lookup"><span data-stu-id="23b8a-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-319">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-320">VN2</span><span class="sxs-lookup"><span data-stu-id="23b8a-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-321">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-322">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-323">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-324">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-325">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-326">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-327">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-328">O1</span><span class="sxs-lookup"><span data-stu-id="23b8a-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-329">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-330">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-331">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-332">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-333">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-334">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-335">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-336">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-337">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="23b8a-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23b8a-338">Säännön 4 mukaan Q1 ja Q2 ovat kaksi tarjousta eri mahdollisuudelle, joten ne eivät voi arvioida saman projektin samoja osia.</span><span class="sxs-lookup"><span data-stu-id="23b8a-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="23b8a-339">O2</span><span class="sxs-lookup"><span data-stu-id="23b8a-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="23b8a-340">VN1</span><span class="sxs-lookup"><span data-stu-id="23b8a-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="23b8a-341">QL1</span><span class="sxs-lookup"><span data-stu-id="23b8a-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-342">K1</span><span class="sxs-lookup"><span data-stu-id="23b8a-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="23b8a-343">Kaikki projektitehtävät tai tyhjä</span><span class="sxs-lookup"><span data-stu-id="23b8a-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="23b8a-344">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="23b8a-345">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="23b8a-346">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23b8a-347">Kyllä</span><span class="sxs-lookup"><span data-stu-id="23b8a-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
