---
title: Käyttöliittymässä siirtyminen
description: Tässä aiheessa on tietoja projektinhallinnasta Dynamics 365:n projektitoiminnoissa.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286739"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="43d97-103">Käyttöliittymässä siirtyminen</span><span class="sxs-lookup"><span data-stu-id="43d97-103">Navigating the user interface</span></span>

<span data-ttu-id="43d97-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="43d97-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="43d97-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="43d97-105">Overview</span></span>

<span data-ttu-id="43d97-106">Pääprojektilomake on erotettu useiksi välilehdiksi.</span><span class="sxs-lookup"><span data-stu-id="43d97-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="43d97-107">Kukin välilehti edustaa projektin eritasoisia yksityiskohtia.</span><span class="sxs-lookup"><span data-stu-id="43d97-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="43d97-108">**Yhteenveto**: Näyttää projektin kuvauksen ja kokoaa sekä suunnitellun että toteutuneen projektin tehokkuuden.</span><span class="sxs-lookup"><span data-stu-id="43d97-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Yhteenveto-välilehti ja -kentät](media/navigation7.png)

- <span data-ttu-id="43d97-110">**Tehtävät**: Sisältää ruudukkonäkymän, kaavionäkymän ja Gantt-kaavion työrakennetta koskevista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="43d97-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Tehtävä-välilehti ja -kentät](media/navigation8.png)

- <span data-ttu-id="43d97-112">**Ryhmä**: Sisältää projektin osallistujia koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="43d97-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="43d97-113">Kunkin ryhmän jäsenen delegoitu työmäärä on myös koottu tähän näkymään.</span><span class="sxs-lookup"><span data-stu-id="43d97-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Ryhmä-välilehti ja -kentät](media/navigation9.png)

- <span data-ttu-id="43d97-115">**Resurssien delegoinnit**: Sisältää aikajaksopohjaisen näkymän projektin kunkin resurssin työmäärästä.</span><span class="sxs-lookup"><span data-stu-id="43d97-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Resurssien delgoinnit -välilehti ja -kentät](media/navigation10.png)

- <span data-ttu-id="43d97-117">**Resurssien täsmäytys**: Sisältää aikajaksopohjaisen näkymän kunkin nimetyn resurssin delegointien ja varausten eroista.</span><span class="sxs-lookup"><span data-stu-id="43d97-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Resurssien täsmäytys -välilehti ja -kentät](media/navigation11.png)

- <span data-ttu-id="43d97-119">**Arviot**: Sisältää aikajaksopohjaisen näkymän projektin kustannus- ja myyntiarvioista.</span><span class="sxs-lookup"><span data-stu-id="43d97-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Arviot-välilehti ja -kentät](media/navigation12.png)

- <span data-ttu-id="43d97-121">**Seuranta**: Sisältää näkymän, joka näyttää töiden, kustannusten ja myynnin työnrakenteen tehtävien etenemisen.</span><span class="sxs-lookup"><span data-stu-id="43d97-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Seuranta-välilehti ja -kentät](media/navigation13.png)

- <span data-ttu-id="43d97-123">**Myynti**: Sisältää syvälinkit projektiin liittyviin tarjouksiin ja sopimuksiin.</span><span class="sxs-lookup"><span data-stu-id="43d97-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="43d97-124">**Kuluarviot**: Sisältää ruudukon, joka määrittää projektin kulut organisaation kululuokkien perusteella.</span><span class="sxs-lookup"><span data-stu-id="43d97-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Kuluarviot-välilehti ja -kentät](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="43d97-126">Ruudukko-ohjausobjektit</span><span class="sxs-lookup"><span data-stu-id="43d97-126">Grid controls</span></span>

<span data-ttu-id="43d97-127">Seuraavassa on lyhyt yleiskatsaus erilaisista projektisuunnittelun välilehdistä löytyvistä tyypillisistä ohjausobjekteista.</span><span class="sxs-lookup"><span data-stu-id="43d97-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="43d97-128">Lataa uudelleen</span><span class="sxs-lookup"><span data-stu-id="43d97-128">Refresh</span></span>

<span data-ttu-id="43d97-129">**Päivitä**: Noutaa uusimmat tiedot palvelimesta, jos ruudukon lataamisen jälkeen tapahtui muutoksia.</span><span class="sxs-lookup"><span data-stu-id="43d97-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Päivitä-painike](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="43d97-131">Ryhmittele</span><span class="sxs-lookup"><span data-stu-id="43d97-131">Group by</span></span>

<span data-ttu-id="43d97-132">**Ryhmittele**: Päivittää ruudukon rivien ryhmittelyn niin, että se vastaa joko resursseja, rooleja tai luokkia käyttäjän tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="43d97-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Ryhmittele-painike](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="43d97-134">Edellinen/Seuraava</span><span class="sxs-lookup"><span data-stu-id="43d97-134">Previous/Next</span></span>

<span data-ttu-id="43d97-135">**Edellinen**/**Seuraava**: Päivitä aikajaksotettujen ruudukkojen näkyvät aikajaksot.</span><span class="sxs-lookup"><span data-stu-id="43d97-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Edellinen- ja Seuraava-painikkeet](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="43d97-137">Aikajakso</span><span class="sxs-lookup"><span data-stu-id="43d97-137">Timescale</span></span>

<span data-ttu-id="43d97-138">**Aikajana**: Muuta aikajaksotettujen tietojen koosteita päivien, viikkojen, kuukausien ja vuosien välillä.</span><span class="sxs-lookup"><span data-stu-id="43d97-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Aikajana-painike](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="43d97-140">Laajenna</span><span class="sxs-lookup"><span data-stu-id="43d97-140">Expand</span></span>

<span data-ttu-id="43d97-141">**Laajenna**: Muodosta näkyvä ruudukko koko näytön kokoiseksi, jotta näet lisää rooleja.</span><span class="sxs-lookup"><span data-stu-id="43d97-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Laajenna-painike](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="43d97-143">Aikajaksoperuste</span><span class="sxs-lookup"><span data-stu-id="43d97-143">Time-phase by</span></span>

<span data-ttu-id="43d97-144">**Aikajaksoperuste** : Päivitä ruudukon rivien ryhmittely vastaamaan myynti arvioiden kustannus arvioita.</span><span class="sxs-lookup"><span data-stu-id="43d97-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="43d97-145">Tämä ohjausobjekti koskee myös arviokomentosarjaa ja seurantaruudukkoa.</span><span class="sxs-lookup"><span data-stu-id="43d97-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Aikajaksoperuste-painike](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="43d97-147">Lisää sarake</span><span class="sxs-lookup"><span data-stu-id="43d97-147">Add column</span></span>

<span data-ttu-id="43d97-148">**Lisää sarake**: Sallii käyttäjän määrittää ruudukon näkyvät sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="43d97-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="43d97-149">Vain käyttövalmiit sarakkeet voidaan lisätä **Projektisuunnittelu**-lomakkeen ruudukoihin.</span><span class="sxs-lookup"><span data-stu-id="43d97-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Lisää sarake -painike](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]