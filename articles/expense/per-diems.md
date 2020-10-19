---
title: Päivärahat
description: Tässä aiheessa on tietoja kulujen hallinnassa käytettävistä päivärahasäännöistä.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908080"
---
# <a name="per-diems"></a><span data-ttu-id="493c7-103">Päivärahat</span><span class="sxs-lookup"><span data-stu-id="493c7-103">Per diems</span></span>

<span data-ttu-id="493c7-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="493c7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="493c7-105">Päiväraha on palkka, joka maksetaan työhön matkustavalle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="493c7-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="493c7-106">Kulujen hallinnassa voit luoda päivärahasääntöjä eri matkatilanteisiin.</span><span class="sxs-lookup"><span data-stu-id="493c7-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="493c7-107">Päivärahahinnat voivat perustua vuodenaikaan, matkustuspaikkaan tai molempiin.</span><span class="sxs-lookup"><span data-stu-id="493c7-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="493c7-108">Kun luot päivärahasäännön, voit määrittää, että prosenttiosuus päivärahahinnasta pidätetään, jos työntekijä saa ilmaisia aterioita tai palveluita.</span><span class="sxs-lookup"><span data-stu-id="493c7-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="493c7-109">Voit myös määrittää tuntien vähimmäis- ja enimmäismäärät, joiden puitteissa päiväraha koskee työntekijän matkustamista.</span><span class="sxs-lookup"><span data-stu-id="493c7-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="493c7-110">Määritys</span><span class="sxs-lookup"><span data-stu-id="493c7-110">Configuration</span></span> 

1. <span data-ttu-id="493c7-111">Voit lisätä päivärahasijainteja valitsemalla **Määritä** > **Laskutoimitukset ja koodit** > **Päivärahasijainnit**.</span><span class="sxs-lookup"><span data-stu-id="493c7-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="493c7-112">Valitse kunkin yllä lisätyn sijainnin kohdalla päivärahahinta ja valuutta, joka on voimassa hotellin, aterioiden ja muiden kulujen alkamis- ja päättymispäivän välillä.</span><span class="sxs-lookup"><span data-stu-id="493c7-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="493c7-113">Päivärahahinnat ja valuutat määritetään kohdassa **Määritä** > **Laskutoimitukset ja koodit** > **Päivärahat**.</span><span class="sxs-lookup"><span data-stu-id="493c7-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="493c7-114">**Päivärahasijainnit**-sivulla määritetään päivärahahintojen tasot.</span><span class="sxs-lookup"><span data-stu-id="493c7-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="493c7-115">Päivärahahintojen tasojen avulla voit määrittää, kuinka monta prosenttia päivittäisestä korvauksesta jaetaan hotelli-, ateria- ja muiden kulujen mukaan.</span><span class="sxs-lookup"><span data-stu-id="493c7-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="493c7-116">Voit määrittää aamiaisen, lounaan tai päivällisen aterianvähennysprosentin päivittämällä kentät **Kulujen hallinnan parametrit** -sivun **Päiväraha**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="493c7-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="493c7-117">Kulujen lähettäminen päivärahan avulla</span><span class="sxs-lookup"><span data-stu-id="493c7-117">Submit expenses using per diem</span></span>
<span data-ttu-id="493c7-118">Jos haluat lähettää kuluja käyttäen päivärahoja, käytä **Päiväraha**-kululuokkaa, kun luot kuluraporttia.</span><span class="sxs-lookup"><span data-stu-id="493c7-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="493c7-119">Anna **Päivärahan alkupäivämäärä**-, **Päivärahan loppupäivämäärä** ja **Päivärahan sijainti**.</span><span class="sxs-lookup"><span data-stu-id="493c7-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="493c7-120">Summa lasketaan valitun sijainnin päivärahahintojen perusteella, ja ateriavähennys lasketaan päivärahatasojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="493c7-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
