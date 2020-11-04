---
title: Projektin asetukset
description: Tässä aiheessa on tietoja projektinhallinnan asetuksista.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075511"
---
# <a name="project-settings"></a><span data-ttu-id="de27f-103">Projektin asetukset</span><span class="sxs-lookup"><span data-stu-id="de27f-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="de27f-104">Seuraavien asetusten avulla voit käyttää projektin suunnitteluominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="de27f-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="de27f-105">Työmalli</span><span class="sxs-lookup"><span data-stu-id="de27f-105">Work template</span></span>

<span data-ttu-id="de27f-106">Määritä projektin aikataulun luomista varten projektikalenteri, joka määrittää päivittäisten työtuntien määrän ja mahdolliset yrityksen kiinnioloajat.</span><span class="sxs-lookup"><span data-stu-id="de27f-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="de27f-107">Projektikalenterimallin luomiseksi työmalli liitetään projektin **Kalenterimalli** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="de27f-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="de27f-108">Luo työmalli seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="de27f-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="de27f-109">Napauta PSA:n vasemmanpuoleisessa navigointipaneelissa **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="de27f-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="de27f-110">Avaa **Resurssit** -listaussivulla käyttäjän tietue, ja valitse sitten **Näytä työtunnit**.</span><span class="sxs-lookup"><span data-stu-id="de27f-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="de27f-111">Varmista, että ponnahdusikkunat on sallittu selaimen sivulla.</span><span class="sxs-lookup"><span data-stu-id="de27f-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="de27f-112">Näin näet resurssille määritetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="de27f-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="de27f-113">Napauta **Kuukausinäkymä** -välilehdellä **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="de27f-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="de27f-114">Kolme vaihtoehtoa sisältävä lista tulee näkyviin:</span><span class="sxs-lookup"><span data-stu-id="de27f-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="de27f-115">Uusi viikkoaikataulu</span><span class="sxs-lookup"><span data-stu-id="de27f-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="de27f-116">Yhden päivän työaikataulu</span><span class="sxs-lookup"><span data-stu-id="de27f-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="de27f-117">Vapaa-aika</span><span class="sxs-lookup"><span data-stu-id="de27f-117">Time Off</span></span>

> ![Määritystoiminnot](media/project-13.png)

4. <span data-ttu-id="de27f-119">Valise **Uusi viikkoaikataulu** , ja määritä sen jälkeen tiedot tälle resurssiaikataululle.</span><span class="sxs-lookup"><span data-stu-id="de27f-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="de27f-120">Voit määrittää toistuvan viikoittaisen aikataulun, päivittäiset tuntiparametrit, yrityksen kiinnioloajat ja muita seikkoja.</span><span class="sxs-lookup"><span data-stu-id="de27f-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="de27f-121">Määritä päivämääräväli, valitse **Tallenna** , ja napauta sen jälkeen **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="de27f-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="de27f-122">Palaa **Resurssit** -luettelosivulle ja valitse resurssi, jolle määrität työtunnit.</span><span class="sxs-lookup"><span data-stu-id="de27f-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="de27f-123">Valitse **Määritä kalenteri** määrittääksesi työmallin.</span><span class="sxs-lookup"><span data-stu-id="de27f-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="de27f-124">Syötä **Työmalli** -dialogilaatikossa työmallin nimi, ja valitse sen jälkeen **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="de27f-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="de27f-125">Voit nyt liittää työmallin projektin kalenterimalliin.</span><span class="sxs-lookup"><span data-stu-id="de27f-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="de27f-126">Resurssiroolit</span><span class="sxs-lookup"><span data-stu-id="de27f-126">Resource roles</span></span>

<span data-ttu-id="de27f-127">Termi *resurssirooli* viittaa joukkoon taitoja, osaamista ja sertifikaatteja, jotka henkilöllä on oltava, jotta hän voisi suorittaa tietyn tehtäväjoukon projektissa.</span><span class="sxs-lookup"><span data-stu-id="de27f-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="de27f-128">PSA:n avulla voit laskea kustannukset ja laskuttaa resurssin ajasta perustuen siihen rooliin, johon resurssi on liitetty.</span><span class="sxs-lookup"><span data-stu-id="de27f-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="de27f-129">Jokaisen organisaation on määritettävä nämä roolit käyttämällä **Project Service** -valikon vasemmanpuoleista siirtymispainiketta.</span><span class="sxs-lookup"><span data-stu-id="de27f-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="de27f-130">Jokaisen organisaation on määritettävä nämä roolit **Aktiiviset resurssiluokat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="de27f-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="de27f-131">Valitse vasemmanpuoleisessa siirtymispaneelissa **Resurssiroolit** avataksesi tämän sivun.</span><span class="sxs-lookup"><span data-stu-id="de27f-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="de27f-132">hinnastot</span><span class="sxs-lookup"><span data-stu-id="de27f-132">Price lists</span></span>

<span data-ttu-id="de27f-133">Hinnastot antavat mahdollisuuden määrittää kustannus- ja myyntihinnat resurssirooleille, kululuokille, tuotteille ja muille organisaation elementeille.</span><span class="sxs-lookup"><span data-stu-id="de27f-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="de27f-134">Ennen kuin asetat talausarvion työlle, joka projektissa on toimitettava, sinun tulisi luoda sitä tukeva kustannus- ja myyntihinnasto.</span><span class="sxs-lookup"><span data-stu-id="de27f-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="de27f-135">Sinun tulisi myös määrittää parametrit-osiossa oletuskustannus- ja myyntihinnasto, jota sovelletaan kaikkiin organisaatiossa luotuihin projekteihin.</span><span class="sxs-lookup"><span data-stu-id="de27f-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="de27f-136">Varmista **Aktiiviset projektiparametrit** -sivulla, että määritit oletusarvoisen kustannus- ja myyntihinnaston.</span><span class="sxs-lookup"><span data-stu-id="de27f-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
