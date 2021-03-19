---
title: Kausityypit
description: Tässä aiheessa on tietoja tuoton arvioinnin kausityyppien määrittämisestä.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287279"
---
# <a name="period-types"></a><span data-ttu-id="1f8f2-103">Kausityypit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-103">Period types</span></span>

<span data-ttu-id="1f8f2-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="1f8f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1f8f2-105">Kausityyppi määrittää, miten usein projektin tuotto arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="1f8f2-106">Tässä aiheessa on tietoja tuoton arvioinnin kausityyppien määrittämisestä.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="1f8f2-107">Kausityyppien luominen ja käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="1f8f2-107">Create and work with period types</span></span>
<span data-ttu-id="1f8f2-108">Jos haluat luoda ja käsitellä kausityyppejä, suorita seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="1f8f2-109">Siirry Dynamics 365 Finance -ympäristössä kohtaan **Projektinhallinta ja kirjanpito** > **Asetukset** > **Arviot** > **Kausityypit**.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="1f8f2-110">Valitse **Uusi** uuden kausityypin luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-110">Select **New** to create new period type.</span></span> <span data-ttu-id="1f8f2-111">Syötä nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-111">Enter a name and description.</span></span>
3. <span data-ttu-id="1f8f2-112">Valitse arvo kentässä **Toistumistiheys**:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="1f8f2-113">Jos valitset arvon **Viikoittain**, **Kahden viikon välein**, **Kaksi kertaa kuukaudessa**, **Kuukausittain**, **Päivittäin**, **Neljännesvuosittain** tai **Vuosittain**, kausien luomiseen käytetään kalenteria.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="1f8f2-114">Jos valitset **Kirjanpitojakson**, kirjanpitojaksoja yleisen tapahtumaluettelon määrityksestä käytetään jaksojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="1f8f2-115">Jos valitset arvon **Rajoittamaton**, voit määrittää mukautettuja kausia.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="1f8f2-116">Valitse kausityyppitietue ja valitse sitten **Luo kaudet** luodaksesi kausityypille kaudet.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="1f8f2-117">Valitsemasi kausitiheyden perusteella voi olla mahdollista määrittää alkamispäivä tai kuinka monta kautta luodaan.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="1f8f2-118">Valitse **Kaudet** tarkastellaksesi luotuja kausia.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]