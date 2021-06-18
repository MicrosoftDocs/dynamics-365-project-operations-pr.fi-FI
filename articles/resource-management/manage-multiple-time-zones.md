---
title: Aikavyöhykkeiden hallinta
description: Kun projekti luodaan, sen aika vyöhyke perustuu käytettyyn työtuntimalliin määritettyyn aikavyöhykkeeseen.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997732"
---
# <a name="manage-time-zones"></a><span data-ttu-id="13d89-103">Aikavyöhykkeiden hallinta</span><span class="sxs-lookup"><span data-stu-id="13d89-103">Manage time zones</span></span>

<span data-ttu-id="13d89-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="13d89-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="13d89-105">Projektit</span><span class="sxs-lookup"><span data-stu-id="13d89-105">Projects</span></span>

<span data-ttu-id="13d89-106">Kun projekti luodaan, sen aika vyöhyke perustuu käytetyssä työtuntimallissa määritettyyn aikavyöhykkeeseen.</span><span class="sxs-lookup"><span data-stu-id="13d89-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="13d89-107">**Projektissa** päivämäärät ovat aina suhteessa sen käyttäjän aikavyöhykkeeseen, joka on kirjautunut kuhunkin välilehteen **Tehtävä**-välilehteä lukuun ottamatta. Kun tarkastelet työrakennetta, päivämäärät näkyvät aina projektin aikavyöhykkeessä.</span><span class="sxs-lookup"><span data-stu-id="13d89-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="13d89-108">Tehtävät</span><span class="sxs-lookup"><span data-stu-id="13d89-108">Tasks</span></span>

<span data-ttu-id="13d89-109">Kun tehtävä luodaan, alkamisaikaa, päättymisaikaa ja tuntia/päivää ohjataan projektin työaikojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="13d89-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="13d89-110">Jos tehtävän on esimerkiksi luonut projekti, jonka aika vyöhyke on -8 PST ja jonka työaika on klo 9:00 – 17:00 maanantaista perjantaihin, mikä tahansa ilman delegointia luotu tehtävä noudattaa projektikalenterin alkamisaikaa ja päättymisaikaa.</span><span class="sxs-lookup"><span data-stu-id="13d89-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="13d89-111">Resurssien hallinta aikavyöhykkeissä</span><span class="sxs-lookup"><span data-stu-id="13d89-111">Manage resources with time zones</span></span>

<span data-ttu-id="13d89-112">Jotta saat tarkat ja ennustettavat tulokset, kun käytät **Laajenna varausta** -toimintoa, on täytettävä kaksi keskeistä edellytystä:</span><span class="sxs-lookup"><span data-stu-id="13d89-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="13d89-113">Käyttäjän on määritettävä laitteensa aikavyöhyke vastaamaan järjestelmän **mukautusasetuksissa** määritettyä aikavyöhykettä.</span><span class="sxs-lookup"><span data-stu-id="13d89-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Aikavyöhykeasetukset Windows 10:ssä](media/reconcile-assignments-03.png)

  ![Aikavyöhykeasetukset mukautusasetuksissa](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="13d89-116">Varattavissa olevalla resurssilla on oltava vähintään yksi minuutti työaikaa, joka on päällekkäinen pyydetyn laajennuksen määrittämiseen käytettävien tietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="13d89-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="13d89-117">Esimerkiksi seuraavat resurssit ovat työaikoja, jotka ovat välillä 9:00–19:00.</span><span class="sxs-lookup"><span data-stu-id="13d89-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Resurssien muotojen vertailu](media/reconcile-assignments-05.png)

<span data-ttu-id="13d89-119">Seuraavassa taulukossa näkyy:</span><span class="sxs-lookup"><span data-stu-id="13d89-119">The following table shows:</span></span>

- <span data-ttu-id="13d89-120">Projektin kalenterimalli</span><span class="sxs-lookup"><span data-stu-id="13d89-120">A project calendar template</span></span>
- <span data-ttu-id="13d89-121">Resurssi A: Tällä resurssilla on sama kalenteri ja se on samassa aikavyöhykkeessä kuin projekti.</span><span class="sxs-lookup"><span data-stu-id="13d89-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="13d89-122">Varausten alkamisaika on 9.00.</span><span class="sxs-lookup"><span data-stu-id="13d89-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="13d89-123">Resurssi B: Tämä resurssi sijaitsee eri aikavyöhykkeellä kuin projekti, ja projekti alkaa klo 7:00 resurssin aikavyöhykkeessä.</span><span class="sxs-lookup"><span data-stu-id="13d89-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="13d89-124">Varaukset alkavat kuitenkin alkaen klo 9.00, koska se on määritysmallin varhaisin alkamisaika.</span><span class="sxs-lookup"><span data-stu-id="13d89-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="13d89-125">Resurssit C ja D: Resurssit sijaitsevat eri aikavyöhykkeillä, molemmat eri vyöhykkeillä verrattuna toisiinsa ja projektiin, ja resurssien varaukset alkavat aikaisintaan niiden käytettävissä olevina alkamisaikoina.</span><span class="sxs-lookup"><span data-stu-id="13d89-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="13d89-126">Entiteetti</span><span class="sxs-lookup"><span data-stu-id="13d89-126">Entity</span></span>  |<span data-ttu-id="13d89-127">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="13d89-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="13d89-128">Projektin kalenterimalli</span><span class="sxs-lookup"><span data-stu-id="13d89-128">Project calendar template</span></span>   | ![projektikalenteri](media/reconcile-assignments-06.png) |
|<span data-ttu-id="13d89-130">Resurssi A</span><span class="sxs-lookup"><span data-stu-id="13d89-130">Resource A</span></span>  | ![Resurssin A kalenteri](media/reconcile-assignments-06.png) |
|<span data-ttu-id="13d89-132">Resurssi B</span><span class="sxs-lookup"><span data-stu-id="13d89-132">Resource B</span></span>  |  ![Resurssin B kalenteri](media/reconcile-assignments-07.png) |
|<span data-ttu-id="13d89-134">Resurssi C</span><span class="sxs-lookup"><span data-stu-id="13d89-134">Resource C</span></span>  |  ![Resurssin C kalenteri](media/reconcile-assignments-08.png) |
|<span data-ttu-id="13d89-136">Resurssi D</span><span class="sxs-lookup"><span data-stu-id="13d89-136">Resource D</span></span>  | ![Resurssin D kalenteri](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="13d89-138">Kun siirryt **Täsmäytys**-näkymään, näkyviin tulevat resurssien delegoinnit ja niihin liittyvä varausvajeet.</span><span class="sxs-lookup"><span data-stu-id="13d89-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Täsmäytysnäkymä ennen laajentamista](media/reconcile-assignments-10.png)

<span data-ttu-id="13d89-140">Kun Laajenna varausta -toimintoa on käytetty kunkin resurssin kohdalla, varauksia laajennetaan onnistuneesti kullekin resurssille, koska kunkin resurssin työaika on päällekkäinen vajeen aikavälin kanssa.</span><span class="sxs-lookup"><span data-stu-id="13d89-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Täsmäytysnäkymä varauksen laajentamisen jälkeen](media/reconcile-assignments-11.png) 

<span data-ttu-id="13d89-142">Huomaa, että lähemmät tiedot varauksista osoittavat, miten varausten alkamisaika on erilainen.</span><span class="sxs-lookup"><span data-stu-id="13d89-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="13d89-143">Varaus alkaa aikaisintaan delegoinnin aikavälin alussa ja aikaisintaan resurssin käytettävissäoloajan alkamisaikana.</span><span class="sxs-lookup"><span data-stu-id="13d89-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Resurssien uudet varaukset aikataulutaulukossa](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]