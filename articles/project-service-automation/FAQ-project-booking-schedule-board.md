---
title: Projektivarauksen luominen aikataulutaulukosta
description: Tässä aiheessa on tietoja projektivarauksen luomisesta aikataulutaulukosta.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751234"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="84ef2-103">Projektivarauksen luominen aikataulutaulukosta</span><span class="sxs-lookup"><span data-stu-id="84ef2-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="84ef2-104">Voit varata resurssin projektiin joko suoraan projektin **Ryhmä**-välilehdessä tai luomalla resurssitarpeen yleisestä ryhmän jäsenen delegoinnista ja täyttämällä luodun tarpeen projektin ryhmän jäsenellä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="84ef2-105">Voit varata resurssin projektiin myös suoraan aikataulutaulukosta.</span><span class="sxs-lookup"><span data-stu-id="84ef2-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="84ef2-106">Tähän on kolme ratkaisua:</span><span class="sxs-lookup"><span data-stu-id="84ef2-106">There are three ways to do this:</span></span>

- <span data-ttu-id="84ef2-107">**Varaus luodusta resurssitarpeesta:** Voit luoda resurssitarpeen, kun olet luonut yleisen resurssin ja kohdentanut tehtäviä projektin sisällä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="84ef2-108">**Varaus ensisijaisesta tarpeesta:** Ensisijaiset tarpeet tulevat näkyviin aikataulutaulukon **Projekti**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="84ef2-109">**Varaus uudesta resurssitarpeesta:** Voit luoda resurssitarpeen alusta ja yhdistää sen projektiin.</span><span class="sxs-lookup"><span data-stu-id="84ef2-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="84ef2-110">Resurssitarve näkyy aikataulutaulukossa **Avoimet tarpeet** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="84ef2-111">Varaus luodusta resurssitarpeesta</span><span class="sxs-lookup"><span data-stu-id="84ef2-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="84ef2-112">Voit luoda yleisen resurssin ja kohdentaa sille projektissa yhden tehtävän tai useita tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="84ef2-113">Tämän jälkeen voit luoda resurssitarpeen yleisen ryhmän jäsenestä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="84ef2-114">Aikataulutaulukossa tämä resurssi näkyy **Avoimet tarpeet** -välilehdessä. Jos avoimia tarpeita on useita, ruudukossa kannattaa käyttää sarakesuodattimia.</span><span class="sxs-lookup"><span data-stu-id="84ef2-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="84ef2-115">![Aikataulutaulukon Avoimet tarpeet -välilehti](media/FAQ-Project-Booking-Schedule-Board-1.png "Varausten ja delegointien taulukon näyttökuva")</span><span class="sxs-lookup"><span data-stu-id="84ef2-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="84ef2-116">Valitse tarve.</span><span class="sxs-lookup"><span data-stu-id="84ef2-116">Select the requirement.</span></span> <span data-ttu-id="84ef2-117">**Etsi saatavuus** -välilehti tulee näkyviin valitun rivin yläosassa.</span><span class="sxs-lookup"><span data-stu-id="84ef2-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="84ef2-118">Kun välilehti valitaan, aikataulutaulukon ajoitusavustajatila käynnistyy ja suodattaa käytettävissä olevat resurssitarvetta vastaavat resurssit.</span><span class="sxs-lookup"><span data-stu-id="84ef2-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="84ef2-119">Tämän jälkeen voit valita resurssin.</span><span class="sxs-lookup"><span data-stu-id="84ef2-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="84ef2-120">Voit myös vetää ja pudottaa valitun rivin aikataulutaulukon alaosasta yllä olevan ruudukon resurssisoluun.</span><span class="sxs-lookup"><span data-stu-id="84ef2-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="84ef2-121">Kun pudotat sen, **Luo resurssin varaus** -paneeli avautuu oikealle.</span><span class="sxs-lookup"><span data-stu-id="84ef2-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="84ef2-122">Kun valitset **Varaa**, resurssi varataan projektiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="84ef2-122">Selecting **Book** books the resource onto the project team.</span></span>

![Resurssivarauspaneelin luominen](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="84ef2-124">Varaus ensisijaisesta tarpeesta</span><span class="sxs-lookup"><span data-stu-id="84ef2-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="84ef2-125">Kun Project Service -sovelluksessa luodaan projekti, luodaan myös resurssitarve nimeltä Ensisijainen tarve.</span><span class="sxs-lookup"><span data-stu-id="84ef2-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="84ef2-126">Tämä on tyhjä tarve, jonka avulla resurssi voidaan varata nopeasti aikataulutaulukon avulla ilman, että tarve on luotava alusta alkaen tai muulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="84ef2-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="84ef2-127">Koska tarve on tyhjä, tarvittavat päivämäärät, kohdennustapa ja tunnit on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="84ef2-128">Jos haluat varata resurssin aikataulutaulukon Ensisijainen tarve -kohdassa, valitse **Projekti**-välilehti. Jos projekteja on useita, kannattaa käyttää **Projekti**-sarakkeen sarakesuodatinta.</span><span class="sxs-lookup"><span data-stu-id="84ef2-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="84ef2-129">![Sarakesuodattimet aikataulutaulukossa](media/FAQ-Project-Booking-Schedule-Board-2.png "Varausten ja delegointien taulukon näyttökuva")</span><span class="sxs-lookup"><span data-stu-id="84ef2-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="84ef2-130">Valitse tarve, jonka nimi on projektin nimi ja jonka kesto on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="84ef2-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="84ef2-131">Valitse rivillä näkyvä **Etsi saatavuus** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="84ef2-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="84ef2-132">Tällöin aikataulutaulukko siirtyy ajoitusavustajatilaan ja näyttää käytettävissä olevat resurssit, jotka voidaan varata projektiin.</span><span class="sxs-lookup"><span data-stu-id="84ef2-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="84ef2-133">Koska **Ensisijainen tarve** on tyhjä tarve, jonka kesto on 0 (nolla), kesto on määritettävä **Luo resurssin varaus** -paneelissa resurssin valitsemisen ja varaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="84ef2-134">Voit myös valita aikataulutaulukon alaosassa olevan **Projektin ensisijainen tarve** -kohdan ja varata sen vetämällä ja pudottamalla sen resurssiin.</span><span class="sxs-lookup"><span data-stu-id="84ef2-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="84ef2-135">Koska **Ensisijainen tarve** on tyhjä tarve, jonka kesto on 0 (nolla), kesto on määritettävä **Luo resurssin varaus** -paneelissa resurssin valitsemisen ja varaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="84ef2-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="84ef2-136">Kun resurssi varataan aikataulutaulukon **Ensisijainen tarve** -kohdan kautta, se voidaan lisätä projektiryhmään ilman kohdennuksia.</span><span class="sxs-lookup"><span data-stu-id="84ef2-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="84ef2-137">Varaus uudesta resurssitarpeesta</span><span class="sxs-lookup"><span data-stu-id="84ef2-137">Book from a new resource requirement</span></span>
<span data-ttu-id="84ef2-138">Resurssi voidaan varata uudesta resurssitarpeesta seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="84ef2-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="84ef2-139">Siirry **Resurssitarpeet**-kohtaan ja valitse **Uusi** luodaksesi uuden resurssitarpeen.</span><span class="sxs-lookup"><span data-stu-id="84ef2-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="84ef2-140">Valitse **Projekti** -välilehdessä projekti yhdistääksesi resurssin projektiin.</span><span class="sxs-lookup"><span data-stu-id="84ef2-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="84ef2-141">Aikataulutaulukossa tämä uusi tarve näkyy muodossa **Avoin tarve**, joka voidaan täyttää.</span><span class="sxs-lookup"><span data-stu-id="84ef2-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="84ef2-142">Lisää resurssi projektiryhmään varaamalla se.</span><span class="sxs-lookup"><span data-stu-id="84ef2-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="84ef2-143">Nyt kun resurssi on varattu, tehtävät on kohdennettava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="84ef2-143">Now that the resource is booked, you must assign tasks manually.</span></span>

