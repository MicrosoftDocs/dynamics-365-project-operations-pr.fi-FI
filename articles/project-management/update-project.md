---
title: Projektin päivittäminen
description: Tässä aiheessa on tietoja projektien päivittämisestä Project Operationsissa.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993367"
---
# <a name="update-a-project"></a><span data-ttu-id="db389-103">Projektin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="db389-103">Update a project</span></span>

<span data-ttu-id="db389-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="db389-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="db389-105">Alla on yhteenveto kentistä, jotka voidaan päivittää projektiin sen jälkeen, kun se on luotu, sekä mahdolliset päivitysten vaikutukset.</span><span class="sxs-lookup"><span data-stu-id="db389-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="db389-106">Projektin tietokentät</span><span class="sxs-lookup"><span data-stu-id="db389-106">Project detail fields</span></span>

- <span data-ttu-id="db389-107">**Nimi**: Projektin otsikko.</span><span class="sxs-lookup"><span data-stu-id="db389-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="db389-108">**Kuvaus**: Projektin yleiskuvaus.</span><span class="sxs-lookup"><span data-stu-id="db389-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="db389-109">**Asiakas**: Yritys, jolle projekti toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="db389-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="db389-110">**Kalenterimalli**: Projektin työtunnit.</span><span class="sxs-lookup"><span data-stu-id="db389-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="db389-111">Kun tätä kenttää muutetaan, koko aikataulu lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="db389-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="db389-112">**Valuutta**: Projektin valuutta.</span><span class="sxs-lookup"><span data-stu-id="db389-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="db389-113">Tämä kentän oletusarvo on valuutta, joka on määritetty sopimusyksikössä.</span><span class="sxs-lookup"><span data-stu-id="db389-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="db389-114">Kun sopimusyksikkö päivitetään, myös tämä kenttä päivittyy.</span><span class="sxs-lookup"><span data-stu-id="db389-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="db389-115">**Sopimusyksikkö**: Organisaatioyksikkö, joka edustaa sitä yrityksen ryhmää tai osastoa, joka on pääasiallisesti vastuussa myynnin parantamisesta ja työn ja palvelujen asiakkaalle toimittamisen hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="db389-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="db389-116">**Projektipäällikkö**: Projektiryhmän jäsen, jolla on valtuudet tarkastella ja hyväksyä aikamerkintöjä ja kuluja.</span><span class="sxs-lookup"><span data-stu-id="db389-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="db389-117">Arviokentät</span><span class="sxs-lookup"><span data-stu-id="db389-117">Estimate fields</span></span>

- <span data-ttu-id="db389-118">**Arvioitu alkamispäivä**: Päivämäärä, jolloin projekti alkaa.</span><span class="sxs-lookup"><span data-stu-id="db389-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="db389-119">Kun tämä kenttä päivitetään, kaikki projektin tehtävät siirtyvät suhteessa uuteen alkamispäivään.</span><span class="sxs-lookup"><span data-stu-id="db389-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="db389-120">**Päättymispäivä**: Päivä määrä, jona projekti on aikataulutettu päättymään.</span><span class="sxs-lookup"><span data-stu-id="db389-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="db389-121">**Työmäärä**: Projektin arvioitu työmäärä.</span><span class="sxs-lookup"><span data-stu-id="db389-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="db389-122">Kun projektiin lisätään tehtäviä, tätä kenttää ei enää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="db389-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="db389-123">**Arvioitu työvoimakustannus**: Projektin arvioitu työvoimakustannus.</span><span class="sxs-lookup"><span data-stu-id="db389-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="db389-124">Kun projektiin lisätään työnvoimakustannuksia, tätä kenttää ei enää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="db389-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="db389-125">**Arvioidut kulut**: Projektin arvioidut kulut.</span><span class="sxs-lookup"><span data-stu-id="db389-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="db389-126">Kun projektiin lisätään kuluja, tätä kenttää ei enää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="db389-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="db389-127">Projektin toteutuneiden arvojen kentät</span><span class="sxs-lookup"><span data-stu-id="db389-127">Project actual fields</span></span>
- <span data-ttu-id="db389-128">**Todellinen aloituspäivämäärä**: Päivämäärä, jolloin projekti alkoi.</span><span class="sxs-lookup"><span data-stu-id="db389-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="db389-129">**Todellinen päättymispäivä**: Päivitetään, kun projekti on valmis.</span><span class="sxs-lookup"><span data-stu-id="db389-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="db389-130">Projektin tilakentät</span><span class="sxs-lookup"><span data-stu-id="db389-130">Project status fields</span></span>

- <span data-ttu-id="db389-131">**Projektin yleinen tila**: Projektipäällikön määrittämä projektin kunto.</span><span class="sxs-lookup"><span data-stu-id="db389-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="db389-132">**Kommentit**: Projektipäällikön kirjoittama kuvaus projektin nykyisestä kunnosta.</span><span class="sxs-lookup"><span data-stu-id="db389-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]