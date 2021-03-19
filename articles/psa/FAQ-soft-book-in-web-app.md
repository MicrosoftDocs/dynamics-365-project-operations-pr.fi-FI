---
title: Miten varaan resursseja alustavasti sovellusversiossa 2.x?
description: Tässä artikkelissa kerrotaan, miten projektiryhmän jäseniä varataan alustavasti Project Service -sovelluksessa.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286019"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="aabd6-103">Miten varaan resursseja alustavasti verkkosovelluksessa (Project Service -sovelluksen versio 2.x)?</span><span class="sxs-lookup"><span data-stu-id="aabd6-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="aabd6-104">Voit ajoittaa tai varata resurssin alustavasti projektiryhmään, jolloin resurssin projektiin delegoimista koskeva suunnitelma näkyy muille.</span><span class="sxs-lookup"><span data-stu-id="aabd6-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="aabd6-105">Alustavat varaukset eivät kuluta resurssin käytettävissä olevaa kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="aabd6-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="aabd6-106">Alustavasti varattuja ryhmän jäseniä ei voi delegoida projektitehtäville.</span><span class="sxs-lookup"><span data-stu-id="aabd6-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="aabd6-107">Vain resurssit, joiden tila on Varattu sitovasti ja vahvistustyyppi on Vahvistettu, voidaan delegoida tehtäville (jos niillä on delegoinnin työn vaatima määrä sitovan varauksen tunteja).</span><span class="sxs-lookup"><span data-stu-id="aabd6-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="aabd6-108">Alustavasti varatut projektiryhmän jäsenet näkyvät Ryhmän jäsen -ruudukossa niin, että heidän alustavasti varatut tuntinsa näkyvät Alustava varaus -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="aabd6-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="aabd6-109">Ne näkyvät myös aikataulutaulukossa.</span><span class="sxs-lookup"><span data-stu-id="aabd6-109">They also show up on the schedule board.</span></span> <span data-ttu-id="aabd6-110">Ne eivät osoita kapasiteetin kulutusta, koska alustava varaus ei kuluta resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="aabd6-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="aabd6-111">Project Service -sovelluksen versiossa 2.x ryhmän jäsenen voi varata projektiin alustavasti kolmella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="aabd6-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="aabd6-112">Voit tehdä alustavan varauksen aikataulutaulukossa Ylläpidä varauksia -toiminnon avulla tai luomalla yleisen resurssin.</span><span class="sxs-lookup"><span data-stu-id="aabd6-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="aabd6-113">Nämä tavat esitellään alla.</span><span class="sxs-lookup"><span data-stu-id="aabd6-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="aabd6-114">Alustava varaus aikataulutaulukon avulla</span><span class="sxs-lookup"><span data-stu-id="aabd6-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="aabd6-115">Voit tehdä alustavan varauksen aikataulutaulukon avulla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aabd6-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="aabd6-116">Avaa aikataulutaulukko.</span><span class="sxs-lookup"><span data-stu-id="aabd6-116">Open the schedule board.</span></span>
2. <span data-ttu-id="aabd6-117">Valitse Projekti-välilehden aikataulutaulukon Varaustarpeet-paneeli.</span><span class="sxs-lookup"><span data-stu-id="aabd6-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="aabd6-118">Etsi projekti, jonka resurssin haluat varata alustavasti.</span><span class="sxs-lookup"><span data-stu-id="aabd6-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="aabd6-119">Jos sinulla on useita projekteja, valitse Projekti-sarakkeen otsikko ja etsi projekti suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="aabd6-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="aabd6-120">Valitse projekti, vedä se resurssin aikaruudukkoon ja pudota projekti sinne.</span><span class="sxs-lookup"><span data-stu-id="aabd6-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="aabd6-121">Oikealla oleva Luo resurssin varaus -paneeli avautuu.</span><span class="sxs-lookup"><span data-stu-id="aabd6-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="aabd6-122">Muokkaa alku- ja loppupäivämäärää, valitse varauksen tilaksi ALustava ja määritä tunnit.</span><span class="sxs-lookup"><span data-stu-id="aabd6-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="aabd6-123">Valitse Varaa.</span><span class="sxs-lookup"><span data-stu-id="aabd6-123">Click Book.</span></span>
7. <span data-ttu-id="aabd6-124">Resurssi näkyy nyt projektissa ryhmän jäsenenä, jolla on alustavasti varattuja tunteja Alustava varaus -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="aabd6-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="aabd6-125">Huomaa, että et voi delegoida niitä työrakenteen tehtäville, koska resurssit on varattava sitovasti ryhmässä delegointia varten.</span><span class="sxs-lookup"><span data-stu-id="aabd6-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="aabd6-126">Alustava varaus Ylläpidä varauksia -toiminnon avulla</span><span class="sxs-lookup"><span data-stu-id="aabd6-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="aabd6-127">Voit tehdä alustavan varauksen Ylläpidä varauksia -toiminnon avulla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aabd6-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="aabd6-128">Valitse ryhmän jäsenen ruudukossa Uusi.</span><span class="sxs-lookup"><span data-stu-id="aabd6-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="aabd6-129">Valitse varattavan resurssin roolin alku ja loppu.</span><span class="sxs-lookup"><span data-stu-id="aabd6-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="aabd6-130">Valitse kohdistustavaksi jokin seuraavista (tapa ei voi olla Ei mitään):</span><span class="sxs-lookup"><span data-stu-id="aabd6-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="aabd6-131">Täysi kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="aabd6-131">Full Capacity</span></span>
- <span data-ttu-id="aabd6-132">Kapasiteettiprosentti</span><span class="sxs-lookup"><span data-stu-id="aabd6-132">Percentage Capacity</span></span>
- <span data-ttu-id="aabd6-133">Tuntien mukaan – jaa tasaisesti</span><span class="sxs-lookup"><span data-stu-id="aabd6-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="aabd6-134">Tuntien mukaan – etupainotteinen</span><span class="sxs-lookup"><span data-stu-id="aabd6-134">By Hours Front Load</span></span>
4. <span data-ttu-id="aabd6-135">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="aabd6-135">Click Save.</span></span> <span data-ttu-id="aabd6-136">Resurssi näkyy ryhmän ruudukossa. Resurssin tunnit näkyvät sitovasti varattuina.</span><span class="sxs-lookup"><span data-stu-id="aabd6-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="aabd6-137">Ylläpidä resurssin varauksia valitsemalla Ylläpidä varauksia.</span><span class="sxs-lookup"><span data-stu-id="aabd6-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="aabd6-138">Kun aikataulutaulukko avautuu, laajenna resurssia niin, että varaukset näkyvät.</span><span class="sxs-lookup"><span data-stu-id="aabd6-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="aabd6-139">Varaus näkyy sitovana varauksena.</span><span class="sxs-lookup"><span data-stu-id="aabd6-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="aabd6-140">Napsauta varausta hiiren kakkospainikkeella Muuta tilaa -kohdassa. Valitse Alustava varaus ja sitten Alustava.</span><span class="sxs-lookup"><span data-stu-id="aabd6-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="aabd6-141">Varauksen tila on nyt Alustava.</span><span class="sxs-lookup"><span data-stu-id="aabd6-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="aabd6-142">Kun aikataulutaulukko suljetaan, näet, että resurssin tuntien varaus on muuttunut sitovasta alustavaksi ryhmän jäsenen ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="aabd6-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="aabd6-143">Huomaa, että jos varaat resurssin sitovasti ryhmälle, delegoit työrakenteen tehtävät ja muutat tilan Ylläpidä varauksia -toiminnon avulla sitovasta alustavaksi, kyseisen resurssin tehtävien delegoinnit poistetaan. Näin tehdään sen vuoksi, että vain sitovasti varattuja resursseja voi delegoida tehtäville.</span><span class="sxs-lookup"><span data-stu-id="aabd6-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="aabd6-144">Tee alustava varaus luomalla yleinen resurssi</span><span class="sxs-lookup"><span data-stu-id="aabd6-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="aabd6-145">Voit luoda alustavan varauksen luomalla yleisen resurssin ryhmän jäsenen, täyttämällä aikataulutaulukon tai resurssipyynnön ja muuttamalla tyyppiä varauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="aabd6-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="aabd6-146">Voit tehdä niin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aabd6-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="aabd6-147">Delegoi roolit projektin työrakenteen niihin tehtäviin, joille haluat luoda yleisen ryhmän jäsenet.</span><span class="sxs-lookup"><span data-stu-id="aabd6-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="aabd6-148">Valitse Luo projektiryhmä.</span><span class="sxs-lookup"><span data-stu-id="aabd6-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="aabd6-149">Valitse projektiryhmän ruudukossa yleinen resurssi ja valitse sitten Varaa.</span><span class="sxs-lookup"><span data-stu-id="aabd6-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="aabd6-150">Valitse aikataulutaulukossa varattava resurssi.</span><span class="sxs-lookup"><span data-stu-id="aabd6-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="aabd6-151">Muuta aikataulutaulukon Luo resurssin varaus -paneelissa varauksen tilaksi Alustava.</span><span class="sxs-lookup"><span data-stu-id="aabd6-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="aabd6-152">Valitse Varaa tai Varaa ja lopeta.</span><span class="sxs-lookup"><span data-stu-id="aabd6-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="aabd6-153">Kun olet sulkenut aikataulutaulukon, valittu Alustava-tilassa oleva resurssi ja sen delegoidut tunnit näkyvät ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="aabd6-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="aabd6-154">Näet myös, että yleinen resurssi on yhä ryhmässä. Se osoittaa, että tehtävät on delegoitu alustavasti varatulle ryhmän jäsenelle.</span><span class="sxs-lookup"><span data-stu-id="aabd6-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="aabd6-155">Kun olet valmis muuttamaan alustavasti varatun ryhmän jäsenen resurssin sitovasti varatuksi ryhmän jäseneksi, jolle voi delegoida tehtäviä, tee seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="aabd6-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="aabd6-156">Valitse resurssi ja valitse sitten Ylläpidä varauksia -kohta.</span><span class="sxs-lookup"><span data-stu-id="aabd6-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="aabd6-157">Kun aikataulutaulukko avautuu, laajenna resurssia niin, että varaukset näkyvät.</span><span class="sxs-lookup"><span data-stu-id="aabd6-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="aabd6-158">Näkyviin tulee varaus, joka on merkitty alustavaksi.</span><span class="sxs-lookup"><span data-stu-id="aabd6-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="aabd6-159">Napsauta varausta hiiren kakkospainikkeella Muuta tilaa -kohdassa. Valitse Sitova varaus ja sitten Sitova.</span><span class="sxs-lookup"><span data-stu-id="aabd6-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="aabd6-160">Varauksen tila on nyt Sitova.</span><span class="sxs-lookup"><span data-stu-id="aabd6-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="aabd6-161">Kun aikataulutaulukko suljetaan, näet, että resurssin tuntien varaus on muuttunut alustavasta sitovaksi ryhmän jäsenen ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="aabd6-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="aabd6-162">Voit nyt delegoida resurssin tehtäville (jos tehtävän sitovasti varatut tunnit ja työtunnit vastaavat toisiaan delegoinnissa).</span><span class="sxs-lookup"><span data-stu-id="aabd6-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="aabd6-163">Huomaa, että jos seurasit yleisen resurssin täyttämisen vaiheita ylempänä kohteessa kolme, kun muutit alustavasti varatun resurssin tilan sitovaksi, yleisen ryhmän jäsen poistetaan ryhmästä.</span><span class="sxs-lookup"><span data-stu-id="aabd6-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]