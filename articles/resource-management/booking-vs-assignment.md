---
title: Varausten ja delegointien vertailu
description: Tässä aiheessa on tietoja resurssivarausten ja resurssien delegointien välisistä eroista.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130214"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="e30ab-103">Varausten ja delegointien vertailu</span><span class="sxs-lookup"><span data-stu-id="e30ab-103">Bookings vs assignments</span></span>

<span data-ttu-id="e30ab-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="e30ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e30ab-105">Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin.</span><span class="sxs-lookup"><span data-stu-id="e30ab-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="e30ab-106">Sitovat varaukset kuluttavat resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="e30ab-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="e30ab-107">Varaukset ilmaiset tiimien organisaatiokäsitteitä, jotta ne ymmärtävät, miten resursseja käytetään eri projekteissa.</span><span class="sxs-lookup"><span data-stu-id="e30ab-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="e30ab-108">Dynamics 365 Project Operationsissa varaukset ovat projektitason käsite.</span><span class="sxs-lookup"><span data-stu-id="e30ab-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="e30ab-109">Varauksista poiketen delegoinnit ovat projektiaikataulun projektitehtäviin sitoutettuja resursseja.</span><span class="sxs-lookup"><span data-stu-id="e30ab-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="e30ab-110">Resurssit voivat olla nimettyjä tai yleisiä.</span><span class="sxs-lookup"><span data-stu-id="e30ab-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="e30ab-111">Yleensä resurssin varausten summa on yhtä suuri kuin resurssin delegointien summa yhdessä tai useassa tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="e30ab-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="e30ab-112">Project Operations ei kuitenkaan pakota tätä yhdenmukaisuutta.</span><span class="sxs-lookup"><span data-stu-id="e30ab-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="e30ab-113">Projektipäällikkö näkee **Täsmäytys**-näkymässä kohteet, joissa resurssin varaukset ja delegoinnit eivät täsmää.</span><span class="sxs-lookup"><span data-stu-id="e30ab-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
