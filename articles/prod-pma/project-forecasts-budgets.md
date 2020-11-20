---
title: Projektiennusteet ja -budjetit
description: Microsoft Dynamics 365 Finance tarjoaa projektiennusteita ja projektibudjetteja projektien hallintaa ja valvontaa varten.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075461"
---
# <a name="project-forecasts-and-budgets"></a><span data-ttu-id="18a50-103">Projektiennusteet ja -budjetit</span><span class="sxs-lookup"><span data-stu-id="18a50-103">Project forecasts and budgets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18a50-104">Projektinhallintaan on kaksi tapaa: projektiennusteet ja projektibudjetit.</span><span class="sxs-lookup"><span data-stu-id="18a50-104">There are two ways to manage and control your projects: project forecasts and project budgets.</span></span> 

<span data-ttu-id="18a50-105">Voit käyttää projektiennusteita, jos organisaatiollasi on operatiivinen perspektiivi ja jos se keskittyy tuottoihin ja kustannuksiin, jotka johdetaan tietyistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="18a50-105">Use project forecasting if your organization has an operational perspective, and if it focuses on revenues and costs that are derived from specific transactions.</span></span> <span data-ttu-id="18a50-106">Käytä projektibudjetointia, jos organisaatiosi keskittyy enemmän rahamääriin.</span><span class="sxs-lookup"><span data-stu-id="18a50-106">Use project budgeting if your organization focuses more on the financial amounts.</span></span> 

<span data-ttu-id="18a50-107">Sekä projektiennusteet että projektibudjetit käyttävät ennustemalleja suunniteltujen tapahtumasummien määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="18a50-107">Both project forecasts and project budgets use forecast models to hold the projected transaction amounts.</span></span> 

<span data-ttu-id="18a50-108">Kullakin tavalla on etunsa.</span><span class="sxs-lookup"><span data-stu-id="18a50-108">Each method has its advantages.</span></span> <span data-ttu-id="18a50-109">Ota huomioon seuraavat seikat, ennen kuin valitset menetelmän organisaatiollesi.</span><span class="sxs-lookup"><span data-stu-id="18a50-109">You should consider the following points before you select a method for your organization.</span></span>

|   <span data-ttu-id="18a50-110">Kohdistustapa</span><span class="sxs-lookup"><span data-stu-id="18a50-110">Allocation method</span></span>       |           <span data-ttu-id="18a50-111">Projektin ennustaminen</span><span class="sxs-lookup"><span data-stu-id="18a50-111">Project forecasting</span></span>            |        <span data-ttu-id="18a50-112">Projektin budjetointi</span><span class="sxs-lookup"><span data-stu-id="18a50-112">Project budgeting</span></span>                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="18a50-113">**Jaksokohdistus**</span><span class="sxs-lookup"><span data-stu-id="18a50-113">**Period allocation**</span></span>     | <span data-ttu-id="18a50-114">Tapahtumia ei voi kohdistaa eksplisiittisesti kirjanpitokauden ajalle.</span><span class="sxs-lookup"><span data-stu-id="18a50-114">You can't explicitly allocate transactions over a fiscal period.</span></span> <span data-ttu-id="18a50-115">Sen sijaan ennuste ja ennusteen valvonta perustuvat projektin elinkaareen.</span><span class="sxs-lookup"><span data-stu-id="18a50-115">Instead, the forecast, and the control of the forecast, are based on the life of the project.</span></span> <span data-ttu-id="18a50-116">Koska ennusteet perustuvat tiettyyn päivämäärään, sinun täytyy päätellä ajanjakso päivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="18a50-116">Because forecasts are based on a specific date, you must infer the period from the date.</span></span> | <span data-ttu-id="18a50-117">Voit kohdistaa tapahtumia koko projektin tai kirjanpitokauden ajalle.</span><span class="sxs-lookup"><span data-stu-id="18a50-117">You can allocate transactions over the whole project or a fiscal period.</span></span> <span data-ttu-id="18a50-118">Jos kohdistat jakson ajalle, voit siirtää käyttämättömiä summia seuraavalle kirjanpitokaudelle.</span><span class="sxs-lookup"><span data-stu-id="18a50-118">If you allocate over a period, you can carry unused amounts forward to the next fiscal period.</span></span> |
| <span data-ttu-id="18a50-119">**Tapahtumien tarkasteleminen**</span><span class="sxs-lookup"><span data-stu-id="18a50-119">**Viewing transactions**</span></span>  | <span data-ttu-id="18a50-120">Voit tarkastella tapahtumia ennustelomakkeissa, joissa näet koko yrityksen ja kaikkien projektien ennusteet hierarkiasta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="18a50-120">You can view transactions in the forecast forms, where you see the forecasts for the whole company and for all projects, regardless of the hierarchy.</span></span> <span data-ttu-id="18a50-121">Jos haluat keskittyä tiettyyn projektiin, sinun on suodatettava tiedot.</span><span class="sxs-lookup"><span data-stu-id="18a50-121">To focus on a particular project, you must filter the data.</span></span>                                       | <span data-ttu-id="18a50-122">Voit tarkastella yhden projektihierarkian budjetoituja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="18a50-122">You can view budgeted transactions for a single project hierarchy.</span></span> <span data-ttu-id="18a50-123">Siten voit tarkastella pääprojektin tai sen aliprojektien tapahtumatietoja.</span><span class="sxs-lookup"><span data-stu-id="18a50-123">Therefore, you can view transaction details for a parent project or its subprojects.</span></span>                 |
| <span data-ttu-id="18a50-124">**Tapahtumamuuttujat**</span><span class="sxs-lookup"><span data-stu-id="18a50-124">**Transaction variables**</span></span> | <span data-ttu-id="18a50-125">Kun lisäät ennustetapahtumia, voit käyttää kaikkia toteutuneeseen tapahtumaan liittyviä määritteitä.</span><span class="sxs-lookup"><span data-stu-id="18a50-125">When you enter forecast transactions, you can use every attribute that exists for an actual transaction.</span></span> <span data-ttu-id="18a50-126">Tämä lisää ennusteen mahdollista yksityiskohtaisuutta.</span><span class="sxs-lookup"><span data-stu-id="18a50-126">This allows for greater detail in the forecast.</span></span> <span data-ttu-id="18a50-127">Voit esimerkiksi syöttää tietoja määristä, työntekijöistä, nimikkeistä tai riviominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="18a50-127">For example, you can enter details for quantities, workers, items, or line properties.</span></span>         | <span data-ttu-id="18a50-128">Kun syötät budjettitietoja, voit käyttää vain summia, luokkia ja aktiviteetteja.</span><span class="sxs-lookup"><span data-stu-id="18a50-128">When you enter budget details, you can use only amounts, categories, and activities.</span></span>                    |
| <span data-ttu-id="18a50-129">**Suojaus**</span><span class="sxs-lookup"><span data-stu-id="18a50-129">**Security**</span></span>              | <span data-ttu-id="18a50-130">Ennusteet perustuvat tapahtumiin, jotka lisätään ennustelomakkeisiin, eikä niihin liity prosessinvalvonnan mekanismia.</span><span class="sxs-lookup"><span data-stu-id="18a50-130">Forecasting is based on transactions that you enter in the forecast forms and involves no process control mechanism.</span></span> <span data-ttu-id="18a50-131">Kaikki työntekijät, joilla on käyttöoikeudet ennustelomakkeeseen, voivat tarkistaa tietoja ilman hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="18a50-131">Any worker who has permissions for a forecast form can revise information without approval.</span></span>                                        | <span data-ttu-id="18a50-132">Budjetointi käyttää työnkulkujärjestelmää, mikä mahdollistaa muutoksenhallinnan sekä tarkistushistorian ylläpitämisen.</span><span class="sxs-lookup"><span data-stu-id="18a50-132">Budgeting uses the workflow system, which enables change management and lets you keep a history of the revisions.</span></span>         |
| <span data-ttu-id="18a50-133">**Kirjaustyypit**</span><span class="sxs-lookup"><span data-stu-id="18a50-133">**Entry types**</span></span>           | <span data-ttu-id="18a50-134">Ennustetapahtumien kirjaukset perustuvat yksikköjen määrään sekä kustannuksiin ja myyntiyksikköhintoihin.</span><span class="sxs-lookup"><span data-stu-id="18a50-134">Forecast transaction entries are based on the number of units, and on cost and sales unit prices.</span></span>  | <span data-ttu-id="18a50-135">Budjetintiedot perustuvat summiin, jotka jaetaan kustannusten ja tuottojen kesken.</span><span class="sxs-lookup"><span data-stu-id="18a50-135">Budget details are based on amounts, which are split between costs and revenues.</span></span>                                          |
| <span data-ttu-id="18a50-136">**Ennustemallit**</span><span class="sxs-lookup"><span data-stu-id="18a50-136">**Forecast models**</span></span>       | <span data-ttu-id="18a50-137">Koska jokainen ennuste on liitettävä malliin, voit luoda useita ennustemalleja ja määrittää myös alimalleja.</span><span class="sxs-lookup"><span data-stu-id="18a50-137">Because each forecast must be associated with a model, you can create multiple forecast models and also set up submodels.</span></span>           | <span data-ttu-id="18a50-138">Projektin budjetointi rajoittaa budjetoinnissa käytettäviä ennustemalleja.</span><span class="sxs-lookup"><span data-stu-id="18a50-138">Project budgeting limits the forecast models that are used for budgeting.</span></span> <span data-ttu-id="18a50-139">Pienempi määrä ennustemalleja voi parantaa ennusteiden yhdenmukaisuutta.</span><span class="sxs-lookup"><span data-stu-id="18a50-139">Fewer forecast models can help increase consistency in projections.</span></span>                           |
| <span data-ttu-id="18a50-140">**Kustannusten ylittyminen**</span><span class="sxs-lookup"><span data-stu-id="18a50-140">**Cost overruns**</span></span>         | <span data-ttu-id="18a50-141">Voit vain sallia tai estää sellaisten tapahtumien kirjauksen, joka aiheuttaisi kustannusten ylittymisen.</span><span class="sxs-lookup"><span data-stu-id="18a50-141">You can only allow or disallow the entry of transactions that will cause a cost overrun.</span></span>   | <span data-ttu-id="18a50-142">Projektin budjetointi tarjoaa käyttäjille lisää ohjausmahdollisuuksia.</span><span class="sxs-lookup"><span data-stu-id="18a50-142">Project budgeting provides additional control options for users.</span></span> <span data-ttu-id="18a50-143">Voit sallia varoitukset ja ylitykset.</span><span class="sxs-lookup"><span data-stu-id="18a50-143">You can allow warnings and overruns.</span></span>                    |
| <span data-ttu-id="18a50-144">**Ohjausobjekti**</span><span class="sxs-lookup"><span data-stu-id="18a50-144">**Control**</span></span>               | <span data-ttu-id="18a50-145">Ennustevalvontaa suoritetaan käyttämällä ennusteiden vähentämistä.</span><span class="sxs-lookup"><span data-stu-id="18a50-145">Forecast control is performed by using forecast reduction.</span></span> <span data-ttu-id="18a50-146">Todelliset summat vähennetään ennustetapahtumien saldoista ilman kirjausketjua.</span><span class="sxs-lookup"><span data-stu-id="18a50-146">Actual amounts are subtracted from forecast transaction balances without any audit trail.</span></span> <span data-ttu-id="18a50-147">Tämä voi vaikeuttaa sen jäljittämistä, missä todelliset tapahtumat ovat tapahtuneet.</span><span class="sxs-lookup"><span data-stu-id="18a50-147">This can make it more difficult to trace where the actual transactions occurred.</span></span>                   | <span data-ttu-id="18a50-148">Projektin budjetinvalvonnassa todelliset summat vähennetään jäljellä olevan budjetin summista.</span><span class="sxs-lookup"><span data-stu-id="18a50-148">In project budget control, actual amounts are subtracted from amounts in the remaining budget.</span></span> <span data-ttu-id="18a50-149">Tämä mahdollistaa selkeämmän kirjausketjun.</span><span class="sxs-lookup"><span data-stu-id="18a50-149">This allows for a clearer audit trail.</span></span>                                   |

## <a name="project-forecasts"></a><span data-ttu-id="18a50-150">Projektiennusteet</span><span class="sxs-lookup"><span data-stu-id="18a50-150">Project forecasts</span></span>
<span data-ttu-id="18a50-151">Kun käytät projektiennusteita, voit lisätä kullekin tapahtumatyypille ennustetapahtumia ennustelomakkeisiin.</span><span class="sxs-lookup"><span data-stu-id="18a50-151">When you use project forecasting, you can enter forecast transactions in forecast forms for each transaction type.</span></span> <span data-ttu-id="18a50-152">Jokaista todellista tapahtumaa varten käytettävissä olevaa määritettä voidaan käyttää ennustetapahtumassa. Esimerkkejä näistä määritteistä ovat rivin kannattavuus, rivimääritteet, työntekijät ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="18a50-152">Every attribute that is available for an actual transaction can be used for a forecast transaction—for example, line profitability, line attributes, workers, or descriptions.</span></span> <span data-ttu-id="18a50-153">Voit myös ennustaa, kuinka kauan kulun ilmaantumisesta kestää asiakkaan laskuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="18a50-153">You can also project how long after you incur a cost you will invoice a customer.</span></span> 

<span data-ttu-id="18a50-154">Projektiennusteen tapahtumat perustuvat yksikköihin ja määriin.</span><span class="sxs-lookup"><span data-stu-id="18a50-154">Project forecasting transactions are based on units and amounts.</span></span> 

<span data-ttu-id="18a50-155">Sinun on yhdistettävä jokainen projektiennuste ennustemalliin.</span><span class="sxs-lookup"><span data-stu-id="18a50-155">You must associate each project forecast with a forecast model.</span></span> <span data-ttu-id="18a50-156">Kun lisäät ennustetapahtuman, järjestelmä ehdottaa automaattisesti ennustemallia.</span><span class="sxs-lookup"><span data-stu-id="18a50-156">When you enter a forecast transaction, a forecast model is automatically suggested.</span></span> <span data-ttu-id="18a50-157">Ennustemalli toimii ennustetapahtumien säilönä.</span><span class="sxs-lookup"><span data-stu-id="18a50-157">The forecast model acts as a container for the forecast transactions.</span></span> 

<span data-ttu-id="18a50-158">Voit määrittää ennustemalleja mallien alimalleiksi.</span><span class="sxs-lookup"><span data-stu-id="18a50-158">You can designate forecast models as submodels for a model.</span></span> <span data-ttu-id="18a50-159">Tämän avulla voit ennustaa alueen, ajanjakson tai osaston mukaan.</span><span class="sxs-lookup"><span data-stu-id="18a50-159">This lets you forecast by region, time period, or department.</span></span> <span data-ttu-id="18a50-160">Voit kopioida ennustetapahtumat malliin, jos haluat luoda uuden mallin, ja voit myös siirtää tapahtumat pääkirjaan.</span><span class="sxs-lookup"><span data-stu-id="18a50-160">You can copy the forecast transactions in a model to create a new model, and you can also transfer the transactions to the general ledger.</span></span> <span data-ttu-id="18a50-161">Koska ennusteen ja mallin välillä on yksi-yhteen-suhde, kukin ennustemalli muodostaa projektille erillisen budjetin.</span><span class="sxs-lookup"><span data-stu-id="18a50-161">Because there is a one-to-one relationship between a forecast and a model, each forecast model makes up a separate budget for a project.</span></span> 

<span data-ttu-id="18a50-162">Ennustemalleissa voi käyttää ennusteen vähentämistä projektien ohjausmekanismina.</span><span class="sxs-lookup"><span data-stu-id="18a50-162">Forecast models can use forecast reduction as the control mechanism for projects.</span></span> <span data-ttu-id="18a50-163">Ennusteen vähentämisessä toteutuneet tapahtumat vähentävät ennusteen tapahtumasaldoja.</span><span class="sxs-lookup"><span data-stu-id="18a50-163">In forecast reduction, actual transactions reduce forecast transaction balances.</span></span> <span data-ttu-id="18a50-164">Koska ennusteen vähennystä kuitenkin käytetään hierarkian korkeimmassa projektissa, se tarjoaa rajallisen näkymän ennusteen muutoksista.</span><span class="sxs-lookup"><span data-stu-id="18a50-164">However, because forecast reduction is applied to the highest project in the hierarchy, it provides a limited view of changes in the forecast.</span></span> <span data-ttu-id="18a50-165">Jos työntekijä on esimerkiksi liitetty aliprojektiin, työntekijän toteutuneet tapahtumat kirjataan pääprojektiin.</span><span class="sxs-lookup"><span data-stu-id="18a50-165">For example, if a worker is associated with a subproject, the actual transactions for the worker are posted to the parent project.</span></span> <span data-ttu-id="18a50-166">Tämä voi vaikeuttaa muutosten seuraamista, koska et voi helposti selvittää, mikä tapahtuma missä aliprojektissa aiheutti ennustesumman vähennyksen.</span><span class="sxs-lookup"><span data-stu-id="18a50-166">This can make it difficult to track changes, because you can't easily determine which transaction in which subproject caused a reduction to the forecast amount.</span></span> <span data-ttu-id="18a50-167">Siksi on hyvä luoda ennustemallin kopio käytettäväksi ennusteen vähentämisessä.</span><span class="sxs-lookup"><span data-stu-id="18a50-167">Therefore, it's a good idea to create a copy of a forecast model for forecast reduction to use.</span></span> <span data-ttu-id="18a50-168">Raporttien avulla voit tarkastella alun perin ennustettuja tietoja.</span><span class="sxs-lookup"><span data-stu-id="18a50-168">You can then use reports to view what was originally forecasted.</span></span> 

<span data-ttu-id="18a50-169">Voit tarkistaa, kopioida, poistaa tai siirtää projektiennusteita pääkirjan budjettiin.</span><span class="sxs-lookup"><span data-stu-id="18a50-169">You can revise, copy, delete, or transfer project forecasts to a general ledger budget.</span></span> <span data-ttu-id="18a50-170">Prosessinvalvontaa ei kuitenkaan ole.</span><span class="sxs-lookup"><span data-stu-id="18a50-170">However, there is no process control.</span></span> <span data-ttu-id="18a50-171">Kaikki työntekijät, joilla on käyttöoikeus ennustelomakkeeseen, tehdä tarkistuksia ilman arviointia.</span><span class="sxs-lookup"><span data-stu-id="18a50-171">Any worker who has permission for a forecast form can make revisions without review.</span></span>

-   <span data-ttu-id="18a50-172">**Tarkista** – Voit tarkistaa ennustetapahtuma samoissa lomakkeissa, joihin alkuperäiset kirjaukset tehtiin.</span><span class="sxs-lookup"><span data-stu-id="18a50-172">**Revise** – You can revise a forecast transaction in the same forms where the original entries were made.</span></span>
-   <span data-ttu-id="18a50-173">**Kopioi tai poista** – Kun kopioit ennustetapahtumia, kopioit yhden ennustemallin rivit toiseen ennustemalliin.</span><span class="sxs-lookup"><span data-stu-id="18a50-173">**Copy or delete** – When you copy forecast transactions, you copy the transaction lines of one forecast model to another forecast model.</span></span> <span data-ttu-id="18a50-174">Kun poistat ennusteen, poistat ennustetapahtumat ennustemallista.</span><span class="sxs-lookup"><span data-stu-id="18a50-174">When you delete a forecast, you delete the forecast transactions from a forecast model.</span></span> <span data-ttu-id="18a50-175">Jos haluat rajoittaa kopioitavia tai poistettavia ennustetapahtumia, valitse tietyt tapahtumatyypit ja -päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="18a50-175">To limit the forecast transactions that are copied or deleted, select specific transaction types and dates.</span></span> <span data-ttu-id="18a50-176">Siten voit kopioida tai poistaa vain tiettyjä ennusteen osia.</span><span class="sxs-lookup"><span data-stu-id="18a50-176">This lets you copy or delete only specific parts of a forecast.</span></span>
-   <span data-ttu-id="18a50-177">**Siirto** – Kun siirrät projektiennusteen pääkirjan budjettiin, siirrät ennustemallin ennustetapahtumat pääkirjan budjettiin.</span><span class="sxs-lookup"><span data-stu-id="18a50-177">**Transfer** – When you transfer a project forecast to a general ledger budget, you transfer the forecast transactions of a forecast model to a general ledger budget.</span></span> <span data-ttu-id="18a50-178">Voit korvata kaikki siihen pääkirjaan aiemmin siirretyt tapahtumat, johon siirrät projektiennusteesi.</span><span class="sxs-lookup"><span data-stu-id="18a50-178">You can overwrite any previously transferred transactions in the general ledger budget that you transfer your project forecast to.</span></span>

## <a name="project-budgets"></a><span data-ttu-id="18a50-179">Projektibudjetit</span><span class="sxs-lookup"><span data-stu-id="18a50-179">Project budgets</span></span>
<span data-ttu-id="18a50-180">Projektien budjetointi on ennustamista yksinkertaisempaa, vaikka se integroituukin ennustemalleihin.</span><span class="sxs-lookup"><span data-stu-id="18a50-180">Project budgeting is a simpler method than forecasting, although it does integrate with forecast models.</span></span> <span data-ttu-id="18a50-181">Siinä käytetään yksittäistä kirjauslomaketta alkuperäisiä budjettitietoja ja -tarkistuksia varten ja mahdollistaa ennusteet, jotka perustuvat ainoastaan määrään, luokkaan tai aktiviteettiin.</span><span class="sxs-lookup"><span data-stu-id="18a50-181">It uses a single entry form for original budget details and revisions, and allows for projections that are based only on amount, category, or activity.</span></span> 

<span data-ttu-id="18a50-182">Projektin budjetoinnissa kaikki alkuperäiset budjetit ja tarkistukset on lähetettävä hyväksyttäväksi projektityönkulkuun.</span><span class="sxs-lookup"><span data-stu-id="18a50-182">In project budgeting, all original budgets and revisions must be sent to a project workflow for approval.</span></span> <span data-ttu-id="18a50-183">Työnkulkujen avulla voit hallita prosessia entistä laajemmin ja luoda muutoksia historiatietueeseen.</span><span class="sxs-lookup"><span data-stu-id="18a50-183">Workflows give you increased control over the process and create a change history record.</span></span> 

<span data-ttu-id="18a50-184">Projektin budjetointi muistuttaa pääkirjan budjetointia, mutta sen määrittäminen on nopeampaa ja helpompaa.</span><span class="sxs-lookup"><span data-stu-id="18a50-184">Project budgeting resembles general ledger budgeting, but is faster and easier to set up.</span></span> <span data-ttu-id="18a50-185">Monia pääkirjan budjetoinnin asetuksia, kuten numerosarjoja tai valuuttaa, ei tarvitse määrittää erikseen projekteille.</span><span class="sxs-lookup"><span data-stu-id="18a50-185">Many of the options in general ledger budgeting, such as number sequences or currency, do not have to be set up separately for projects.</span></span>

<span data-ttu-id="18a50-186">Projektibudjetit liitetään automaattisesti kahteen ennustemalliin, joista toinen on alkuperäiselle budjetille ja toinen jäljellä olevalle budjetille.</span><span class="sxs-lookup"><span data-stu-id="18a50-186">Project budgets are automatically associated with two forecast models, one for original budget and one for remaining budget.</span></span> <span data-ttu-id="18a50-187">Siten ennustemalleihin perustuvissa raporteissa voi käyttää budjettitietoja.</span><span class="sxs-lookup"><span data-stu-id="18a50-187">Therefore, reports that are based on forecast models can use budget data.</span></span> <span data-ttu-id="18a50-188">Kun projektibudjetti on vahvistettu, järjestelmä luo ennustesiirtoja niiden määritettyjen mallien perusteella, joita käytetään raportointi- ja hallintatarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="18a50-188">When a project budget is committed, the system creates forecast transactions based on the associated models, which are used for reporting and control purposes.</span></span>

## <a name="forecast-models"></a><span data-ttu-id="18a50-189">Ennustemallit</span><span class="sxs-lookup"><span data-stu-id="18a50-189">Forecast models</span></span>
<span data-ttu-id="18a50-190">Ennustemalleilla on yksikerroksinen hierarkia.</span><span class="sxs-lookup"><span data-stu-id="18a50-190">Forecast models have a single-layer hierarchy.</span></span> <span data-ttu-id="18a50-191">Tämä tarkoittaa sitä, että yksi projektiennuste on liitettävä yhteen ennustemalliin.</span><span class="sxs-lookup"><span data-stu-id="18a50-191">This means that one project forecast must be associated with one forecast model.</span></span>

<span data-ttu-id="18a50-192">Jos käytät projektiennustusta, voit määrittää malleja alimalleiksi.</span><span class="sxs-lookup"><span data-stu-id="18a50-192">If you use project forecasting, you can identify models as submodels.</span></span> <span data-ttu-id="18a50-193">Sitten voit luoda malleja osastoittain, aikajaksoittain tai alueittain.</span><span class="sxs-lookup"><span data-stu-id="18a50-193">You can then create forecasts by department, time period, or region.</span></span> <span data-ttu-id="18a50-194">Voit esimerkiksi luoda ennustemallin vuodeksi ja luoda sitten alimallit koillisen, kaakon, lounaan ja luoteen alue-ennusteille, jotka aluepäälliköt lähettävät.</span><span class="sxs-lookup"><span data-stu-id="18a50-194">For example, you can create a forecast model for a year, and then create submodels for the Northeast, Southeast, Northwest, and Southwest regional forecasts that regional heads submit.</span></span> <span data-ttu-id="18a50-195">Valitsemalla eri vaihto ehtoja käytettävissä olevissa raporteissa voit tarkastella tietoja kokonaisennusteen tai alimallin mukaan.</span><span class="sxs-lookup"><span data-stu-id="18a50-195">By selecting different options in the available reports, you can view information by total forecast or by submodel.</span></span>


