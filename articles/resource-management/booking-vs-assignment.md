---
title: Varausten ja delegointien vertailu
description: Tässä aiheessa on tietoja resurssivarausten ja resurssien delegointien välisistä eroista.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896007"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="869c5-103">Varausten ja delegointien vertailu</span><span class="sxs-lookup"><span data-stu-id="869c5-103">Bookings vs assignments</span></span>

<span data-ttu-id="869c5-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="869c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="869c5-105">Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin.</span><span class="sxs-lookup"><span data-stu-id="869c5-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="869c5-106">Sitovat varaukset kuluttavat resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="869c5-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="869c5-107">Kohdennukset ovat resurssien kohdennuksia projektitehtäviin projektiaikataulussa.</span><span class="sxs-lookup"><span data-stu-id="869c5-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="869c5-108">Resurssit voivat olla joko todellisia tai yleisiä.</span><span class="sxs-lookup"><span data-stu-id="869c5-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="869c5-109">Ihannetapauksessa todellisille resursseilla varausten ja kohdennusten tulisi olla ristiriidattomia, koska niissä ei ole eroja.</span><span class="sxs-lookup"><span data-stu-id="869c5-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="869c5-110">Microsoft Dynamics Project Operations ei kuitenkaan pakota tähän yhteensopivuuteen.</span><span class="sxs-lookup"><span data-stu-id="869c5-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="869c5-111">**Täsmäytys**-näkymä näyttää projektipäällikölle kohteet, joissa resurssin varaukset ja kohdennukset eivät täsmää.</span><span class="sxs-lookup"><span data-stu-id="869c5-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
