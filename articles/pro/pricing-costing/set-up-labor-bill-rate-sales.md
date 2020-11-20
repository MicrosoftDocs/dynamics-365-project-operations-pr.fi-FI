---
title: Työn laskutushintojen määrittäminen
description: Tämä aihe sisältää tietoja työvoiman laskutushinnoista Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e6294895857442f3a24a9d73ee07d2b90926a4fb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075410"
---
# <a name="setting-up-bill-rates-for-labor-rate-billing"></a><span data-ttu-id="8bb99-103">Laskutushintojen määrittäminen työvoimahintalaskutusta varten</span><span class="sxs-lookup"><span data-stu-id="8bb99-103">Setting up bill rates for labor rate billing</span></span> 

<span data-ttu-id="8bb99-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="8bb99-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8bb99-105">Jokaisella hinnastolla on joukkoroolien hintoja tai työvoimahintoja, jotka ovat voimassa sen kontekstin ja päivämäärän mukaan, joka sisältyy hinnasto-otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="8bb99-105">Each price list has a set of role prices, or labor rates, that are effective for the context and date effectivity included on the price list header.</span></span> <span data-ttu-id="8bb99-106">Dynamics 365 Project Operationsin laskutushinnat voidaan määrittää vain yhdessä valuutassa, joka on hinnasto-otsikon valuutta.</span><span class="sxs-lookup"><span data-stu-id="8bb99-106">Bill rates for time in Dynamics 365 Project Operations can be set up in only one currency, which is the currency on the Price list header.</span></span>

1. <span data-ttu-id="8bb99-107">Jos haluat määrittää myyntihinnaston työvoimalaskujen hinnat, luo hinnasto-otsikon perusteella hinnasto.</span><span class="sxs-lookup"><span data-stu-id="8bb99-107">To set up labor bill rates for a sales price list, create a price list based on the price list header.</span></span> 
2. <span data-ttu-id="8bb99-108">Valitse **roolien hinnat** -välilehden aliruudukossa **+ Uusi roolien hinta**.</span><span class="sxs-lookup"><span data-stu-id="8bb99-108">On the **Role Prices** tab, in the subgrid, select **+ New Role Price**.</span></span> 
3. <span data-ttu-id="8bb99-109">Kirjoita **pikaluonti** -ruutuun se roolien ja organisaatioyksiköiden yhdistelmä, jolle haluat määrittää laskun hinnan.</span><span class="sxs-lookup"><span data-stu-id="8bb99-109">On the **Quick Create** pane, enter the role and organization unit combination for which you need to set up the bill rate.</span></span>

  <span data-ttu-id="8bb99-110">Seuraavassa taulukossa on sisältää **yleiset** -välilehden kentät ja roolin hintarivin **pikaluontisivu** -ruudun, joka täytyy pitää mielessä, kun luot roolihintoja myyntihinnastossa:</span><span class="sxs-lookup"><span data-stu-id="8bb99-110">The following table includes the fields on the **General** tab and the **Quick Create** pane of a role price line that you need keep in mind as you create role prices on a sales price list:</span></span>

  | <span data-ttu-id="8bb99-111">Field</span><span class="sxs-lookup"><span data-stu-id="8bb99-111">Field</span></span> | <span data-ttu-id="8bb99-112">Sijainti</span><span class="sxs-lookup"><span data-stu-id="8bb99-112">Location</span></span> | <span data-ttu-id="8bb99-113">Relevanssi, tarkoitus ja opastus</span><span class="sxs-lookup"><span data-stu-id="8bb99-113">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="8bb99-114">Loppupään vaikutus</span><span class="sxs-lookup"><span data-stu-id="8bb99-114">Downstream impact</span></span> |
  | --- | --- | --- | --- |
  | <span data-ttu-id="8bb99-115">Rooli</span><span class="sxs-lookup"><span data-stu-id="8bb99-115">Role</span></span> | <span data-ttu-id="8bb99-116">**Yleiset** -välilehti ja **pikaluonti** -ruutu</span><span class="sxs-lookup"><span data-stu-id="8bb99-116">**General** tab and **Quick Create** pane</span></span> | <span data-ttu-id="8bb99-117">Valitse rooli, jolle haluat määrittää laskun hinnan.</span><span class="sxs-lookup"><span data-stu-id="8bb99-117">Select the role that you are setting the bill rate for.</span></span> | <span data-ttu-id="8bb99-118">Saapuva arvio tai todellinen rooli sovitetaan tämän rivin kanssa roolin oletuslaskutusprosenttiin.</span><span class="sxs-lookup"><span data-stu-id="8bb99-118">Role on the incoming estimate or actual will be matched against this line to default bill rate of the role.</span></span> |
  | <span data-ttu-id="8bb99-119">Resursointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="8bb99-119">Resourcing Unit</span></span> | <span data-ttu-id="8bb99-120">**Yleiset** -välilehti ja **pikaluonti** -ruutu</span><span class="sxs-lookup"><span data-stu-id="8bb99-120">**General** tab and **Quick Create** pane</span></span> | <span data-ttu-id="8bb99-121">Valitse sen yrityksen organisaatioyksikkö tai osasto, josta osa on peräisin.</span><span class="sxs-lookup"><span data-stu-id="8bb99-121">Select the organizational unit or division of the company that the role is from.</span></span> <span data-ttu-id="8bb99-122">Kyseessä on esimerkiksi Fabrikam Intian Robotics Divisionin kehittäjä tai Fabrikam USA:n ohjelmisto-osaston kehittäjä.</span><span class="sxs-lookup"><span data-stu-id="8bb99-122">For example, a developer from the Robotics division of Fabrikam India or a developer from the Software division of Fabrikam USA.</span></span> | <span data-ttu-id="8bb99-123">Saapuvan arvion tai todellisen resurssien tarjoajayksikkö vertaa tätä riviä oletusarvoisesti roolin laskutusprosenttiin.</span><span class="sxs-lookup"><span data-stu-id="8bb99-123">The resourcing unit on the incoming estimate or actual will be matched against this line to default the bill rate of the role.</span></span> |
  | <span data-ttu-id="8bb99-124">Hinta</span><span class="sxs-lookup"><span data-stu-id="8bb99-124">Price</span></span> | <span data-ttu-id="8bb99-125">**Yleiset** -välilehti ja **pikaluonti** -ruutu</span><span class="sxs-lookup"><span data-stu-id="8bb99-125">**General** tab and **Quick Create** pane</span></span> | <span data-ttu-id="8bb99-126">Määritä roolienresurssointi- ja resursointiyksikön yhdistelmän laskutushinta.</span><span class="sxs-lookup"><span data-stu-id="8bb99-126">Set up the bill rate for the role resourcing company and resourcing unit combination.</span></span> <span data-ttu-id="8bb99-127">Esimerkiksi Fabrikam Intian kehittäjälle on määritetty 100 USD tai Fabrikam USA:n kehittäjän laskutushinta on 150 USD.</span><span class="sxs-lookup"><span data-stu-id="8bb99-127">For example, a developer from Fabrikam India has a bill rate of 100 USD or a developer from Fabrikam USA has a bill rate of 150 USD.</span></span> | <span data-ttu-id="8bb99-128">Tämä hinta on oletuslaskenta saapuvan arvion tai todellisen rivin yksikköhinnalle aika-tapahtumaluokalle.</span><span class="sxs-lookup"><span data-stu-id="8bb99-128">This price is the default bill rate on the per unit price of the incoming estimate or actual line for Time transaction class.</span></span> |
  | <span data-ttu-id="8bb99-129">Valuutta</span><span class="sxs-lookup"><span data-stu-id="8bb99-129">Currency</span></span> | <span data-ttu-id="8bb99-130">**Yleiset** -välilehti ja **pikaluonti** -ruutu</span><span class="sxs-lookup"><span data-stu-id="8bb99-130">**General** tab and **Quick Create** pane</span></span>| <span data-ttu-id="8bb99-131">Oletusarvon mukaan tämä valuutta on myyntihinnaston otsikossa oleva valuutta.</span><span class="sxs-lookup"><span data-stu-id="8bb99-131">By default, the currency value comes from the currency on the sales price list header.</span></span> <span data-ttu-id="8bb99-132">Myyntihinnastossa valuuttaa ei voi ohittaa.</span><span class="sxs-lookup"><span data-stu-id="8bb99-132">On a sales price list, the currency can't be overridden.</span></span> | <span data-ttu-id="8bb99-133">Tämä valuutta on oletusvaluutta saapuvan varsinaisen myyntirivin yksikköhinnassa aika-tapahtumaluokalle.</span><span class="sxs-lookup"><span data-stu-id="8bb99-133">This currency is the default currency on the per unit price of the incoming actual sales line for Time transaction class.</span></span> |
  | <span data-ttu-id="8bb99-134">Yksikön aikataulutus</span><span class="sxs-lookup"><span data-stu-id="8bb99-134">Unit Schedule</span></span> | <span data-ttu-id="8bb99-135">**Yleiset** -välilehti ja **pikaluonti** -ruutu</span><span class="sxs-lookup"><span data-stu-id="8bb99-135">**General** tab and **Quick Create** pane</span></span> | <span data-ttu-id="8bb99-136">Tämän yksikön aikataulun oletusarvo on aika, eikä sitä voi muuttaa roolihintaentiteetissä, koska sitä käytetään ilmaisemaan hinnat yksiköiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="8bb99-136">This unit schedule defaults to Time and can't be changed on the Role price entity because it's used to express rates by units of time.</span></span> | <span data-ttu-id="8bb99-137">Tämä kenttä ei vaikuta loppupään prosessiin.</span><span class="sxs-lookup"><span data-stu-id="8bb99-137">There is no downstream impact for this field.</span></span> |
  | <span data-ttu-id="8bb99-138">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="8bb99-138">Unit</span></span> | <span data-ttu-id="8bb99-139">**Yleiset** -välilehti ja **pikaluonti** -ruutu</span><span class="sxs-lookup"><span data-stu-id="8bb99-139">**General** tab and **Quick Create** pane</span></span> | <span data-ttu-id="8bb99-140">Yksikköarvo tulee myyntihinnasto-otsikon **Aikayksikkö** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="8bb99-140">The unit value comes from the **Time Unit** field on the sales price list header.</span></span> <span data-ttu-id="8bb99-141">Arvoa ei voi ohittaa.</span><span class="sxs-lookup"><span data-stu-id="8bb99-141">But the value can be overridden.</span></span> <span data-ttu-id="8bb99-142">Esimerkiksi Fabrikam Intian sovelluskehittäjällä on laskutushinta, joka on 1000 USD per **Intian päivä**.</span><span class="sxs-lookup"><span data-stu-id="8bb99-142">For example, a developer from Fabrikam India has bill rate of 1000 USD per **India Day**.</span></span> <span data-ttu-id="8bb99-143">Fabrikam USA:n kehittäjällä on laskutushinta 1500 USD per **USA:n päivä**.</span><span class="sxs-lookup"><span data-stu-id="8bb99-143">A developer from Fabrikam USA has a bill rate of 1500 USD per **US Day**.</span></span> | <span data-ttu-id="8bb99-144">Kun yksikköhinnan oletusarvona on saapuva arvio tai todellinen rivi, järjestelmä käyttää yksiköiden järjestelmää ja muuntamista perusyksikköinä yksikköhinnan laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="8bb99-144">When the per unit price defaults on an incoming estimate or actual line, the system uses the system of units and conversion in base units to calculate a per unit price.</span></span> <span data-ttu-id="8bb99-145">Esimerkiksi arvio on 10 **Intian päivän** verran työtä kehittäjälle Intiasta, ja Intian päiväyksikkö määritetään 10 tunniksi.</span><span class="sxs-lookup"><span data-stu-id="8bb99-145">For example, the estimate is for 10 **India Days** worth of work for a Developer from India, and the unit India Day is defined as 10 hours.</span></span> <span data-ttu-id="8bb99-146">Kun arvioriviä hinnoitellaan, sovellus laskee yksikköhinnan arvioon 1 000 USD/10 tuntia = 100 USD tunnissa.</span><span class="sxs-lookup"><span data-stu-id="8bb99-146">When pricing that estimate line, the application calculates the unit price on the estimate as 1000 USD/10 hours = 100 USD per hour.</span></span> |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a><span data-ttu-id="8bb99-147">Siirrä hinnoittelu tai määritä laskujen hinnat muiden organisaatioyksiköiden tai osastojen resursseille</span><span class="sxs-lookup"><span data-stu-id="8bb99-147">Transfer pricing or set up bill rates for resources from other organizational units or divisions</span></span> 

<span data-ttu-id="8bb99-148">Projektipohjaiset yritykset, jotka käyttävät yrityksen eri osastojen työntekijöitä projektien työstöihin.</span><span class="sxs-lookup"><span data-stu-id="8bb99-148">Project-based companies to use employees from different divisions of the company to work on projects.</span></span> <span data-ttu-id="8bb99-149">Projektit voidaan suorittaa yhdestä divisioonista samalla, kun työntekijät tai konsultit ovat peräisin samasta eri yrityksen jaoksesta.</span><span class="sxs-lookup"><span data-stu-id="8bb99-149">Projects can be executed from one division while the employees or consultants come from the same a different division of the company.</span></span> <span data-ttu-id="8bb99-150">Hanke voi myös koostua erilaisista eri divisioonien henkilöistä.</span><span class="sxs-lookup"><span data-stu-id="8bb99-150">The project could also be made up of a combination of people from different divisions.</span></span> <span data-ttu-id="8bb99-151">Project Operationsissa projektin toimituksen omistava yritys on nimeltään **hankintayksikkö**.</span><span class="sxs-lookup"><span data-stu-id="8bb99-151">In Project Operations, the company that owns the delivery of the project is called the **Contracting Unit**.</span></span> <span data-ttu-id="8bb99-152">Kaikkia muita resursseja toimittavien osastojen nimi on **resursointiyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="8bb99-152">All the other divisions that provide resources are called the **Resourcing Units**.</span></span> <span data-ttu-id="8bb99-153">Koska työvoimakustannukset vaihtelevat eri maantieteellisillä alueilla ja työmarkkinoilla eri puolilla maailmaa, työntekijöiden laskujen hinnat määritetään eri maantieteellisillä alueilla eri tavoin.</span><span class="sxs-lookup"><span data-stu-id="8bb99-153">Because of the differences in labor costs across various geographies and labor markets across the world, bill rates for labor are also set up differently for different geographies.</span></span>

<span data-ttu-id="8bb99-154">Esimerkiksi Yhdysvalloissa työskentelevä Fabrikam Intian kehittäjä laskuttaa 100 USD tunnissa.</span><span class="sxs-lookup"><span data-stu-id="8bb99-154">For example, a developer from Fabrikam India working on a US project is billed at the rate of 100 USD per hour.</span></span> <span data-ttu-id="8bb99-155">Fabrikam US USA -projektin kehittäjä laskuttaa 150 USD tunnissa.</span><span class="sxs-lookup"><span data-stu-id="8bb99-155">A developer from Fabrikam US working on US Project is billed at 150 USD per hour.</span></span>

### <a name="example-set-up-a-bill-rate"></a><span data-ttu-id="8bb99-156">Esimerkki: laskun hinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8bb99-156">Example: Set up a bill rate</span></span>

1. <span data-ttu-id="8bb99-157">Luo myyntihinnasto, jonka nimi on *Fabrikam US -laskutushinnat* , ja määritä voimassaolopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="8bb99-157">Create a sales price list called *Fabrikam US Bill Rates* , and set the date effectivity.</span></span>
2. <span data-ttu-id="8bb99-158">Kirjoita Myyntihinnasto-lomakkeeseen seuraavat hintatiedot:</span><span class="sxs-lookup"><span data-stu-id="8bb99-158">In the sales price list, enter the following rate information:</span></span>

    | <span data-ttu-id="8bb99-159">Rooli</span><span class="sxs-lookup"><span data-stu-id="8bb99-159">Role</span></span> | <span data-ttu-id="8bb99-160">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="8bb99-160">Organizational unit</span></span> | <span data-ttu-id="8bb99-161">Laskun hinta</span><span class="sxs-lookup"><span data-stu-id="8bb99-161">Bill rate</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="8bb99-162">Developer</span><span class="sxs-lookup"><span data-stu-id="8bb99-162">Developer</span></span> | <span data-ttu-id="8bb99-163">Fabrikam Intia</span><span class="sxs-lookup"><span data-stu-id="8bb99-163">Fabrikam India</span></span> | <span data-ttu-id="8bb99-164">100 $</span><span class="sxs-lookup"><span data-stu-id="8bb99-164">$100</span></span> |
    | <span data-ttu-id="8bb99-165">Developer</span><span class="sxs-lookup"><span data-stu-id="8bb99-165">Developer</span></span> | <span data-ttu-id="8bb99-166">Fabrikam Filippiinit</span><span class="sxs-lookup"><span data-stu-id="8bb99-166">Fabrikam Philippines</span></span> | <span data-ttu-id="8bb99-167">90 $</span><span class="sxs-lookup"><span data-stu-id="8bb99-167">$90</span></span> |
    | <span data-ttu-id="8bb99-168">Developer</span><span class="sxs-lookup"><span data-stu-id="8bb99-168">Developer</span></span> | <span data-ttu-id="8bb99-169">Fabrikam US</span><span class="sxs-lookup"><span data-stu-id="8bb99-169">Fabrikam US</span></span> | <span data-ttu-id="8bb99-170">150 $</span><span class="sxs-lookup"><span data-stu-id="8bb99-170">$150</span></span> |

3. <span data-ttu-id="8bb99-171">Liitä myyntihinnasto **Fabrikam USA:n laskuhinnat** projektisopimuksen projektihinnastoon tai tietylle tilille.</span><span class="sxs-lookup"><span data-stu-id="8bb99-171">Attach the sales price list, **Fabrikam US Bill Rates** to the project price list of the project contract or to a certain account.</span></span>