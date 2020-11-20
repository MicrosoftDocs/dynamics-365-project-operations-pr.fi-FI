---
title: Resurssien hallinnan keskeiset käsitteet
description: Tämä aihe tarjoaa tietoja Microsoft Dynamics Project Operationsin resurssinhallintatoiminnosta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a14f0ec328049d1b199201955c384df9fac61e39
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123869"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="96839-103">Resurssien hallinnan keskeiset käsitteet</span><span class="sxs-lookup"><span data-stu-id="96839-103">Resource management key concepts</span></span>

<span data-ttu-id="96839-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="96839-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="96839-105">Resurssit ovat palvelupohjaisen organisaation tärkeimpiä varoja.</span><span class="sxs-lookup"><span data-stu-id="96839-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="96839-106">Mahdollisuus löytää oikeat resurssit oikeaan aikaan, varata resurssit projekteihin ja pitää ne käytössä, auttaa organisaatiota täyttämään tulotavoitteet ja asiakastyytyväisyystavoitteet.</span><span class="sxs-lookup"><span data-stu-id="96839-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="96839-107">Dynamics 365 Project Operations resursointitoimintojen avulla voit tehdä seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="96839-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="96839-108">Luo projektiryhmiä varaamalla vapaita ja päteviä resursseja.</span><span class="sxs-lookup"><span data-stu-id="96839-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="96839-109">Luo yleisiä ryhmänjäsentietueita ja määritä niiden roolit ja resurssiorganisaatioyksikkö.</span><span class="sxs-lookup"><span data-stu-id="96839-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="96839-110">Luo resurssivaatimuksia yleisille ryhmän jäsenille niiden tehtäväkohdennuksista.</span><span class="sxs-lookup"><span data-stu-id="96839-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="96839-111">Yhdistä taitoja tunnistamalla taidot, jotka on määritelty resurssitarpeissa ja vertaamalla niitä resurssien taitoihin.</span><span class="sxs-lookup"><span data-stu-id="96839-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="96839-112">Korvaa resursseja.</span><span class="sxs-lookup"><span data-stu-id="96839-112">Substitute resources.</span></span>
- <span data-ttu-id="96839-113">Saata projektin aikataulukohdennukset samalle tasolle resurssivarausten kanssa.</span><span class="sxs-lookup"><span data-stu-id="96839-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="96839-114">Täsmäytä varausten ja kohdennusten erot.</span><span class="sxs-lookup"><span data-stu-id="96839-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="96839-115">Muuta resurssivarauksia vastauksena poissa toimistolta -tilaan.</span><span class="sxs-lookup"><span data-stu-id="96839-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="96839-116">Tee yhteistyötä projektipäälliköiden ja resurssipäälliköiden välillä.</span><span class="sxs-lookup"><span data-stu-id="96839-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="96839-117">Tarkastele resurssien käytön historiaa suhteessa tavoitteeseen, mukaan lukien erittely siitä, miten resurssien aikaa on käytetty.</span><span class="sxs-lookup"><span data-stu-id="96839-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="96839-118">Ylläpidä osaamis- ja pätevyystietovarastoa.</span><span class="sxs-lookup"><span data-stu-id="96839-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="96839-119">Voit miehittää projektisi ryhmällä yleisiä tai nimettyjä resursseja Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="96839-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="96839-120">Voit käyttää useita tapoja ryhmän jäsenten lisäämiseen ja kohdentamiseen ja heidän varaustensa ja kohdennustensa hallintaan.</span><span class="sxs-lookup"><span data-stu-id="96839-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
