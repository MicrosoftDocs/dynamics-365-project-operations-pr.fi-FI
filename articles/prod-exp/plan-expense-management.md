---
title: Määritä käyttöoikeuksien hallinta
description: Tässä artikkelissa käsitellään suunnitteluun liittyviä seikkoja ja päätöksiä, jotka on tehtävä suunnitteluprosessin aikana ennen kulunhallinnan määrittämistä Microsoft Dynamics 365 Financessa.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271349"
---
# <a name="configure-expense-management"></a><span data-ttu-id="5cc00-103">Määritä käyttöoikeuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="5cc00-103">Configure expense management</span></span>

<span data-ttu-id="5cc00-104">Tässä aiheessa käsitellään suunnitteluun liittyviä seikkoja ja päätöksiä, jotka on tehtävä suunnitteluprosessin aikana ennen kulunhallinnan määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="5cc00-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="5cc00-105">Kulunhallinnassa voit tallentaa tietoja esimerkiksi maksutavoista, matkustusehdotuksista, kuluraporteista ja käytännöistä.</span><span class="sxs-lookup"><span data-stu-id="5cc00-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="5cc00-106">Koska monet niistä päätöksistä, joita teet, kun suunnittelet kulunhallinnan määrityksiä, perustuvat organisaation hierarkiaan ja talousrakenteeseen, sinun on viitattava kyseisten alueiden suunnitteluasiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="5cc00-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="5cc00-107">Konsernin sisäiset kulut</span><span class="sxs-lookup"><span data-stu-id="5cc00-107">Intercompany expenses</span></span>

<span data-ttu-id="5cc00-108">Kun otat konserniyritysten väliset kulut käyttöön, voit sallia, että yritykset ja työntekijät aiheuttavat kuluja toisen yrityksen puolesta, ja kerätä maksuja organisaation juridisesta työyksiköstä.</span><span class="sxs-lookup"><span data-stu-id="5cc00-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="5cc00-109">Esimerkiksi yrityksen työntekijä A täydentää projektia yritykselle B, ja projektiin liittyy matkustamiseen liittyviä kuluja.</span><span class="sxs-lookup"><span data-stu-id="5cc00-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="5cc00-110">Jos konsernin sisäiset kulut on otettu käyttöön, työntekijä voi sitten arkistoida kuluraportin, joka kirjaa kulun yritykselle B, ja tämän jälkeen yrityksen A on maksettava kulu. Jos organisaatiolla ei ole useita yrityksiä, konsernin sisäisiä kuluja ei tarvitse ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5cc00-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="5cc00-111">**Päätös:** Haluatko ottaa käyttöön konsernin sisäiset kulut?</span><span class="sxs-lookup"><span data-stu-id="5cc00-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="5cc00-112">Taloushallinto</span><span class="sxs-lookup"><span data-stu-id="5cc00-112">Financial management</span></span>

<span data-ttu-id="5cc00-113">Kulujen hallinta on integroitu tiiviisti organisaation taloushallintoon.</span><span class="sxs-lookup"><span data-stu-id="5cc00-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="5cc00-114">Monet kulun hallinnan määritykset perustuvat päätöksiin, jotka olet tehnyt organisaation taloudesta.</span><span class="sxs-lookup"><span data-stu-id="5cc00-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="5cc00-115">Seuraavissa osissa kuvataan eri alueita, jotka edellyttävät suunnittelua ja päätöksiä, organisaation talouspäätösten ja johtoryhmän ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="5cc00-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="5cc00-116">Päivärahat</span><span class="sxs-lookup"><span data-stu-id="5cc00-116">Per diems</span></span>

<span data-ttu-id="5cc00-117">Sinun täytyy määrittää työntekijän päivärahat, joita organisaatiosi tarjoaa.</span><span class="sxs-lookup"><span data-stu-id="5cc00-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="5cc00-118">Koska päivärahoja käytetään yleensä kattamaan esimerkiksi ateriat, majoitus ja muut satunnaiset kulut, voit luoda säännöt organisaation tarjouksista.</span><span class="sxs-lookup"><span data-stu-id="5cc00-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="5cc00-119">päivärahahinnat voivat perustua vuodenaikaan, matkustuspaikkaan tai molempiin.</span><span class="sxs-lookup"><span data-stu-id="5cc00-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5cc00-120">Kun määrität päivärahasäännön, voit määrittää, että prosenttiosuus päivärahahinnasta pidätetään, jos työntekijä saa ilmaisia aterioita tai palveluita.</span><span class="sxs-lookup"><span data-stu-id="5cc00-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5cc00-121">Voit myös määrittää päivärahamäärät asettamaan vähimmäis- ja enimmäistuntimäärät, joita päivärahaa voidaan soveltaa työntekijän matkoihin.</span><span class="sxs-lookup"><span data-stu-id="5cc00-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="5cc00-122">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="5cc00-122">**Decisions:**</span></span>

- <span data-ttu-id="5cc00-123">Päivärahasääntöjen oletusarvot ensimmäisinä ja viimeisinä päivinä:</span><span class="sxs-lookup"><span data-stu-id="5cc00-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="5cc00-124">Mikä on pienin tuntimäärä, jonka työntekijä voi vaatia päiväksi ja silti saada päivärahan?</span><span class="sxs-lookup"><span data-stu-id="5cc00-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="5cc00-125">Onko olemassa alennusmäärä, joka on tarjottu ateriaa varten ensimmäisenä ja viimeisenä päivänä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="5cc00-126">Jos vähennys on olemassa, mikä on vähennysprosentti?</span><span class="sxs-lookup"><span data-stu-id="5cc00-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5cc00-127">Onko olemassa alennusmäärä, joka on tarjottu hotellia varten ensimmäisenä ja viimeisenä päivänä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="5cc00-128">Jos vähennys on olemassa, mikä on vähennysprosentti?</span><span class="sxs-lookup"><span data-stu-id="5cc00-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5cc00-129">Onko olemassa alennusmäärä, joka on tarjottu muita kuluja varten, jotka tapahtuvat ensimmäisenä ja viimeisenä päivänä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="5cc00-130">Jos vähennys on olemassa, mikä on vähennysprosentti?</span><span class="sxs-lookup"><span data-stu-id="5cc00-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="5cc00-131">Oletuspäivärahasäännöt:</span><span class="sxs-lookup"><span data-stu-id="5cc00-131">Default per diem rules:</span></span>

    - <span data-ttu-id="5cc00-132">Onko kunkin aterian päiväraha-alennuksessa alennusprosentti, jos ateria on esimerkiksi maksuton?</span><span class="sxs-lookup"><span data-stu-id="5cc00-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="5cc00-133">Jos vähennys on olemassa, mikä on vähennysprosentti ateriaa kohti?</span><span class="sxs-lookup"><span data-stu-id="5cc00-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="5cc00-134">Onko aterioiden vähennys laskettu päivää kohti, matkaa kohti vai per aterioiden määrä päivässä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="5cc00-135">Onko päivärahasummat pyöristettävä säännöllisellä tavalla vai pyöristettävä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="5cc00-136">Lasketaanko päivärahat 24 tunnin jakson vai kalenteripäivän perusteella?</span><span class="sxs-lookup"><span data-stu-id="5cc00-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="5cc00-137">Sijaintiin perustuvat päiväraha säännöt:</span><span class="sxs-lookup"><span data-stu-id="5cc00-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="5cc00-138">Vaihtelevatko päivärahahinnat sijainnin mukaan?</span><span class="sxs-lookup"><span data-stu-id="5cc00-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="5cc00-139">Mitkä sijainnit sisältyvät?</span><span class="sxs-lookup"><span data-stu-id="5cc00-139">What locations are included?</span></span>
    - <span data-ttu-id="5cc00-140">Jos päivärahat vaihtelevat sijainnin mukaan, kullekin sijainnille määritetään seuraavien kulujen prosenttiosuus:</span><span class="sxs-lookup"><span data-stu-id="5cc00-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="5cc00-141">Ateriat</span><span class="sxs-lookup"><span data-stu-id="5cc00-141">Meals</span></span>
        - <span data-ttu-id="5cc00-142">Hotelli</span><span class="sxs-lookup"><span data-stu-id="5cc00-142">Hotel</span></span>
        - <span data-ttu-id="5cc00-143">Muut kulut</span><span class="sxs-lookup"><span data-stu-id="5cc00-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="5cc00-144">Kulujen hallinnan kirjauskansiot ja asiakkuudet</span><span class="sxs-lookup"><span data-stu-id="5cc00-144">Expense management journals and accounts</span></span>

<span data-ttu-id="5cc00-145">Kulujen hallinta edellyttää, että käytössä on useita päiväkirjoja ja asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="5cc00-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="5cc00-146">Sinun on esimerkiksi päätettävä, käytetäänkö samaa tiliä käteisennakko- ja luottokorttikiistoissa.</span><span class="sxs-lookup"><span data-stu-id="5cc00-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="5cc00-147">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="5cc00-147">**Decisions:**</span></span>

- <span data-ttu-id="5cc00-148">Mille kirjanpitokirjauskansiolle on kirjattu kuluraportit?</span><span class="sxs-lookup"><span data-stu-id="5cc00-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="5cc00-149">Mitä tiliä käytetään käteisennakolle?</span><span class="sxs-lookup"><span data-stu-id="5cc00-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="5cc00-150">Tuleeko käteisennakot kirjata heti?</span><span class="sxs-lookup"><span data-stu-id="5cc00-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="5cc00-151">Maksutavat</span><span class="sxs-lookup"><span data-stu-id="5cc00-151">Payment methods</span></span>

<span data-ttu-id="5cc00-152">Kun sallit työntekijöiden kulujen syntymisen yrityksen puolesta, sinun täytyy määrittää maksutavat, joita työntekijöillä on oikeus käyttää.</span><span class="sxs-lookup"><span data-stu-id="5cc00-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="5cc00-153">Voit esimerkiksi sallia työntekijöiden käyttää käteistä tai yrityksen luottokorttia.</span><span class="sxs-lookup"><span data-stu-id="5cc00-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="5cc00-154">Työntekijät voivat myös sallia henkilökohtaisten luottokorttien käytön ja hyvittää työntekijöitä.</span><span class="sxs-lookup"><span data-stu-id="5cc00-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="5cc00-155">Sinun on tehtävä seuraavat päätökset kullekin sallitulle maksutavalle.</span><span class="sxs-lookup"><span data-stu-id="5cc00-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="5cc00-156">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="5cc00-156">**Decisions:**</span></span>

- <span data-ttu-id="5cc00-157">Mitkä maksutavat ovat sallittuja?</span><span class="sxs-lookup"><span data-stu-id="5cc00-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="5cc00-158">Kuka omistaa maksutavan kulut?</span><span class="sxs-lookup"><span data-stu-id="5cc00-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="5cc00-159">Onko vastatilin tyyppiä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-159">Is there an offset account type?</span></span> <span data-ttu-id="5cc00-160">Jos vastatilintyyppi on olemassa, mikä se on?</span><span class="sxs-lookup"><span data-stu-id="5cc00-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="5cc00-161">Jos vastatilintyyppi on olemassa, mikä tili on?</span><span class="sxs-lookup"><span data-stu-id="5cc00-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="5cc00-162">Jos maksutapa on luottokortti, käytetäänkö maksutapaa vain tuotujen tapahtumien yhteydessä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="5cc00-163">Kululuokat ja jaetut luokat</span><span class="sxs-lookup"><span data-stu-id="5cc00-163">Expense categories and shared categories</span></span>

<span data-ttu-id="5cc00-164">Kun työntekijät luovat kuluraportin, kukin heidän tallentamansa kulu on liitettävä kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="5cc00-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="5cc00-165">Kululuokat johdetaan jaetuista luokista, jotka voidaan jakaa organisaation yritysten kesken.</span><span class="sxs-lookup"><span data-stu-id="5cc00-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="5cc00-166">Nämä luokat voidaan jakaa myös projektinhallintaan ja kirjanpitoon sen mukaan, miten organisaatio on määritetty.</span><span class="sxs-lookup"><span data-stu-id="5cc00-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="5cc00-167">Määritä organisaatiosi määrittelyn ja toteutusryhmän antamien ohjeiden perusteella, käytetäänkö kuluhallinnassa käytettyjä luokkia vain kulujen hallinnassa vai pitäisikö ne jakaa projektinhallinnan ja kirjanpidon sekä kuluhallinnan kesken.</span><span class="sxs-lookup"><span data-stu-id="5cc00-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="5cc00-168">Huomaa, että nämä luokat voidaan jakaa projektin ja kulun tai projektin ja tuotannon kesken, mutta ei kulujen ja tuotannon kesken.</span><span class="sxs-lookup"><span data-stu-id="5cc00-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="5cc00-169">Sinun täytyy tehdä seuraavat päätökset kullekin kululuokalle.</span><span class="sxs-lookup"><span data-stu-id="5cc00-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="5cc00-170">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="5cc00-170">**Decisions:**</span></span>

- <span data-ttu-id="5cc00-171">Mikä on kululuokka?</span><span class="sxs-lookup"><span data-stu-id="5cc00-171">What is the expense category?</span></span> <span data-ttu-id="5cc00-172">Esimerkkeinä voidaan mainita luokat lennoille, hotellille tai kilometrikorvauksille.</span><span class="sxs-lookup"><span data-stu-id="5cc00-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="5cc00-173">Voiko kululuokkaa käyttää myös projektinhallinnassa ja kirjanpidossa?</span><span class="sxs-lookup"><span data-stu-id="5cc00-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="5cc00-174">Mikä on kulutyyppi?</span><span class="sxs-lookup"><span data-stu-id="5cc00-174">What is the expense type?</span></span>
- <span data-ttu-id="5cc00-175">Mikä on kululuokan oletusmaksutapa?</span><span class="sxs-lookup"><span data-stu-id="5cc00-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="5cc00-176">Onko kululuokan kulut eriteltävä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="5cc00-177">Mikä on kululuokan oletuspäätili?</span><span class="sxs-lookup"><span data-stu-id="5cc00-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="5cc00-178">Mikä on kululuokan nimikkeen oletusarvonlisäveroryhmä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="5cc00-179">Sallitaanko kululuokalle muita maksutapoja?</span><span class="sxs-lookup"><span data-stu-id="5cc00-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="5cc00-180">Jos lisämaksutavat ovat sallittuja, mitä ne ovat?</span><span class="sxs-lookup"><span data-stu-id="5cc00-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="5cc00-181">Onko kululuokassa aliluokkia?</span><span class="sxs-lookup"><span data-stu-id="5cc00-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="5cc00-182">Jos aliluokkia on, on tehtävä myös seuraavat päätökset:</span><span class="sxs-lookup"><span data-stu-id="5cc00-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="5cc00-183">Jätetäänkö jotkin aliluokat pois veronpalautuksesta?</span><span class="sxs-lookup"><span data-stu-id="5cc00-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="5cc00-184">Mikä on aliluokkien nimikkeen arvonlisäveroryhmä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="5cc00-185">Jos kululuokkaa käytetään myös projektinhallinnassa ja kirjanpidossa, vastaa muihin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="5cc00-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="5cc00-186">Muussa tapauksessa voit siirtyä seuraavaan osaan.</span><span class="sxs-lookup"><span data-stu-id="5cc00-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="5cc00-187">Mitä kustannustilejä käytetään seuraaviin kuluihin?</span><span class="sxs-lookup"><span data-stu-id="5cc00-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="5cc00-188">Kustannus</span><span class="sxs-lookup"><span data-stu-id="5cc00-188">Cost</span></span>
    - <span data-ttu-id="5cc00-189">Palkanlaskennan kohdistus</span><span class="sxs-lookup"><span data-stu-id="5cc00-189">Payroll allocation</span></span>
    - <span data-ttu-id="5cc00-190">KET-kustannusarvo</span><span class="sxs-lookup"><span data-stu-id="5cc00-190">WIP-cost value</span></span>
    - <span data-ttu-id="5cc00-191">Kustannusnimike</span><span class="sxs-lookup"><span data-stu-id="5cc00-191">Cost-item</span></span>
    - <span data-ttu-id="5cc00-192">KET-kustannuksen arvonimike</span><span class="sxs-lookup"><span data-stu-id="5cc00-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="5cc00-193">Jaksotettu tappio</span><span class="sxs-lookup"><span data-stu-id="5cc00-193">Accrued loss</span></span>
    - <span data-ttu-id="5cc00-194">KET – jaksotettu tappio</span><span class="sxs-lookup"><span data-stu-id="5cc00-194">WIP-accrued loss</span></span>

- <span data-ttu-id="5cc00-195">Mitä tuottotilejä käytetään seuraaviin?</span><span class="sxs-lookup"><span data-stu-id="5cc00-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="5cc00-196">Laskutettu tuotto</span><span class="sxs-lookup"><span data-stu-id="5cc00-196">Invoiced revenue</span></span>
    - <span data-ttu-id="5cc00-197">Jaksotetun tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="5cc00-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="5cc00-198">KET – myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="5cc00-198">WIP-sales value</span></span>
    - <span data-ttu-id="5cc00-199">Jaksotettu tuotto – tuotanto</span><span class="sxs-lookup"><span data-stu-id="5cc00-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="5cc00-200">KET – tuotanto</span><span class="sxs-lookup"><span data-stu-id="5cc00-200">WIP-production</span></span>
    - <span data-ttu-id="5cc00-201">Jaksotettu tuotto – voitto</span><span class="sxs-lookup"><span data-stu-id="5cc00-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="5cc00-202">KET – voitto</span><span class="sxs-lookup"><span data-stu-id="5cc00-202">WIP-profit</span></span>
    - <span data-ttu-id="5cc00-203">Jaksotettu tuotto – tilaus</span><span class="sxs-lookup"><span data-stu-id="5cc00-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="5cc00-204">KET – tilaus</span><span class="sxs-lookup"><span data-stu-id="5cc00-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="5cc00-205">Verot</span><span class="sxs-lookup"><span data-stu-id="5cc00-205">Taxes</span></span>

<span data-ttu-id="5cc00-206">Jos kyseessä on kulujen liittyvä verotus, sinun täytyy määrittää, mitä kuluraporteissa on sisällytetty tai otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5cc00-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="5cc00-207">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="5cc00-207">**Decisions:**</span></span>

- <span data-ttu-id="5cc00-208">Sisältyykö liikevaihtovero kulusummiin?</span><span class="sxs-lookup"><span data-stu-id="5cc00-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="5cc00-209">Onko veronpalautus otettava käyttöön kuluina?</span><span class="sxs-lookup"><span data-stu-id="5cc00-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="5cc00-210">Kun suunnittelit pääkirjan, jos olet päättänyt käyttää USA:n myyntiveroa ja käyttää verosääntöjä, et voi ottaa kulujen veron palautumista käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5cc00-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="5cc00-211">(Jos haluat käyttää USA:n myyntiveroa ja käyttää verosääntöjä, määritä **Käytä arvon lisäveron verosääntöjä** -asetuksen arvoksi **Kyllä** .)</span><span class="sxs-lookup"><span data-stu-id="5cc00-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="5cc00-212">Käytännöt</span><span class="sxs-lookup"><span data-stu-id="5cc00-212">Policies</span></span>

<span data-ttu-id="5cc00-213">Luomalla kuluraporttikäytäntöjä voit auttaa organisaatiota säästämään aikaa ja rahaa, kun työntekijöille aiheutuu kuluja sen puolesta.</span><span class="sxs-lookup"><span data-stu-id="5cc00-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="5cc00-214">Käytännöt varmistavat, että työntekijät pysyvät budjetissa, toimittavat kaikki tarvittavat tiedot ja käyttävät rahaa vain tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="5cc00-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="5cc00-215">Sinun täytyy tehdä seuraavat päätökset kullekin kuluraporttikäytännölle ja kullekin luotavalle kuluraportin hyväksyntäkäytännölle.</span><span class="sxs-lookup"><span data-stu-id="5cc00-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="5cc00-216">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="5cc00-216">**Decisions:**</span></span>

- <span data-ttu-id="5cc00-217">Mikä on käytännön nimi?</span><span class="sxs-lookup"><span data-stu-id="5cc00-217">What is the name of the policy?</span></span>
- <span data-ttu-id="5cc00-218">Mihin kulukäytäntöä käytetään?</span><span class="sxs-lookup"><span data-stu-id="5cc00-218">What is the expense policy for?</span></span>
- <span data-ttu-id="5cc00-219">Jos olet aiemmin päättänyt ottaa käyttöön konserniyritysten väliset kulut, mitkä organisaatiosi yritykset voivat käyttää tätä käytäntöä?</span><span class="sxs-lookup"><span data-stu-id="5cc00-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="5cc00-220">Milloin käytäntö tulee voimaan?</span><span class="sxs-lookup"><span data-stu-id="5cc00-220">When does the policy become effective?</span></span>
- <span data-ttu-id="5cc00-221">Milloin käytäntö vanhenee?</span><span class="sxs-lookup"><span data-stu-id="5cc00-221">When does the policy expire?</span></span>
- <span data-ttu-id="5cc00-222">Mikä on käytäntösääntö?</span><span class="sxs-lookup"><span data-stu-id="5cc00-222">What is the policy rule?</span></span>
- <span data-ttu-id="5cc00-223">Mikä on käytäntösäännön tulos?</span><span class="sxs-lookup"><span data-stu-id="5cc00-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]