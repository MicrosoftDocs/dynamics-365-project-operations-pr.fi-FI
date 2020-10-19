---
title: Projektin päivittäminen
description: Tässä aiheessa on tietoja projektien päivittämisestä Project Operationsissa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897808"
---
# <a name="update-a-project"></a><span data-ttu-id="b31f3-103">Projektin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="b31f3-103">Update a project</span></span>

<span data-ttu-id="b31f3-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="b31f3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b31f3-105">Alla on yhteenveto kentistä, jotka voidaan päivittää projektiin sen jälkeen, kun se on luotu, sekä mahdolliset päivitysten vaikutukset.</span><span class="sxs-lookup"><span data-stu-id="b31f3-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="b31f3-106">Projektin tietokentät</span><span class="sxs-lookup"><span data-stu-id="b31f3-106">Project detail fields</span></span>

- <span data-ttu-id="b31f3-107">**Nimi**: Projektin otsikko.</span><span class="sxs-lookup"><span data-stu-id="b31f3-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="b31f3-108">**Kuvaus**: Projektin yleiskuvaus.</span><span class="sxs-lookup"><span data-stu-id="b31f3-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="b31f3-109">**Asiakas**: Yritys, jolle projekti toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="b31f3-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="b31f3-110">**Kalenterimalli**: Projektin työtunnit.</span><span class="sxs-lookup"><span data-stu-id="b31f3-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="b31f3-111">Kun tätä kenttää muutetaan, koko aikataulu lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b31f3-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="b31f3-112">**Valuutta**: Projektin valuutta.</span><span class="sxs-lookup"><span data-stu-id="b31f3-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="b31f3-113">Tämä kentän oletusarvo on valuutta, joka on määritetty sopimusyksikössä.</span><span class="sxs-lookup"><span data-stu-id="b31f3-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="b31f3-114">Kun sopimusyksikkö päivitetään, myös tämä kenttä päivittyy.</span><span class="sxs-lookup"><span data-stu-id="b31f3-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="b31f3-115">**Sopimusyksikkö**: Organisaatioyksikkö, joka edustaa sitä yrityksen ryhmää tai osastoa, joka on pääasiallisesti vastuussa myynnin parantamisesta ja työn ja palvelujen asiakkaalle toimittamisen hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="b31f3-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="b31f3-116">**Projektipäällikkö**: Projektiryhmän jäsen, jolla on valtuudet tarkastella ja hyväksyä aikamerkintöjä ja kuluja.</span><span class="sxs-lookup"><span data-stu-id="b31f3-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="b31f3-117">Arviokentät</span><span class="sxs-lookup"><span data-stu-id="b31f3-117">Estimate fields</span></span>

- <span data-ttu-id="b31f3-118">**Arvioitu alkamispäivä**: Päivämäärä, jolloin projekti alkaa.</span><span class="sxs-lookup"><span data-stu-id="b31f3-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="b31f3-119">Kun tämä kenttä päivitetään, kaikki projektin tehtävät siirtyvät suhteessa uuteen alkamispäivään.</span><span class="sxs-lookup"><span data-stu-id="b31f3-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="b31f3-120">**Päättymispäivä**: Päivä määrä, jona projekti on aikataulutettu päättymään.</span><span class="sxs-lookup"><span data-stu-id="b31f3-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="b31f3-121">**Työmäärä**: Projektin arvioitu työmäärä.</span><span class="sxs-lookup"><span data-stu-id="b31f3-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="b31f3-122">Kun projektiin lisätään tehtäviä, tätä kenttää ei enää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="b31f3-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="b31f3-123">**Arvioitu työvoimakustannus**: Projektin arvioitu työvoimakustannus.</span><span class="sxs-lookup"><span data-stu-id="b31f3-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="b31f3-124">Kun projektiin lisätään työnvoimakustannuksia, tätä kenttää ei enää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="b31f3-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="b31f3-125">**Arvioidut kulut**: Projektin arvioidut kulut.</span><span class="sxs-lookup"><span data-stu-id="b31f3-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="b31f3-126">Kun projektiin lisätään kuluja, tätä kenttää ei enää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="b31f3-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="b31f3-127">Projektin toteutuneiden arvojen kentät</span><span class="sxs-lookup"><span data-stu-id="b31f3-127">Project actual fields</span></span>
- <span data-ttu-id="b31f3-128">**Todellinen aloituspäivämäärä**: Päivämäärä, jolloin projekti alkoi.</span><span class="sxs-lookup"><span data-stu-id="b31f3-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="b31f3-129">**Todellinen päättymispäivä**: Päivitetään, kun projekti on valmis.</span><span class="sxs-lookup"><span data-stu-id="b31f3-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="b31f3-130">Projektin tilakentät</span><span class="sxs-lookup"><span data-stu-id="b31f3-130">Project status fields</span></span>

- <span data-ttu-id="b31f3-131">**Projektin yleinen tila**: Projektipäällikön määrittämä projektin kunto.</span><span class="sxs-lookup"><span data-stu-id="b31f3-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="b31f3-132">**Kommentit**: Projektipäällikön kirjoittama kuvaus projektin nykyisestä kunnosta.</span><span class="sxs-lookup"><span data-stu-id="b31f3-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

