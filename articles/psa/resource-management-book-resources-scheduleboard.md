---
title: Käytä aikataulutaulukkoa projektin resurssien varaamiseen
description: Tässä aiheessa on tietoja resurssien varaamisesta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: ac3438da6bae45683d9eb2dee3544dff862e3ddd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120224"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="2c5dd-103">Käytä aikataulutaulukkoa projektin resurssien varaamiseen</span><span class="sxs-lookup"><span data-stu-id="2c5dd-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="2c5dd-104">Sen lisäksi, että projektiin voidaan varata resursseja projektista, on mahdollista varata resursseja sitovasti tai ei-sitovasti aikataulutaulukosta.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="2c5dd-105">Ennen kuin aikataulutaulukosta on mahdollista varata, on luotava resurssitarpeet.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="2c5dd-106">Seuraa näitä vaiheita luodaksesi resurssitarpeet aikataulutaulokon kautta.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="2c5dd-107">Jos **Resurssitarpeet**-ruutu sivun alalaidassa on kutistettu, valtse laajennin sen laajentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="2c5dd-108">Valitse **Varaustarpeet**-ruudussa **Projekti**-välilehdellä varaustarve.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![Projekti-välilehdellä valittu tarve](media/Resource-Management-image73.png)

3. <span data-ttu-id="2c5dd-110">Valitse **Etsi saatavuus**, jos haluat suodattaa varattavissa olevat resurssit ja tarkastella käytettävissä olevia resursseja.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="2c5dd-111">Valitse vähintään yksi resurssi aikataulutaulukosta.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="2c5dd-112">Syötä **Luo resurssivaraus** -ruudussa sivun oikeassa laidassa varaustiedot ja valitse sitten **Varaa ja poistu**.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Luo resurssin varausruutu valitulle varattavissa olevalle resurssille](media/Resource-Management-image74.png)

6. <span data-ttu-id="2c5dd-114">Kun tarve on valittu **Luo resurssivaraus** -ruudussa, valitse vähintään yksi resurssin solu luodaksesi varauksen.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Useita resurssille valittuja soluja](media/Resource-Management-image75.png)

7. <span data-ttu-id="2c5dd-116">Valitse **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-116">Select **Book**.</span></span>

<span data-ttu-id="2c5dd-117">Tarve täytetään valitulla resurssilla.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="2c5dd-118">Huomaa, että **Varausvaatimukset**-ruudussa vaatimukset on päivitetty, ja resurssi näkyy varattuna projektissa.</span><span class="sxs-lookup"><span data-stu-id="2c5dd-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Projektiin varattu resurssi](media/Resource-Management-image76.png)
