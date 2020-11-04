---
title: Projektien ja tehtävien yhdistäminen projektipohjaiselle tarjousriville
description: Tässä aiheessa on tietoja siitä, miten projektit ja tehtävät yhdistetään projektipohjaiseen tehtäväriviin.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075240"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="a7b66-103">Projektien ja tehtävien yhdistäminen projektipohjaiselle tarjousriville</span><span class="sxs-lookup"><span data-stu-id="a7b66-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="a7b66-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a7b66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a7b66-105">Projektipohjaisilla tarjousriveillä voit yhdistää tiettyihin tehtäviin projektissa, joka on jo liitetty tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="a7b66-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="a7b66-106">Kun yhdistät tehtäviä tarjousriviin, seuraavat tarjousrivillä määritetyt kohteet koskevat vain kyseisiä tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="a7b66-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="a7b66-107">Laskutustapa</span><span class="sxs-lookup"><span data-stu-id="a7b66-107">Billing method</span></span>
- <span data-ttu-id="a7b66-108">Veloitusasetukset</span><span class="sxs-lookup"><span data-stu-id="a7b66-108">Chargeability options</span></span>
- <span data-ttu-id="a7b66-109">Ei-ylitettävät rajoitukset</span><span class="sxs-lookup"><span data-stu-id="a7b66-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="a7b66-110">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="a7b66-110">Customers</span></span>

<span data-ttu-id="a7b66-111">Sinulla voi olla esimerkiksi projekti, jossa yksi vaihe on kiinteähintainen ja kaikki muut vaiheet ovat aika- ja materiaalipohjaisia.</span><span class="sxs-lookup"><span data-stu-id="a7b66-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="a7b66-112">Tässä tapauksessa voit liittää ensimmäisen vaiheen ja kaikki sen alitehtävät kyseisen vaiheen tarjousriviin kiinteähintaisella laskutusmenetelmällä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="a7b66-113">Tämän jälkeen voit liittää kaikki muut vaiheet aika- ja materiaaliperusteiseen tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="a7b66-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="a7b66-114">Tehtävien liittäminen projektipohjaisiin tarjousriveihin</span><span class="sxs-lookup"><span data-stu-id="a7b66-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="a7b66-115">Voit liittää tehtäviä tarjousriveihin seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="a7b66-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="a7b66-116">**Projekti** -sivu > **Tehtävän laskutus** -välilehti (optimaalinen)</span><span class="sxs-lookup"><span data-stu-id="a7b66-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="a7b66-117">**Tarjousrivi** -sivu > **Veloitettavat tehtävät** -välilehti</span><span class="sxs-lookup"><span data-stu-id="a7b66-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="a7b66-118">Projekti-sivulta</span><span class="sxs-lookup"><span data-stu-id="a7b66-118">From the Project page</span></span>

<span data-ttu-id="a7b66-119">**Projekti** -sivulla on optimaalinen kokemus tehtävien liittämiseksi tarjousriveihin.</span><span class="sxs-lookup"><span data-stu-id="a7b66-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="a7b66-120">Tämän sivun avulla voit valita useita tehtäviä ja liittää valittuun tarjousriviin kaikki ne sekä niiden alitehtävät.</span><span class="sxs-lookup"><span data-stu-id="a7b66-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="a7b66-121">Tarkista projektipohjaisen tarjous rivin **Yleiset** -välilehdestä, että **Projekti** -kenttä on täytetty.</span><span class="sxs-lookup"><span data-stu-id="a7b66-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="a7b66-122">Valitse **Sisällytettävät tehtävät** -kentässä **Vain valitut tehtävät**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="a7b66-123">Tallenna projektipohjainen tarjousrivi.</span><span class="sxs-lookup"><span data-stu-id="a7b66-123">Save the project-based quote line.</span></span> <span data-ttu-id="a7b66-124">Kun lomake päivittyy, näkyviin tulee **Veloitettavat tehtävät** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="a7b66-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="a7b66-125">Valitse **Yleiset** -välilehdessä projektin linkki **Projekti** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="a7b66-126">Valitse **Projekti** -sivulla **Tehtävän laskutus** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="a7b66-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="a7b66-127">Valitse toisesta ruudukosta (joka koskee tehtäväkohtaisia laskutusasetuksia) vähintään yksi tehtävä ja valitse sitten **Liitä tarjousrivit**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="a7b66-128">Valitse näkyviin tulevassa valintaikkunassa tarjousrivi, joka näyttää tarjouksen projektipohjaiset tarjousrivit.</span><span class="sxs-lookup"><span data-stu-id="a7b66-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="a7b66-129">Ilmaise **Laskutustyyppi** -kentässä, ovatko nämä tehtävät veloitettavissa vai ei-laskutettavia.</span><span class="sxs-lookup"><span data-stu-id="a7b66-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="a7b66-130">Valitse valintaruutu, jos haluat määrittää, sisällytetäänkö liitokseen valittujen tehtävien alitehtävät.</span><span class="sxs-lookup"><span data-stu-id="a7b66-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="a7b66-131">Kun valintaruutu on valittuna, valittujen tehtävien alitehtävät yhdistetään tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="a7b66-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="a7b66-132">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="a7b66-133">Tarjousrivi-sivulta</span><span class="sxs-lookup"><span data-stu-id="a7b66-133">From the Quote line page</span></span>

<span data-ttu-id="a7b66-134">Voit liittää projektitehtävät tarjousriveihin **Tarjousrivi** -sivun **Veloitettavat rivit** -välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="a7b66-135">Optimaalinen paikka liittää projektitehtävät tarjousriveihin on **Projekti** -sivun **Tehtävän laskutus** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="a7b66-136">Jos liität tehtäviä **Tarjousrivi** -sivun **Veloitettavat tehtävät** -välilehdessa, kukin projekti täytyy liittää manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a7b66-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="a7b66-137">Tarkista projektipohjaisen tarjous rivin **Yleiset** -välilehdestä, että **Projekti** -kentässä on valittu projekti.</span><span class="sxs-lookup"><span data-stu-id="a7b66-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="a7b66-138">Valitse **Sisällytettävät tehtävät** -kentässä **Vain valitut tehtävät**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="a7b66-139">Tallenna projektipohjainen tarjousrivi.</span><span class="sxs-lookup"><span data-stu-id="a7b66-139">Save the project-based quote line.</span></span> <span data-ttu-id="a7b66-140">Kun lomake päivittyy, näkyviin tulee **Veloitettavat tehtävät** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="a7b66-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="a7b66-141">Valitse **Veloitettavat tehtävät** -välilehdessä **Lisää tarjousrivin tehtävä**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="a7b66-142">Valitse **Tarjousrivin tehtävä** - sivun **Tehtävät** -kentässä tehtävä ja valitse sitten **Laskutustyyppi** -kentässä **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="a7b66-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a7b66-143">Close the page.</span></span> <span data-ttu-id="a7b66-144">Valittu tehtävä liitetään nyt tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="a7b66-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="a7b66-145">Tehtävien liitoksen poistaminen projektipohjaisista tarjousriveistä</span><span class="sxs-lookup"><span data-stu-id="a7b66-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="a7b66-146">Projekti-sivulta</span><span class="sxs-lookup"><span data-stu-id="a7b66-146">From the Project page</span></span>

<span data-ttu-id="a7b66-147">Tämä menetelmä on optimaalinen kokemus tehtävien liitoksen poistamisesta tarjousriveistä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="a7b66-148">Tämän sivun avulla voit valita useita tehtäviä sekä niiden alitehtävät ja poistaa liitoksen valitusta tarjousrivistä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="a7b66-149">Valitse projektipohjaisen tarjousrivin **Yleiset** -välilehdestä, että **Projekti** -kentässä projektin linkki.</span><span class="sxs-lookup"><span data-stu-id="a7b66-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="a7b66-150">Valitse **Projekti** -sivulla **Tehtävän laskutus** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="a7b66-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="a7b66-151">Valitse toisesta ruudukosta (joka koskee tehtäväkohtaisia laskutusasetuksia) vähintään yksi tehtävä ja valitse sitten **Poista tarjousrivien liitos**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="a7b66-152">Valitse näkyviin tulevassa valintaikkunassa tarjousrivi.</span><span class="sxs-lookup"><span data-stu-id="a7b66-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="a7b66-153">Valitse valintaruutu, jos haluat määrittää, poistetaanko liitos myös valittujen tehtävien alitehtävistä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="a7b66-154">Kun valintaruutu on valittuna, valittujen tehtävien alitehtävien liitos poistetaan tarjousrivistä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="a7b66-155">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-155">Select **OK**.</span></span> <span data-ttu-id="a7b66-156">Varoitussanoma ilmoittaa, että jos poistat tämän liitoksen, tehtävään aiemmin tallennetut toteutuneet arvot voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="a7b66-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="a7b66-157">Valitse **OK** , jos haluat jatkaa ja poistaa tehtävän ja projektipohjaisen tarjousrivin välisen liitoksen.</span><span class="sxs-lookup"><span data-stu-id="a7b66-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="a7b66-158">Tarjousrivi-sivulta</span><span class="sxs-lookup"><span data-stu-id="a7b66-158">From the Quote line page</span></span>

<span data-ttu-id="a7b66-159">Voit myös poistaa projektitehtävien liitoksen tarjousriveistä **Tarjousrivi** -sivun **Veloitettavat rivit** -välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="a7b66-160">Valitse **Veloitettavat tehtävät** -välilehdessä **Poista tarjousrivin tehtävä**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="a7b66-161">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7b66-161">Select **OK**.</span></span> <span data-ttu-id="a7b66-162">Varoitussanoma ilmoittaa, että jos poistat tämän liitoksen, tehtävään aiemmin tallennetut toteutuneet arvot voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="a7b66-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="a7b66-163">Valitse **OK** , jos haluat jatkaa ja poistaa tehtävän ja projektipohjaisen tarjousrivin välisen liitoksen.</span><span class="sxs-lookup"><span data-stu-id="a7b66-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="a7b66-164">Tämä toimintosarja ei poista tehtävää projektista.</span><span class="sxs-lookup"><span data-stu-id="a7b66-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="a7b66-165">Se poistaa vain tehtävän liitoksen projektipohjaisesta tarjousrivistä.</span><span class="sxs-lookup"><span data-stu-id="a7b66-165">It only removes the task association from the project-based quote line.</span></span>
