---
title: Projektipohjaisten sopimusrivien yleiskatsaus
description: Tässä aiheessa on tietoja projektipohjaisten sopimusrivien käyttämisestä.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858154"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="3c1fe-103">Projektipohjaisten sopimusrivien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="3c1fe-103">Project-based contract lines overview</span></span>

<span data-ttu-id="3c1fe-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="3c1fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3c1fe-105">Dynamics 365 Project Operationsin projektipohjaiset sopimusrivit on suunniteltu sisältämään sitoumuksen projektityön tiettyjen komponenttien arvio- ja laskutussopimukset.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="3c1fe-106">Projektipohjaisen sopimusrivin rakenne on laajennettu projektin arviointi- ja laskutusskenaarioihin seuraavien käsitteiden avulla:</span><span class="sxs-lookup"><span data-stu-id="3c1fe-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="3c1fe-107">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="3c1fe-107">Billing method</span></span>
- <span data-ttu-id="3c1fe-108">Projektin ja tehtävän yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="3c1fe-108">Project and task mapping</span></span>
- <span data-ttu-id="3c1fe-109">Sisältyvät tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="3c1fe-109">Included transaction classes</span></span>
- <span data-ttu-id="3c1fe-110">Ei-ylitettävä rajoitus</span><span class="sxs-lookup"><span data-stu-id="3c1fe-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="3c1fe-111">Veloitettavuusasetus</span><span class="sxs-lookup"><span data-stu-id="3c1fe-111">Chargeability setup</span></span>
- <span data-ttu-id="3c1fe-112">Sopimusrivin tietoja käyttävät arviot</span><span class="sxs-lookup"><span data-stu-id="3c1fe-112">Estimates using contract line details</span></span>
- <span data-ttu-id="3c1fe-113">Sopimusrivin asiakkaat</span><span class="sxs-lookup"><span data-stu-id="3c1fe-113">Contract line customers</span></span>

<span data-ttu-id="3c1fe-114">Seuraavassa taulukossa on projektipohjaisten sopimusrivien **Yleiset**-välilehden kenttiä, joilla määritetään tarkka ja perusteellinen pohja projektipohjaisen työn arvio- ja laskutussopimuksille.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="3c1fe-115">Field</span><span class="sxs-lookup"><span data-stu-id="3c1fe-115">Field</span></span> | <span data-ttu-id="3c1fe-116">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3c1fe-116">Description</span></span> | <span data-ttu-id="3c1fe-117">Loppupään vaikutus</span><span class="sxs-lookup"><span data-stu-id="3c1fe-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3c1fe-118">**Nimi**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-118">**Name**</span></span> | <span data-ttu-id="3c1fe-119">Sopimusrivin nimi.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-119">Name of the contract line.</span></span> <span data-ttu-id="3c1fe-120">Se määrittää sopimuksen arvioitavan komponentin.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="3c1fe-121">Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavasta projektipohjaisen tarjousrivin arvosta.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="3c1fe-122">Nimi kopioidaan tältä sopimusriviltä luodulle projektin laskuriville, kun lasku luodaan.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="3c1fe-123">**Laskutustapa**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-123">**Billing Method**</span></span> | <span data-ttu-id="3c1fe-124">Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavasta tarjousrivin kentästä.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="3c1fe-125">Tämä asetusjoukko ilmaisee kaksi tärkeintä Project Operationsin tukemaa sopimusmallia:</span><span class="sxs-lookup"><span data-stu-id="3c1fe-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="3c1fe-126">- **Kiinteä hinta**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-126">- **Fixed Price**</span></span></br><span data-ttu-id="3c1fe-127">- **Aika ja materiaalit**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-127">- **Time and Material**</span></span> | <span data-ttu-id="3c1fe-128">Varsinainen tapahtuma käsitellään viitatun sopimusrivin laskutustavan perusteella.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="3c1fe-129">Jos sen sopimusrivin, johon todellinen arvo viittaa, laskutustapana on aika ja materiaali, kustannusten ja laskuttamaton todellisen myynnin tietueet luodaan.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="3c1fe-130">Jos sen sopimusrivin, johon todellinen arvo viittaa, laskutustapa on kiinteä hinta, vain todellinen kustannus luodaan.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="3c1fe-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-131">**Project**</span></span> | <span data-ttu-id="3c1fe-132">Tämän kentän avulla voi määrittää projektin, jonka avulla toimitetaan tämän sitoumuksen työ.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="3c1fe-133">Arvoa käytetään yhdessä **Sisällytetyt tehtävät** - ja **Sisällytetyt tapahtumaluokat** -arvojen kanssa, kun sopimusriviviittaus ratkaistaan toteutuneiden tai arviorivitietueiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="3c1fe-134">**Sisällytettävät tehtävät**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-134">**Included Tasks**</span></span> | <span data-ttu-id="3c1fe-135">Ilmaisee, sisältääkö tämä sopimusrivi valitun projektin kaikki projektitehtävät vai vain tehtävien alijoukon.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="3c1fe-136">Tällä asetusjoukolla on seuraavat mahdolliset arvot:</span><span class="sxs-lookup"><span data-stu-id="3c1fe-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="3c1fe-137">- **Kaikki projektitehtävät**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-137">- **All Project Tasks**</span></span></br><span data-ttu-id="3c1fe-138">- **Vain valitut projektitehtävät**.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="3c1fe-139">Tyhjä arvo tässä kentässä vastaa vaihtoehdon **Kaikki projektitehtävät** valintaa.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="3c1fe-140">Jos **Vain valitut tehtävät** valitaan, voi valita tietyt tehtävät ja liittää ne tähän sopimusriviin **Projekti**-sivun **Tehtävän laskutuksen asetukset** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="3c1fe-141">Tätä arvoa käytetään yhdessä **Projekti**- ja **Sisällytettävät tapahtumaluokat** -luokkien kanssa selvittämään sopimusriviviittaus todellisen arvon tai arvion rivitietueessa.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="3c1fe-142">**Sisällytä aika**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-142">**Include Time**</span></span> | <span data-ttu-id="3c1fe-143">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin aikatapahtumat tai työvoimakustannukset tähän sopimusriviin.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="3c1fe-144">**Ei**-arvo ilmaisee, että aikatapahtumia tai työkustannuksia ei sisällytetä sopimusriville.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="3c1fe-145">**Kyllä**-arvo ilmaisee, että ne sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="3c1fe-146">Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="3c1fe-147">**Sisällytä kulu**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-147">**Include Expense**</span></span> | <span data-ttu-id="3c1fe-148">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin kulutapahtumat tähän sopimusriviin.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="3c1fe-149">**Ei**-arvo ilmaisee, että kulukustannuksia ei sisällytetä sopimusriville.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="3c1fe-150">**Kyllä**-arvo ilmaisee, että se sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="3c1fe-151">Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="3c1fe-152">**Sisällytä materiaalit**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-152">**Include Materials**</span></span> | <span data-ttu-id="3c1fe-153">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin materiaalikustannukset tähän sopimusriviin.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="3c1fe-154">**Ei**-arvo ilmaisee, että materiaalikustannuksia ei sisällytetä tähän sopimusriviin.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="3c1fe-155">**Kyllä**-arvo ilmaisee, että se sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="3c1fe-156">Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="3c1fe-157">**Sisällytä maksu**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-157">**Include Fee**</span></span> | <span data-ttu-id="3c1fe-158">**Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin maksut tähän sopimusriviin.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="3c1fe-159">**Ei**-arvo ilmaisee, että maksuja ei sisällytetä sopimusriville.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="3c1fe-160">**Kyllä**-arvo ilmaisee, että ne sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="3c1fe-161">Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="3c1fe-162">**Palvelusopimuksen summa**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-162">**Contracted Amount**</span></span> | <span data-ttu-id="3c1fe-163">Kiinteähintaisella sopimusrivillä tämä summa on sovittu arvo, joka asiakkaalle laskutetaan kaikesta tähän sopimusriviin liitetyistä työkomponenteista.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="3c1fe-164">Ajan ja materiaalin sopimusrivillä tämä summa on arvio siitä, mitä asiakkaalle laskutetaan kaikesta tähän sopimusriviin liitetyistä työkomponenteista.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="3c1fe-165">Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavan tarjousrivin kentästä.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="3c1fe-166">Jos projektipohjaisella sopimusrivillä on tietoja, kenttä on lukittu eikä sitä voi muokata ja sen arvo saadaan sopimusrivin tietojen summasta.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="3c1fe-167">Jos sopimusrivillä on rivitietoja, tätä arvoa voi muokata muuttamalla rivitietojen summia.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="3c1fe-168">Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan summa ennen veroja säännöllisinä välitavoitteiden laskutusajankohtina.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="3c1fe-169">**Arvioitu vero**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-169">**Estimated Tax**</span></span> | <span data-ttu-id="3c1fe-170">Käyttäjä voi muokata tätä kenttää antamalla arvioidun verosumman sopimusrivillä.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="3c1fe-171">Jos projektipohjaisella sopimusrivillä on tietoja, kenttä on lukittu eikä sitä voi muokata ja sen arvo saadaan sopimusrivin tietojen verosummasta.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="3c1fe-172">Jos sopimusrivillä on rivitietoja, tätä arvoa voi muokata muuttamalla rivitietojen verosummia.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="3c1fe-173">Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan vero säännöllisinä välitavoitteiden laskutusajankohtina.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="3c1fe-174">**Palvelusopimuksen summa veron jälkeen**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="3c1fe-175">Sopimusrivin summa veron jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-175">The contract line amount after tax.</span></span> <span data-ttu-id="3c1fe-176">Tämä kenttä on vain luku -muotoinen, ja se lasketaan kaavalla **Palvelusopimuksen summa + Vero**.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="3c1fe-177">Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan säännölliset välitavoitteiden laskutukset.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="3c1fe-178">**Ei-ylitettävä rajoitus**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="3c1fe-179">Käyttäjä voi muokata tätä kenttää, ja se on käytettävissä vain niillä projektipohjaisilla sopimusriveillä, joissa on laskutustavaksi on määritetty aika ja materiaali.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="3c1fe-180">Käyttäjä voi muokata tätä kenttää.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-180">The user can edit this field.</span></span> <span data-ttu-id="3c1fe-181">Kun ajan tai materiaalin todellinen arvo käyttää viittauksena tämän sopimusrivin aikaa ja materiaalia, todellisen arvon summaa verrataan tämän sopimusrivin ei-ylitettävään rajoitukseen sopimusrivillä.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="3c1fe-182">Tämä arviointi on valmis, kun jo käytetyt ja varatut summat on otettu huomioon.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="3c1fe-183">**Asiakasbudjetti**</span><span class="sxs-lookup"><span data-stu-id="3c1fe-183">**Customer Budget**</span></span> | <span data-ttu-id="3c1fe-184">Tätä kenttää voi muokata ja se kopioidaan tarjousrivin vastaavasta kentästä, jos palvelusopimus on luotu tarjouksesta.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="3c1fe-185">Tämä kenttä on tarkoitettu vain tiedoksi eikä se vaikuta muihin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="3c1fe-186">Projektipohjaisten sopimusrivien Yleiset-välilehden asetusten vahvistussäännöt</span><span class="sxs-lookup"><span data-stu-id="3c1fe-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="3c1fe-187">Sääntö 1: jos **Sisällytettävät tehtävät** -kenttä on tyhjä tai sen määrityksenä on **Kaikki projektitehtävät**, kaikki projektin tehtävät sisällytetään sopimusrivillä.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="3c1fe-188">Sääntö 2: jos **Sisällytettävät tehtävät** -kenttä on tyhjä tai sen määrityksenä on **Kaikki projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhdelle sopimuksen projektipohjaiselle sopimusriville.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="3c1fe-189">Sääntö 3: jos **Sisällytettävät tehtävät** -kenttä on tyhjä tai sen määrityksenä on **Vain valitut projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää useille sopimuksen projektipohjaisille sopimusriveille.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="3c1fe-190">
                    <strong>Sopimus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3c1fe-191">
                    <strong>Palvelusopimuksen rivi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="3c1fe-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="3c1fe-193">
                    <strong>Sisällytettävät tehtävät</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="3c1fe-194">
                    <strong>Sisällytä aika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="3c1fe-195">
                    <strong>Sisällytä kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="3c1fe-196">
                    <strong>Sisällytä materiaalit</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="3c1fe-197">
                    <strong>Sisällytä</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="3c1fe-198">
                    <strong>Maksu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="3c1fe-199">
                    <strong>Kelpaa / ei kelpaa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="3c1fe-200">
                    <strong>Syy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3c1fe-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-201">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-202">SR1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-203">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-204">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-205">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-206">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-207">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-208">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-209">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="3c1fe-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-210">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-210">Violation of Rule #2.</span></span> <span data-ttu-id="3c1fe-211">P1-projektin aika, kulut, materiaalit ja maksut sisältyvät sekä sopimusriveille CL1 että CL2.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-212">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-213">SR2</span><span class="sxs-lookup"><span data-stu-id="3c1fe-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-214">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-215">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-216">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-217">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-218">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-220">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-221">SR1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-222">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-223">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-224">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-225">No</span><span class="sxs-lookup"><span data-stu-id="3c1fe-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-226">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-227">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-228">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="3c1fe-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-229">Säännön 2 rikkominen.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-229">Violation of Rule #2.</span></span> <span data-ttu-id="3c1fe-230">P1-projektin aika, materiaalit ja maksut sisältyvät sekä sopimusriveille CL1 että CL2.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-231">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-232">SR2</span><span class="sxs-lookup"><span data-stu-id="3c1fe-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-233">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-234">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-235">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-236">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-237">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-238">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-239">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-240">SR1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-241">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-242">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-243">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-244">No</span><span class="sxs-lookup"><span data-stu-id="3c1fe-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-245">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-246">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-247">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="3c1fe-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-248">P1-projektin aika, materiaalit ja maksut sisältyvät CL1:een.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="3c1fe-249">Kulu P1-projektissa sisältyy riville CL2.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="3c1fe-250">Sopimusriveillä ei ole päällekkäisyyksiä, joten ne ovat kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-251">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-252">SR2</span><span class="sxs-lookup"><span data-stu-id="3c1fe-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-253">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-254">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-255">No</span><span class="sxs-lookup"><span data-stu-id="3c1fe-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-256">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-257">No</span><span class="sxs-lookup"><span data-stu-id="3c1fe-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-258">No</span><span class="sxs-lookup"><span data-stu-id="3c1fe-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-259">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-260">SR1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-261">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-262">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="3c1fe-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-263">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-264">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-265">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-266">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-267">Ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="3c1fe-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-268">Rikkoo sääntöä 2</span><span class="sxs-lookup"><span data-stu-id="3c1fe-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="3c1fe-269">C1 sisältää projektin P1 tehtävien alijoukon ajan, materiaalit, kulut ja maksut.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="3c1fe-270">CL2 sisältää koko projektin P1 ajan, materiaalit, kulut ja maksut, joten se on päällekkäinen C1:n kanssa.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-271">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-272">SR2</span><span class="sxs-lookup"><span data-stu-id="3c1fe-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-273">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-274">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-275">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-276">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-277">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-278">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-279">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-280">SR1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-281">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-282">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="3c1fe-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-283">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-284">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-285">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-286">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-287">Kelvollinen</span><span class="sxs-lookup"><span data-stu-id="3c1fe-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3c1fe-288">Säännön 3 perusteella</span><span class="sxs-lookup"><span data-stu-id="3c1fe-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="3c1fe-289">C1 sisältää projektin P1 tehtävien alijoukon ajan, kulut, materiaalit, ja maksut.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="3c1fe-290">CL2 sisältää projektin P1 tehtävien alijoukon ajan, kulut, materiaalit, ja maksut.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="3c1fe-291">Ainoa lisätarkistus koskee CL1-tehtävien alijoukkoa, joka eroaa CL2:n tehtävien alijoukosta. Näin voidaan varmistaa, että CL2-tehtävissä ei ole päällekkäisiä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="3c1fe-292">Järjestelmä suorittaa tämän, kun tehtävät on liitetty.</span><span class="sxs-lookup"><span data-stu-id="3c1fe-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="3c1fe-293">S1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3c1fe-294">SR2</span><span class="sxs-lookup"><span data-stu-id="3c1fe-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-295">K1</span><span class="sxs-lookup"><span data-stu-id="3c1fe-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="3c1fe-296">Vain valitut tehtävät</span><span class="sxs-lookup"><span data-stu-id="3c1fe-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-297">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="3c1fe-298">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-299">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="3c1fe-300">Kyllä</span><span class="sxs-lookup"><span data-stu-id="3c1fe-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
