---
title: Resurssivaatimusten täyttäminen
description: Tässä aiheessa on tietoja resurssivaatimusten täyttämisestä.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: c6d61db6-b7f4-4b88-b894-b422c9fbf03d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 23ab3ca56f242fc1940f29fb50b04125300e04ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751254"
---
# <a name="fulfilling-resource-requests"></a><span data-ttu-id="d9deb-103">Resurssipyyntöjen täyttäminen</span><span class="sxs-lookup"><span data-stu-id="d9deb-103">Fulfilling resource requests</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d9deb-104">Resurssivaatimukset voidaan lähettää resurssipyyntöinä resursspäälikkölle, joka vastaa näiden pyyntöjen täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="d9deb-104">Resource requirements can be sent as resource requests to the resource manager who is responsible for fulfilling those requests.</span></span>

<span data-ttu-id="d9deb-105">Resurssipyynnöt näkyvät luettelomuodossa näkymässä **Aktiiviset resurssipyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="d9deb-105">Resource requests are shown as a list in the **Active Resource Requests** view.</span></span>

> ![Luettelo resurssipyynnöistä](media/Resource-Management-image59.png)

<span data-ttu-id="d9deb-107">Voit täyttää pyynnön valitsemalla sen luettelosta ja valitsemalla sen jälkeen **Etsi resurssit**.</span><span class="sxs-lookup"><span data-stu-id="d9deb-107">To fulfill a request, select it in the list, and then select **Find Resources**.</span></span> <span data-ttu-id="d9deb-108">Vaihtoehtoisesti voit kaksoisnapauttaa riviä pyynnön avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="d9deb-108">Alternatively, double-click a row to open the request.</span></span> <span data-ttu-id="d9deb-109">Voit valita sen jälkeen **Resurssivaatimus**-välilehden tarkastellaksesi vaatimuksia tälle pyynnölle.</span><span class="sxs-lookup"><span data-stu-id="d9deb-109">You can then select the **Resource Requirement** tab to view the requirements for that request.</span></span> <span data-ttu-id="d9deb-110">Jos haluat aloittaa pyynnön toteuttamisen, valitse **Etsi resurssit**.</span><span class="sxs-lookup"><span data-stu-id="d9deb-110">To start to fulfill the request, select **Find Resources**.</span></span>

> ![Resursspyynnön tiedot](media/Resource-Management-image60.png)

<span data-ttu-id="d9deb-112">Aikatauluavustaja tulee näkyviin, ja se suodatetaan vaatimusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="d9deb-112">The Schedule Assistant appears and is filtered by the requirements.</span></span> <span data-ttu-id="d9deb-113">Valitse ensin resurri ja sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="d9deb-113">Select the resource, and then select **Book**.</span></span>

> ![Resurssi valittu](media/Resource-Management-image61.png)

<span data-ttu-id="d9deb-115">Yleinen ryhmän jäsen korvataan sitovalla projektiryhmän nimetyn resurssin varauksella ja tehtäväkohdennuksilla projektiaikataulussa.</span><span class="sxs-lookup"><span data-stu-id="d9deb-115">The generic team member is replaced with the hard-booked named resource on the project team and task assignments in the project schedule.</span></span>
