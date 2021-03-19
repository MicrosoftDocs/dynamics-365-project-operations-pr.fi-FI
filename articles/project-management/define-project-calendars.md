---
title: Projektikalenterien määrittäminen
description: Tässä aiheessa on tietoja projektikalenterin käyttämisestä projektin aikataulun seuraamisessa.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286964"
---
# <a name="define-project-calendars"></a><span data-ttu-id="fff39-103">Projektikalenterien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fff39-103">Define project calendars</span></span>

<span data-ttu-id="fff39-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="fff39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fff39-105">Määritä projektin aikataulun luomista varten projektikalenteri, joka määrittää päivittäisten työtuntien määrän ja mahdolliset yrityksen kiinnioloajat.</span><span class="sxs-lookup"><span data-stu-id="fff39-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="fff39-106">Projektikalenterimallin luomiseksi työmalli liitetään projektin **Kalenterimalli**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fff39-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="fff39-107">Luo työmalli seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="fff39-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="fff39-108">Valitse siirtymisruudun **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="fff39-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="fff39-109">Avaa **Resurssit**-listaussivulla käyttäjän tietue, ja valitse sitten **Näytä työtunnit**.</span><span class="sxs-lookup"><span data-stu-id="fff39-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="fff39-110">Varmista, että ponnahdusikkunat on sallittu selaimen sivulla.</span><span class="sxs-lookup"><span data-stu-id="fff39-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="fff39-111">Näin näet resurssille määritetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="fff39-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="fff39-112">Valitse **Kuukausinäkymä**-välilehdessä **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="fff39-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="fff39-113">Kolme vaihtoehtoa sisältävä lista tulee näkyviin:</span><span class="sxs-lookup"><span data-stu-id="fff39-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="fff39-114">Uusi viikkoaikataulu</span><span class="sxs-lookup"><span data-stu-id="fff39-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="fff39-115">Yhden päivän työaikataulu</span><span class="sxs-lookup"><span data-stu-id="fff39-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="fff39-116">Poissaolo</span><span class="sxs-lookup"><span data-stu-id="fff39-116">Time Off</span></span>

4. <span data-ttu-id="fff39-117">Valise **Uusi viikkoaikataulu**, ja määritä sen jälkeen tiedot tälle resurssiaikataululle.</span><span class="sxs-lookup"><span data-stu-id="fff39-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="fff39-118">Voit määrittää toistuvan viikoittaisen aikataulun, päivittäiset tuntiparametrit, yrityksen kiinnioloajat ja muita seikkoja.</span><span class="sxs-lookup"><span data-stu-id="fff39-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="fff39-119">Määritä päivämääräväli, valitse **Tallenna**, ja valitse sen jälkeen **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="fff39-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="fff39-120">Palaa **Resurssit**-luettelosivulle ja valitse resurssi, jolle määrität työtunnit.</span><span class="sxs-lookup"><span data-stu-id="fff39-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="fff39-121">Valitse **Määritä kalenteri** määrittääksesi työmallin.</span><span class="sxs-lookup"><span data-stu-id="fff39-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="fff39-122">Syötä **Työmalli**-dialogilaatikossa työmallin nimi, ja valitse sen jälkeen **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="fff39-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="fff39-123">Voit nyt liittää työmallin projektin kalenterimalliin.</span><span class="sxs-lookup"><span data-stu-id="fff39-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]