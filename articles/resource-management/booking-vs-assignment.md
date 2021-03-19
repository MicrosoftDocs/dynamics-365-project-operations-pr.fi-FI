---
title: Varausten ja delegointien vertailu
description: Tässä aiheessa on tietoja resurssivarausten ja resurssien delegointien välisistä eroista.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279899"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="55aed-103">Varausten ja delegointien vertailu</span><span class="sxs-lookup"><span data-stu-id="55aed-103">Bookings vs assignments</span></span>

<span data-ttu-id="55aed-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="55aed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55aed-105">Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin.</span><span class="sxs-lookup"><span data-stu-id="55aed-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="55aed-106">Sitovat varaukset kuluttavat resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="55aed-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="55aed-107">Varaukset ilmaiset tiimien organisaatiokäsitteitä, jotta ne ymmärtävät, miten resursseja käytetään eri projekteissa.</span><span class="sxs-lookup"><span data-stu-id="55aed-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="55aed-108">Dynamics 365 Project Operations käsittelee varauksia projektitason konseptina.</span><span class="sxs-lookup"><span data-stu-id="55aed-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="55aed-109">Varauksista poiketen delegoinnit ovat projektiaikataulun projektitehtäviin sitoutettuja resursseja.</span><span class="sxs-lookup"><span data-stu-id="55aed-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="55aed-110">Resurssit voivat olla nimettyjä tai yleisiä.</span><span class="sxs-lookup"><span data-stu-id="55aed-110">The resources can be named or generic.</span></span>  <span data-ttu-id="55aed-111">Kun resurssitarve johdetaan projektitehtävien delegoinnista, Project Operations käyttää resurssien delegoinnin jaksottumisia resurssitarpeen tietojen jaksottumisen muodostamiseen.</span><span class="sxs-lookup"><span data-stu-id="55aed-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="55aed-112">Resurssin delegointeja ei kuitenkaan ylläpidetä.</span><span class="sxs-lookup"><span data-stu-id="55aed-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="55aed-113">Resurssivaatimuksesta johdettujen varausten päivitykset eivät päivitä mitään resurssin delegointeja.</span><span class="sxs-lookup"><span data-stu-id="55aed-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="55aed-114">Yleensä resurssin varausten summa on yhtä suuri kuin resurssin delegointien summa yhdessä tai useassa tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="55aed-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="55aed-115">Project Operations ei kuitenkaan pakota tätä yhdenmukaisuutta.</span><span class="sxs-lookup"><span data-stu-id="55aed-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="55aed-116">Projektipäällikkö näkee **Täsmäytys**-näkymässä kohteet, joissa resurssin varaukset ja delegoinnit eivät täsmää.</span><span class="sxs-lookup"><span data-stu-id="55aed-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]