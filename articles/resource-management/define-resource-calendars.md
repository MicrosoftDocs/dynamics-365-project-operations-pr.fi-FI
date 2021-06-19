---
title: Resurssikalenterien määrittäminen
description: Tässä aiheessa on tietoja siitä, miten resurssien työtuntikalenterit määritetään Project Operationsissa.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5ac834e16afc2f559bee6e10434f7015e8a8e51f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012177"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="15c42-103">Resurssikalenterien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="15c42-103">Define resource calendars</span></span>

<span data-ttu-id="15c42-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="15c42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="15c42-105">Jokaisella projektiin varattavalla resurssilla on oltava työaikakalenteri, jotta sen avulla voi määrittää käytettävyyden.</span><span class="sxs-lookup"><span data-stu-id="15c42-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="15c42-106">Resurssin työtunnit voidaan määrittää kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="15c42-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="15c42-107">Määritä resurssin yksilölliset kalenterisäännöt</span><span class="sxs-lookup"><span data-stu-id="15c42-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="15c42-108">Käytä resurssille aiemmin luotua kalenterimallia</span><span class="sxs-lookup"><span data-stu-id="15c42-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="15c42-109">Resurssin työtuntien määritys</span><span class="sxs-lookup"><span data-stu-id="15c42-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="15c42-110">Valitse **Resurssit**- valikosta **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="15c42-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="15c42-111">Valitse ruudukkonäkymästä käytettävä **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="15c42-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="15c42-112">Valitse **Resurssin tiedot**- sivulla **Työaika**-välilehti. Varattavien resurssien kalenterin oletusarvona on organisaatiolle määritetyn oletustyötuntimallin työaika.</span><span class="sxs-lookup"><span data-stu-id="15c42-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="15c42-113">Jos haluat päivittää työtunnit, napsauta hiiren kakkospainikkeella ehdotetun kalenterisäännön alkamispäivää.</span><span class="sxs-lookup"><span data-stu-id="15c42-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="15c42-114">Kalenterisääntö-valikon avulla voit määrittää tietyn päivän, sarjan loppuosan tai koko kalenterin kalenterisäännön.</span><span class="sxs-lookup"><span data-stu-id="15c42-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="15c42-115">Kun vaihtoehto on valittu, voit määrittää seuraavat asiat:</span><span class="sxs-lookup"><span data-stu-id="15c42-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="15c42-116">Viikonpäivä, jolloin työaika on käytössä.</span><span class="sxs-lookup"><span data-stu-id="15c42-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="15c42-117">Kunkin päivän työajat.</span><span class="sxs-lookup"><span data-stu-id="15c42-117">The working times within each day.</span></span>
    - <span data-ttu-id="15c42-118">Kalenterisäännön aikavyöhyke.</span><span class="sxs-lookup"><span data-stu-id="15c42-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="15c42-119">Säännölle voidaan määrittää tarvittaessa myös ei-työaika.</span><span class="sxs-lookup"><span data-stu-id="15c42-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="15c42-120">Kalenterimallin käyttäminen resurssille</span><span class="sxs-lookup"><span data-stu-id="15c42-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="15c42-121">Valitse **Resurssit**- valikosta **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="15c42-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="15c42-122">Valitse ruudukkonäkymästä enintään 25 **varattavissa olevaa resurssia** päivitettäväksi.</span><span class="sxs-lookup"><span data-stu-id="15c42-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="15c42-123">Valitse **Määritä kalenteri** ja näkyviin tulee valintaikkuna, jossa on käytettävissä olevien työtuntimallien luettelo.</span><span class="sxs-lookup"><span data-stu-id="15c42-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="15c42-124">Valitse käytettävä malli sen avulla ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="15c42-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]