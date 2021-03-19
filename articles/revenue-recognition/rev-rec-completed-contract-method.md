---
title: Myyntituottoarvioiden hallinta
description: Tässä aiheessa on tietoja myyntituottoarvioiden määrittämisestä projekteille.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278999"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="a429f-103">Myyntituottoarvioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="a429f-103">Manage revenue estimates</span></span>

<span data-ttu-id="a429f-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="a429f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a429f-105">Voit luoda, laskea, kirjata, peruuttaa tai eliminoida tuottoarvioita.</span><span class="sxs-lookup"><span data-stu-id="a429f-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="a429f-106">Voit tehdä tämän joko manuaalisesti tai kausittaisen prosessin avulla.</span><span class="sxs-lookup"><span data-stu-id="a429f-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="a429f-107">Tässä aiheessa on tietoja myyntituottoarvioiden määrittämisestä projekteille.</span><span class="sxs-lookup"><span data-stu-id="a429f-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="a429f-108">Myyntituottoarvioiden manuaalinen hallinta</span><span class="sxs-lookup"><span data-stu-id="a429f-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="a429f-109">Valitse kiinteähintaisen tuoton arviointiprojektissa tai **Arviokysely** -sivulla (**Projektinhallinta ja kirjanpito** > **Raportit ja kyselyt** > **Arviokyselyt ja raportit**) **Arviot**.</span><span class="sxs-lookup"><span data-stu-id="a429f-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="a429f-110">Tuottoarvioiden hallinta kausittaisen prosessin avulla</span><span class="sxs-lookup"><span data-stu-id="a429f-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="a429f-111">Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Arviot** ja valitse vastaava prosessi.</span><span class="sxs-lookup"><span data-stu-id="a429f-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="a429f-112">Tuottoarvion luominen</span><span class="sxs-lookup"><span data-stu-id="a429f-112">Create a revenue estimate</span></span>

<span data-ttu-id="a429f-113">Suorita seuraavat vaiheet tuottoarvion luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="a429f-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="a429f-114">Siirry kohtaan **Projektinhallintaan ja kirjanpito** > **Kausittainen** > **Arviot**.</span><span class="sxs-lookup"><span data-stu-id="a429f-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="a429f-115">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a429f-115">Select **New**.</span></span> <span data-ttu-id="a429f-116">Valitse seuraavat parametrit sivulla **Arvioiden luonti**:</span><span class="sxs-lookup"><span data-stu-id="a429f-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="a429f-117">**Kausikoodi** : Tämä koodi määrittää, kuinka usein arvioita kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a429f-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="a429f-118">**Arvion päivämäärä**: Päivämäärä, jolloin arvio käsitellään.</span><span class="sxs-lookup"><span data-stu-id="a429f-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="a429f-119">**Jatkuva**: Valitse tämä valintaruutu, jos haluat luoda arvioita vain, jos edellisellä kaudella on kirjattu arvioita tai jos arvio on ensimmäinen luotu arvio.</span><span class="sxs-lookup"><span data-stu-id="a429f-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="a429f-120">Jos tätä ei ole valittu, arviot luodaan, vaikka arvioita ei olisi kirjattu edelliselle kaudelle.</span><span class="sxs-lookup"><span data-stu-id="a429f-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="a429f-121">**Valmistumiskustannukset** -menetelmä: Määritä, miten jäljellä oleva projektityö arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="a429f-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="a429f-122">Lisätietoja on kohdassa [Valmistumiskustannusten menetelmät](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a429f-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="a429f-123">**Valmistumismenetelmä**: Valitse valmistumismenetelmä seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="a429f-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="a429f-124">**Automaattinen**: Valmistumisprosentti lasketaan automaattisesti ja laskentaan sisältyvien kustannusrivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="a429f-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="a429f-125">Kustannusmalli määrittää sisällytetyt kustannusrivit.</span><span class="sxs-lookup"><span data-stu-id="a429f-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="a429f-126">**Manuaalinen**: Valmistumisprosentti on yhtä suuri kuin viimeisen arvion valmistumisprosentti.</span><span class="sxs-lookup"><span data-stu-id="a429f-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="a429f-127">Kun arvio on luotu, voit muuttaa arvoa **Manuaalinen laskenta** **Arviot**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a429f-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="a429f-128">**Kustannusmallista**: Automaattisen ja manuaalisen menetelmän yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="a429f-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="a429f-129">Tämä asetus määritetään automaattisesti tai manuaalisesti kustannusmallin oletusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="a429f-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="a429f-130">**Ennustemalli**: Valitse arviolle ennustemalli.</span><span class="sxs-lookup"><span data-stu-id="a429f-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="a429f-131">**Tulosta arvioluettelo**: Luo ja näytä arvioluettelo.</span><span class="sxs-lookup"><span data-stu-id="a429f-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="a429f-132">Luettelo sisältää nykyisen funktion tilan.</span><span class="sxs-lookup"><span data-stu-id="a429f-132">The list contains the status of the current function.</span></span> <span data-ttu-id="a429f-133">Voit tulostaa arviosta annetut varoitukset raporttiin.</span><span class="sxs-lookup"><span data-stu-id="a429f-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="a429f-134">Seuraavat ehdot aiheuttavat varoitusten näkymisen arviointiluettelossa:</span><span class="sxs-lookup"><span data-stu-id="a429f-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="a429f-135">Valmistumisprosentti on yli 100.</span><span class="sxs-lookup"><span data-stu-id="a429f-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="a429f-136">Valmistumisprosentti on alle nolla.</span><span class="sxs-lookup"><span data-stu-id="a429f-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="a429f-137">Negatiivinen määrä **Valmistuu myöhemmin**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="a429f-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="a429f-138">Arvio, jolla ei ole vastaavaa sopimussummaa.</span><span class="sxs-lookup"><span data-stu-id="a429f-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="a429f-139">Arvio, jolla ei ole liitettyä kustannusarviota.</span><span class="sxs-lookup"><span data-stu-id="a429f-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="a429f-140">**Näytä infoloki**: Valitse tämä vaihtoehto, jos haluat saada sanoman, joka sisältää tietoja arviointiprojekteista, jotka on käsitelty työn suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a429f-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="a429f-141">Kirjaa Käynnissä oleva tai kertymät</span><span class="sxs-lookup"><span data-stu-id="a429f-141">Post WIP or accruals</span></span>

<span data-ttu-id="a429f-142">Kun arviot on arvioitu, ne säilyvät, pienenevät tai kasvavat.</span><span class="sxs-lookup"><span data-stu-id="a429f-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="a429f-143">Voit sitten kirjata käynnissä olevan työn, kun käytössä on **Valmistunut sopimus** -arviointiperiaate, tai kirjata kertymän, kun käynnissä on **Valmistumisprosentti**-arviointiperiaate.</span><span class="sxs-lookup"><span data-stu-id="a429f-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="a429f-144">Arviointikauden tila muuttuu **Luodusta** **Kirjatuksi**.</span><span class="sxs-lookup"><span data-stu-id="a429f-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="a429f-145">Peruuta käynnissä oleva työ tai kertymä</span><span class="sxs-lookup"><span data-stu-id="a429f-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="a429f-146">Käytä peruutustoimintoa palauttamaan jo kirjattu käynnissä oleva työ tai kertymä ja luo sen jälkeen arviot kaudelle.</span><span class="sxs-lookup"><span data-stu-id="a429f-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="a429f-147">Jos haluat peruuttaa kauden, joka on muiden kausien välissä, peruuta tarvittavat arviointikaudet ja kirjaa ne sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="a429f-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="a429f-148">Koska kaikki seuraavat kaudet määräytyvät edellisen kauden arvioiden mukaan, älä ohita kausia.</span><span class="sxs-lookup"><span data-stu-id="a429f-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="a429f-149">Arviointiprojektin poistaminen ja projektin lopettaminen</span><span class="sxs-lookup"><span data-stu-id="a429f-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="a429f-150">Arviointiprosessin viimeisessä vaiheessa poistetaan arviointiprojekti ja lopetetaan kiinteähintainen projekti, kun valmistumisprosentti on 100 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="a429f-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="a429f-151">Seuraava tapahtuu, kun suoritat poiston:</span><span class="sxs-lookup"><span data-stu-id="a429f-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="a429f-152">Jos kyseessä on kiinteähintainen projekti, jonka sopimus on täytetty, käynnissä olevan työn arvot tyhjenevät saldotileiltä ja kirjautuvat tuotto- ja tappiotileille.</span><span class="sxs-lookup"><span data-stu-id="a429f-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="a429f-153">Jos kyseessä on kiinteähintainen projekti, jolla on valmistumisprosentti, kertymät poistetaan tuotto- ja tappiotileiltä.</span><span class="sxs-lookup"><span data-stu-id="a429f-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="a429f-154">Arvion tilaksi vaihtuu **Eliminoitu**.</span><span class="sxs-lookup"><span data-stu-id="a429f-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="a429f-155">Erityistapauksissa prosenttiosuus voi ulottua yli 100 prosenttiin.</span><span class="sxs-lookup"><span data-stu-id="a429f-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="a429f-156">Kun näin tapahtuu, vähennä valmistumis prosenttia käyttämällä **Määritä valmistumiskustannuksiksi nolla -menetelmää**, jotta saavutetaan 100 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="a429f-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="a429f-157">Poiston peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="a429f-157">Reverse elimination</span></span>

1. <span data-ttu-id="a429f-158">Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Arviot** > **Peruuta poisto**.</span><span class="sxs-lookup"><span data-stu-id="a429f-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="a429f-159">Valitse toimintoruudun **Prosessi**-välilehden **Ylläpito**-ryhmässä **Arvio**.</span><span class="sxs-lookup"><span data-stu-id="a429f-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="a429f-160">Valitse **Peruuta poisto**.</span><span class="sxs-lookup"><span data-stu-id="a429f-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="a429f-161">Tämän sivun avulla voit peruuttaa kaikki poistot, joilla on tietty arviopäivä ja joiden arvio tila on **Eliminoitu**.</span><span class="sxs-lookup"><span data-stu-id="a429f-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="a429f-162">Tapahtuman tila muuttuu sen jälkeen, kun olet valinnut tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="a429f-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="a429f-163">Tämä myös muuttaa automaattisesti projektin tilaksi **Työn alla**, jos projektin vaiheeksi on määritetty valmis.</span><span class="sxs-lookup"><span data-stu-id="a429f-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="a429f-164">Projektikauden arvion tila vaihtuu takaisin arvoksi **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="a429f-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]