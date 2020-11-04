---
title: Projektin resurssien aikatauluttaminen
description: Projektin resurssien aikatauluttaminen Project Servicessä
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075554"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="66082-103">Projektin resurssien aikatauluttaminen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="66082-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="66082-104">Voit tarkistaa resurssien käytettävyyden, jotta saat yleisen käsityksen siitä, miten varattuja resurssit ovat, tai voit suodattaa näkymän taitojen, ryhmän, sijainnin ja muiden asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="66082-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="66082-105">Aikataulutaulukossa on luettelo resursseista ja heidän saatavuudestaan.</span><span class="sxs-lookup"><span data-stu-id="66082-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="66082-106">Valitse tila näyttämään saatavuus **tuntien** , **päivän** , **viikon** tai **kuukauden** mukaan.</span><span class="sxs-lookup"><span data-stu-id="66082-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="66082-107">Aikataulutaulukko on määritettävä, ennen kuin sitä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="66082-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="66082-108">Lisätietoja on aiheessa [Aikataulutaulukon määrittäminen (Field Service tai Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="66082-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="66082-109">Jos käytät vanhaa versiota, lisätietoja resurssien saatavuudesta on ohjeaiheessa [Resurssien saatavuuden näyttäminen](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="66082-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="66082-110">Aikataulutaulukon varaustoiminnon, osoitteiden maantieteellisten koodien ja sijaintipalvelujen käyttöä varten kartat on otettava käyttöön.</span><span class="sxs-lookup"><span data-stu-id="66082-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="66082-111">Valitse päävalikosta **Resurssien aikataulutus** > **Hallinta**.</span><span class="sxs-lookup"><span data-stu-id="66082-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="66082-112">Valitse **Aikataulutuksen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="66082-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="66082-113">Avaa tietue ja vieritä alas **Resource Scheduling Optimization** -osaan.</span><span class="sxs-lookup"><span data-stu-id="66082-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="66082-114">Valitse **Muodosta yhteys Mapsiin** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="66082-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="66082-115">Hyväksy ehdot ja tallenna tietue.</span><span class="sxs-lookup"><span data-stu-id="66082-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="66082-116">Valitse päävalikosta **Project Service** > **Aikataulutaulukko**.</span><span class="sxs-lookup"><span data-stu-id="66082-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="66082-117">Varaustarpeen voi tämän jälkeen aikatauluttaa manuaalisesti eri tavoin.</span><span class="sxs-lookup"><span data-stu-id="66082-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="66082-118">Valitse tapa, joka sopii sinulle.</span><span class="sxs-lookup"><span data-stu-id="66082-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="66082-119">Etsi käytettävissä olevat resurssit</span><span class="sxs-lookup"><span data-stu-id="66082-119">Find available resources</span></span>

1.  <span data-ttu-id="66082-120">Napsauta hiiren kakkospainikkeella **Varaustarve** -luettelossa aikatauluttamatonta varausta ja valitse jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="66082-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="66082-121">Etsi käytettävissä olevat resurssit aikataulutaulukon luettelosta valitsemalla **Etsi saatavuus – nykyiset resurssit**.</span><span class="sxs-lookup"><span data-stu-id="66082-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="66082-122">Etsi käytettävissä oleva resurssi järjestelmän resursseista valitsemalla **Etsi saatavuus – nykyiset resurssit**.</span><span class="sxs-lookup"><span data-stu-id="66082-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="66082-123">Kun toimit näin, suodattimet näyttävät valitun varaustarpeen vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="66082-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="66082-124">Kun havaitset käytettävissä olevan ajankohdan, napsauta sitä aikataulutaulukosta hiiren kakkospainikkeella ja valitse **Varaa tässä**.</span><span class="sxs-lookup"><span data-stu-id="66082-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="66082-125">Vaihtoehtoisesti voit vetää ja pudottaa varaustarpeen käytettävissä olevaan ajankohtaan.</span><span class="sxs-lookup"><span data-stu-id="66082-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="66082-126">Resurssin varaaminen päivittäisessä näkymässä ja alivarattujen resurssien etsiminen</span><span class="sxs-lookup"><span data-stu-id="66082-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="66082-127">Valitse aikataulutaulukosta ensin **Näyttötila** ja sitten **Päivät**.</span><span class="sxs-lookup"><span data-stu-id="66082-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="66082-128">Näkyviin tulee ruudukkonäkymä resurssin päiväkohtaisista varaustunneista ja vapaista päivistä.</span><span class="sxs-lookup"><span data-stu-id="66082-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="66082-129">Napsauta varattavan resurssin nimeä ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="66082-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="66082-130">Valitse **Resurssivaraus (luonti)** -valintaikkunasta projekti, jolle haluat varata resurssin, sekä varaustapa ja aloitus- ja päättymisajat.</span><span class="sxs-lookup"><span data-stu-id="66082-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="66082-131">Kun olet valmis, valitse **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="66082-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="66082-132">Aikataulutaulukon tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="66082-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="66082-133">Valitse alareunan luettelosta aikatauluttamaton resurssitarve.</span><span class="sxs-lookup"><span data-stu-id="66082-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="66082-134">Vedä varaustarve vapaaseen resurssiin/ajankohtaan aikataulutaulukossa.</span><span class="sxs-lookup"><span data-stu-id="66082-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="66082-135">Kun olet valmis, valitse **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="66082-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="66082-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="66082-136">Additional resources</span></span>  
 [<span data-ttu-id="66082-137">Resurssipäällikön opas</span><span class="sxs-lookup"><span data-stu-id="66082-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
