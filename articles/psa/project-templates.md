---
title: Projektimallit
description: Tässä aiheessa on tietoja projektimallien käyttämisestä projektien nopeaan määrittämiseen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075510"
---
# <a name="project-templates"></a><span data-ttu-id="26382-103">Projektimallit</span><span class="sxs-lookup"><span data-stu-id="26382-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="26382-104">Projektimalli on esimääritetty kehys, jonka avulla voit nopeasti ja helposti käynnistää projektin.</span><span class="sxs-lookup"><span data-stu-id="26382-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="26382-105">Voit luoda uuden projektin yhdellä napsautuksella käyttämällä valmista mallia.</span><span class="sxs-lookup"><span data-stu-id="26382-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="26382-106">Kuten projekteillekin, myös projektimalleille on määritettävä esitiedot.</span><span class="sxs-lookup"><span data-stu-id="26382-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="26382-107">Jokaiselle projektimallille on määritettävä projekti alenteri, ja roolien ja hinnastojen on oltava ennalta määritettyjä organisaatiossa, jotta mallin komponenteilla on hyödyllisiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="26382-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="26382-108">Projektimalli koostuu kolmesta osasta: aikataulusta, projektiarvioista ja projektiryhmän jäsenistä.</span><span class="sxs-lookup"><span data-stu-id="26382-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="26382-109">Aikatauluta</span><span class="sxs-lookup"><span data-stu-id="26382-109">Schedule</span></span>

<span data-ttu-id="26382-110">Projektimallin aikataulussa on samat elementit kuin projektin aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="26382-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="26382-111">Voit luoda tehtävähierarkian, liittää rooleja tehtäviin, määrittää aikataulu-ominaisuuksia ja luoda riippuvuuksia.</span><span class="sxs-lookup"><span data-stu-id="26382-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="26382-112">Projektimallin aikataulu tukee myös kunkin tehtävän tehtävätiloja.</span><span class="sxs-lookup"><span data-stu-id="26382-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="26382-113">Siksi se tukee aikataulutusmoduulia.</span><span class="sxs-lookup"><span data-stu-id="26382-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="26382-114">Projektikalenteri on liitettävä projektiin.</span><span class="sxs-lookup"><span data-stu-id="26382-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="26382-115">Projektimallilla ja projektilla ei ole eroa työaikataulua luotaessa.</span><span class="sxs-lookup"><span data-stu-id="26382-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="26382-116">Projektin arviot</span><span class="sxs-lookup"><span data-stu-id="26382-116">Project estimates</span></span>

<span data-ttu-id="26382-117">Projektiarviot projektimallissa toimivat samalla tavalla kuin projektin arviot projektissa.</span><span class="sxs-lookup"><span data-stu-id="26382-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="26382-118">Kustannus- ja myyntihinnat kuitenkin haetaan oletuskustannus- ja myyntihinnastoista, jotka on määritetty parametreissa.</span><span class="sxs-lookup"><span data-stu-id="26382-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="26382-119">Projektin luominen mallista</span><span class="sxs-lookup"><span data-stu-id="26382-119">Creating a project from a template</span></span>
 
<span data-ttu-id="26382-120">Projektin voi luoda projektimallista useilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="26382-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="26382-121">Kun luot projektin tarjouksesta voit valita projektimallin **Nopea projektin luonti** -dialogiruudusta.</span><span class="sxs-lookup"><span data-stu-id="26382-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Pikaluonti: projektin dialogiruutu](media/project-11.png)

- <span data-ttu-id="26382-123">Kun luot projektin valitsemalla **Uusi projekti** , **Projekti** -sivu ilmestyy ennen tietueen tallennusta.</span><span class="sxs-lookup"><span data-stu-id="26382-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="26382-124">Valitse **Valitse malli** -kentässä jokin organisaation esimääritetyistä projektimalleista.</span><span class="sxs-lookup"><span data-stu-id="26382-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="26382-125">Käytä **Luo projekti mallista** -toimintoa **Mallikohde** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="26382-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="26382-126">Projektimallin osien kopioiminen projektiin</span><span class="sxs-lookup"><span data-stu-id="26382-126">Copying components of template to project</span></span>

<span data-ttu-id="26382-127">Kun kopioit projektimallin osia projektiin, projektin asetuksista riippuen voi tapahtua joitakin ohituksia.</span><span class="sxs-lookup"><span data-stu-id="26382-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="26382-128">Aikataulun kopioiminen</span><span class="sxs-lookup"><span data-stu-id="26382-128">Copying the schedule</span></span>

<span data-ttu-id="26382-129">Kopioitaessa aikataulu projektimallista, jos projektilla on eri kalenteri kuin mallilla, työtunteja projektin kalenterista käytetään tehtävän aikatauluun.</span><span class="sxs-lookup"><span data-stu-id="26382-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="26382-130">Näin aikataulu sopeutetaan täsmäämään taustaprojektin kalenteriin.</span><span class="sxs-lookup"><span data-stu-id="26382-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="26382-131">Vastaavasti aikataulun ensimmäinen tehtävä saa projektin aloituspäivämäärän, ja muun hierarkian aikataulua päivitetään perustuen mallissa määritettyyn kestoon ja riippuvuuksiin.</span><span class="sxs-lookup"><span data-stu-id="26382-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="26382-132">Projektin arvioiden kopiointi</span><span class="sxs-lookup"><span data-stu-id="26382-132">Copying project estimates</span></span> 

<span data-ttu-id="26382-133">Kopioitaessa projektiarviorivien välillä hinnastot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="26382-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="26382-134">Kustannushinnastossa nämä päivitykset perustuvat projektin omistavaan yksikköön.</span><span class="sxs-lookup"><span data-stu-id="26382-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="26382-135">Myyntihinnastossa ne perustuvat asiakkaaseen.</span><span class="sxs-lookup"><span data-stu-id="26382-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="26382-136">Projekteille, jotka liittyvät myyntikohteeseen, yksikkökustannus- ja myyntihinnat määritellään näiden hinnastojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="26382-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="26382-137">Projektiryhmän kopioiminen</span><span class="sxs-lookup"><span data-stu-id="26382-137">Copying a project team</span></span>

<span data-ttu-id="26382-138">Kun projektiryhmä kopioidaan projektimallista projektiin, kopioidaan yleiset resurssit, samoin kuin mallissa määritetyt taidot ja osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="26382-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="26382-139">Yleisten resurssien kohdennukset myös säilytetään sellaisina, kuin ne olivat projektimallissa.</span><span class="sxs-lookup"><span data-stu-id="26382-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="26382-140">Nimettyjä resursseja ei tueta projektimalleissa.</span><span class="sxs-lookup"><span data-stu-id="26382-140">Named resources aren't supported in project templates.</span></span>
