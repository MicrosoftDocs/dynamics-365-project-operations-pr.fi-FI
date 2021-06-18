---
title: Projektivarauksen luominen aikataulutaulukosta
description: Tässä aiheessa on tietoja projektivarauksen luomisesta aikataulutaulukosta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992962"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="5a1cf-103">Projektivarauksen luominen aikataulutaulukosta</span><span class="sxs-lookup"><span data-stu-id="5a1cf-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5a1cf-104">Voit varata resurssin projektiin joko suoraan projektin **Ryhmä**-välilehdessä tai luomalla resurssitarpeen yleisestä ryhmän jäsenen delegoinnista ja täyttämällä luodun tarpeen projektin ryhmän jäsenellä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="5a1cf-105">Voit varata resurssin projektiin myös suoraan aikataulutaulukosta.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="5a1cf-106">Tähän on kolme ratkaisua:</span><span class="sxs-lookup"><span data-stu-id="5a1cf-106">There are three ways to do this:</span></span>

- <span data-ttu-id="5a1cf-107">**Varaus luodusta resurssitarpeesta:** Voit luoda resurssitarpeen, kun olet luonut yleisen resurssin ja kohdentanut tehtäviä projektin sisällä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="5a1cf-108">**Varaus ensisijaisesta tarpeesta:** Ensisijaiset tarpeet tulevat näkyviin aikataulutaulukon **Projekti**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="5a1cf-109">**Varaus uudesta resurssitarpeesta:** Voit luoda resurssitarpeen alusta ja yhdistää sen projektiin.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="5a1cf-110">Resurssitarve näkyy aikataulutaulukossa **Avoimet tarpeet** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="5a1cf-111">Varaus luodusta resurssitarpeesta</span><span class="sxs-lookup"><span data-stu-id="5a1cf-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="5a1cf-112">Voit luoda yleisen resurssin ja kohdentaa sille projektissa yhden tehtävän tai useita tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="5a1cf-113">Tämän jälkeen voit luoda resurssitarpeen yleisen ryhmän jäsenestä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="5a1cf-114">Aikataulutaulukossa tämä resurssi näkyy **Avoimet tarpeet** -välilehdessä. Jos avoimia tarpeita on useita, ruudukossa kannattaa käyttää sarakesuodattimia.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="5a1cf-115">![Aikataulutaulukon Avoimet tarpeet -välilehti](media/FAQ-Project-Booking-Schedule-Board-1.png "Varausten ja delegointien taulukon näyttökuva")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="5a1cf-116">Valitse tarve.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-116">Select the requirement.</span></span> <span data-ttu-id="5a1cf-117">**Etsi saatavuus** -välilehti tulee näkyviin valitun rivin yläosassa.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="5a1cf-118">Kun välilehti valitaan, aikataulutaulukon ajoitusavustajatila käynnistyy ja suodattaa käytettävissä olevat resurssitarvetta vastaavat resurssit.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="5a1cf-119">Tämän jälkeen voit valita resurssin.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="5a1cf-120">Voit myös vetää ja pudottaa valitun rivin aikataulutaulukon alaosasta yllä olevan ruudukon resurssisoluun.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="5a1cf-121">Kun pudotat sen, **Luo resurssin varaus** -paneeli avautuu oikealle.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="5a1cf-122">Kun valitset **Varaa**, resurssi varataan projektiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-122">Selecting **Book** books the resource onto the project team.</span></span>

![Resurssivarauspaneelin luominen](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="5a1cf-124">Varaus ensisijaisesta tarpeesta</span><span class="sxs-lookup"><span data-stu-id="5a1cf-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="5a1cf-125">Kun Project Service -sovelluksessa luodaan projekti, luodaan myös resurssitarve nimeltä Ensisijainen tarve.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="5a1cf-126">Tämä on tyhjä tarve, jonka avulla resurssi voidaan varata nopeasti aikataulutaulukon avulla ilman, että tarve on luotava alusta alkaen tai muulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="5a1cf-127">Koska tarve on tyhjä, tarvittavat päivämäärät, kohdennustapa ja tunnit on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="5a1cf-128">Jos haluat varata resurssin aikataulutaulukon Ensisijainen tarve -kohdassa, valitse **Projekti**-välilehti. Jos projekteja on useita, kannattaa käyttää **Projekti**-sarakkeen sarakesuodatinta.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="5a1cf-129">![Sarakesuodattimet aikataulutaulukossa](media/FAQ-Project-Booking-Schedule-Board-2.png "Varausten ja delegointien taulukon näyttökuva")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="5a1cf-130">Valitse tarve, jonka nimi on projektin nimi ja jonka kesto on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="5a1cf-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="5a1cf-131">Valitse rivillä näkyvä **Etsi saatavuus** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="5a1cf-132">Tällöin aikataulutaulukko siirtyy ajoitusavustajatilaan ja näyttää käytettävissä olevat resurssit, jotka voidaan varata projektiin.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="5a1cf-133">Koska **Ensisijainen tarve** on tyhjä tarve, jonka kesto on 0 (nolla), kesto on määritettävä **Luo resurssin varaus** -paneelissa resurssin valitsemisen ja varaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="5a1cf-134">Voit myös valita aikataulutaulukon alaosassa olevan **Projektin ensisijainen tarve** -kohdan ja varata sen vetämällä ja pudottamalla sen resurssiin.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="5a1cf-135">Koska **Ensisijainen tarve** on tyhjä tarve, jonka kesto on 0 (nolla), kesto on määritettävä **Luo resurssin varaus** -paneelissa resurssin valitsemisen ja varaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="5a1cf-136">Kun resurssi varataan aikataulutaulukon **Ensisijainen tarve** -kohdan kautta, se voidaan lisätä projektiryhmään ilman kohdennuksia.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="5a1cf-137">Varaus uudesta resurssitarpeesta</span><span class="sxs-lookup"><span data-stu-id="5a1cf-137">Book from a new resource requirement</span></span>
<span data-ttu-id="5a1cf-138">Resurssi voidaan varata uudesta resurssitarpeesta seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="5a1cf-139">Siirry **Resurssitarpeet**-kohtaan ja valitse **Uusi** luodaksesi uuden resurssitarpeen.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="5a1cf-140">Valitse **Projekti** -välilehdessä projekti yhdistääksesi resurssin projektiin.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="5a1cf-141">Aikataulutaulukossa tämä uusi tarve näkyy muodossa **Avoin tarve**, joka voidaan täyttää.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="5a1cf-142">Lisää resurssi projektiryhmään varaamalla se.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="5a1cf-143">Nyt kun resurssi on varattu, tehtävät on kohdennettava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]