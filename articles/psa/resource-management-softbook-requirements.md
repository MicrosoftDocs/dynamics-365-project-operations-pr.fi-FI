---
title: Alustavat varaustarpeet
description: Tässä aiheessa on tietoja alustavien varaustarpeiden käytöstä.
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124094"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="dd774-103">Alustavat varaustarpeet</span><span class="sxs-lookup"><span data-stu-id="dd774-103">Soft-book requirements</span></span>

<span data-ttu-id="dd774-104">Resurssivaatimus voi olla sitova.</span><span class="sxs-lookup"><span data-stu-id="dd774-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="dd774-105">Sitova varaus luo ehdotuksen, joka kuluttaa resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="dd774-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="dd774-106">Tämän jälkeen ehdotus lähetetään pyytäjälle hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="dd774-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="dd774-107">Alustava varaus lisää alustavasti resurssin projektiryhmään, ja sillä on eri tila aikataulutaulukossa, mutta se ei kuluta resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="dd774-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="dd774-108">Jos haluat varata resurssin alustavasti aikataulutaulukosta, aseta **Varauksen tila** -kentän arvoksi **Alustava**.</span><span class="sxs-lookup"><span data-stu-id="dd774-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Varauksen tilaksi määritetty Alustava](media/Resource-Management-image77.png)

<span data-ttu-id="dd774-110">Kun **Ryhmä** -välilehti on **Nimetyt ryhmän jäsenet** -näkymässä, resurssi näkyy siinä.</span><span class="sxs-lookup"><span data-stu-id="dd774-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="dd774-111">Alustavasti varatut tunnit raportoidaan **Alustavasti varatut tunnit** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="dd774-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Alustavasti varatut tunnit Nimetyt ryhmän jäsenet -näkymässä](media/Resource-Management-image78.png)

<span data-ttu-id="dd774-113">Alustavasti varattuja ryhmän jäseniä voi kohdentaa tehtäviin.</span><span class="sxs-lookup"><span data-stu-id="dd774-113">Soft-booked team members can be assigned to tasks.</span></span>

![Alustavasti varattuja ryhmän jäseniä kohdennettuina tehtäviin](media/Resource-Management-image79.png)

<span data-ttu-id="dd774-115">**Täsmäytys**-välilehdellä ei näytetä varauksia alustavasti varatulle resurssille, koska **Täsmäytys**-välilehti ottaa huomioon vain sitovat varaukset.</span><span class="sxs-lookup"><span data-stu-id="dd774-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Alustavasti varattu resurssi ilman varauksia Täsmäytys-välilehdellä](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="dd774-117">Resurssia ei voi varata alustavasti vaatimuksesta, joka luotiin yleisestä ryhmän jäsenestä.</span><span class="sxs-lookup"><span data-stu-id="dd774-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="dd774-118">Aikataulutaulukossa käytetään eri väritystä alustavasti varatuille resursseille.</span><span class="sxs-lookup"><span data-stu-id="dd774-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Alustava varaus aikataulutaulukossa](media/Resource-Management-image81.png)

<span data-ttu-id="dd774-120">Muuttaaksesi alustavan varauksen sitovaksi varaukseksi, napsauta alustavaa varausta hiiren kakkospainikkeella aikataulutaulukossa ja valitse **Muuta tila** \> **Varaa sitovasti** \> **Sitova**.</span><span class="sxs-lookup"><span data-stu-id="dd774-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Varauksen tilan muuttaminen Sitovaksi](media/Resource-Management-image82.png)

<span data-ttu-id="dd774-122">Varausta muutetaan ja tila vaihtuu aikataulutaulukossa.</span><span class="sxs-lookup"><span data-stu-id="dd774-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="dd774-123">Koska varauksen tila on nyt **Sitova**, resurssi näkyy varattuna, ja sen kapasiteetti ja saatavuus ovat muuttuneet.</span><span class="sxs-lookup"><span data-stu-id="dd774-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="dd774-124">Voit käyttää samaa menetelmää sitovan varauksen tai alustavan varauksen peruuttamiseksi aikataulutaulukon kautta.</span><span class="sxs-lookup"><span data-stu-id="dd774-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="dd774-125">Muuttaaksesi alustavasti varatun resurssin sitovasti varatuksi, valitse resurssi projektin **Ryhmä**-välilehdellä ja valitse sitten **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="dd774-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Vahvista-komento](media/Resource-Management-image83.png)