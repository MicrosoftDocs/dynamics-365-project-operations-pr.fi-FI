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
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751150"
---
# <a name="project-settings"></a><span data-ttu-id="c0639-103">Projektin asetukset</span><span class="sxs-lookup"><span data-stu-id="c0639-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c0639-104">Seuraavien asetusten avulla voit käyttää projektin suunnitteluominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c0639-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="c0639-105">Työmalli</span><span class="sxs-lookup"><span data-stu-id="c0639-105">Work template</span></span>

<span data-ttu-id="c0639-106">Määritä projektin aikataulun luomista varten projektikalenteri, joka määrittää päivittäisten työtuntien määrän ja mahdolliset yrityksen kiinnioloajat.</span><span class="sxs-lookup"><span data-stu-id="c0639-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="c0639-107">Projektikalenterimallin luomiseksi työmalli liitetään projektin **Kalenterimalli**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c0639-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="c0639-108">Luo työmalli seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="c0639-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="c0639-109">Napauta PSA:n vasemmanpuoleisessa navigointipaneelissa **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="c0639-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="c0639-110">Avaa **Resurssit**-listaussivulla käyttäjän tietue, ja valitse sitten **Näytä työtunnit**.</span><span class="sxs-lookup"><span data-stu-id="c0639-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c0639-111">Varmista, että ponnahdusikkunat on sallittu selaimen sivulla.</span><span class="sxs-lookup"><span data-stu-id="c0639-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="c0639-112">Näin näet resurssille määritetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="c0639-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="c0639-113">Napauta **Kuukausinäkymä**-välilehdellä **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="c0639-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="c0639-114">Kolme vaihtoehtoa sisältävä lista tulee näkyviin:</span><span class="sxs-lookup"><span data-stu-id="c0639-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="c0639-115">Uusi viikkoaikataulu</span><span class="sxs-lookup"><span data-stu-id="c0639-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="c0639-116">Yhden päivän työaikataulu</span><span class="sxs-lookup"><span data-stu-id="c0639-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="c0639-117">Vapaa-aika</span><span class="sxs-lookup"><span data-stu-id="c0639-117">Time Off</span></span>

> ![Määritystoiminnot](media/project-13.png)

4. <span data-ttu-id="c0639-119">Valise **Uusi viikkoaikataulu**, ja määritä sen jälkeen tiedot tälle resurssiaikataululle.</span><span class="sxs-lookup"><span data-stu-id="c0639-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="c0639-120">Voit määrittää toistuvan viikoittaisen aikataulun, päivittäiset tuntiparametrit, yrityksen kiinnioloajat ja muita seikkoja.</span><span class="sxs-lookup"><span data-stu-id="c0639-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="c0639-121">Määritä päivämääräväli, valitse **Tallenna**, ja napauta sen jälkeen **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="c0639-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="c0639-122">Palaa **Resurssit**-luettelosivulle ja valitse resurssi, jolle määrität työtunnit.</span><span class="sxs-lookup"><span data-stu-id="c0639-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="c0639-123">Valitse **Määritä kalenteri** määrittääksesi työmallin.</span><span class="sxs-lookup"><span data-stu-id="c0639-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="c0639-124">Syötä **Työmalli**-dialogilaatikossa työmallin nimi, ja valitse sen jälkeen **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="c0639-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="c0639-125">Voit nyt liittää työmallin projektin kalenterimalliin.</span><span class="sxs-lookup"><span data-stu-id="c0639-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="c0639-126">Resurssiroolit</span><span class="sxs-lookup"><span data-stu-id="c0639-126">Resource roles</span></span>

<span data-ttu-id="c0639-127">Termi *resurssirooli* viittaa joukkoon taitoja, osaamista ja sertifikaatteja, jotka henkilöllä on oltava, jotta hän voisi suorittaa tietyn tehtäväjoukon projektissa.</span><span class="sxs-lookup"><span data-stu-id="c0639-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="c0639-128">PSA:n avulla voit laskea kustannukset ja laskuttaa resurssin ajasta perustuen siihen rooliin, johon resurssi on liitetty.</span><span class="sxs-lookup"><span data-stu-id="c0639-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="c0639-129">Jokaisen organisaation on määritettävä nämä roolit käyttämällä **Project Service**-valikon vasemmanpuoleista siirtymispainiketta.</span><span class="sxs-lookup"><span data-stu-id="c0639-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="c0639-130">Jokaisen organisaation on määritettävä nämä roolit **Aktiiviset resurssiluokat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c0639-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="c0639-131">Valitse vasemmanpuoleisessa siirtymispaneelissa **Resurssiroolit** avataksesi tämän sivun.</span><span class="sxs-lookup"><span data-stu-id="c0639-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="c0639-132">hinnastot</span><span class="sxs-lookup"><span data-stu-id="c0639-132">Price lists</span></span>

<span data-ttu-id="c0639-133">Hinnastot antavat mahdollisuuden määrittää kustannus- ja myyntihinnat resurssirooleille, kululuokille, tuotteille ja muille organisaation elementeille.</span><span class="sxs-lookup"><span data-stu-id="c0639-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="c0639-134">Ennen kuin asetat talausarvion työlle, joka projektissa on toimitettava, sinun tulisi luoda sitä tukeva kustannus- ja myyntihinnasto.</span><span class="sxs-lookup"><span data-stu-id="c0639-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="c0639-135">Sinun tulisi myös määrittää parametrit-osiossa oletuskustannus- ja myyntihinnasto, jota sovelletaan kaikkiin organisaatiossa luotuihin projekteihin.</span><span class="sxs-lookup"><span data-stu-id="c0639-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="c0639-136">Varmista **Aktiiviset projektiparametrit** -sivulla, että määritit oletusarvoisen kustannus- ja myyntihinnaston.</span><span class="sxs-lookup"><span data-stu-id="c0639-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
