---
title: Project Operationsin kaksoiskirjoituksen integrointi
description: Tässä aiheessa on yleiskatsaus Project Operationsin kaksoiskirjoituksen integroinnista.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955654"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="c2e7f-103">Project Operationsin kaksoiskirjoituksen integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c2e7f-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="c2e7f-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="c2e7f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c2e7f-105">Project Operations käyttää [kaksoiskirjoitustoimintoja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) sykronoidakseen tietoa Microsoft Dataversen ja Dynamics 365 Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="c2e7f-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="c2e7f-106">Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan osana tätä Dataversen ja Financen välistä integrointia.</span><span class="sxs-lookup"><span data-stu-id="c2e7f-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operationsin tietovuon yleiskatsaus](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="c2e7f-108">Project Operations Dataversessä tarjoaa uudenaikaisen käyttöliittymän ja helpon koodittoman ja vähäkoodisen laajennettavuuden käyttämällä Power Platformin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c2e7f-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="c2e7f-109">Projektipäälliköt, henkilöstöpäälliköt, projektiryhmän jäsenet ja muut toimiston jäsenet suorittavat tehtävänsä Project Operationsissa Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="c2e7f-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="c2e7f-110">Financen Project Operations tukee projektien kirjanpitoa ja tuottojen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="c2e7f-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="c2e7f-111">Project Operations liittää Financen rahoituskehykseen arvonlisäveron laskemista, valuuttakursseja, taloudellisen dimension raportointia ja muuta varten.</span><span class="sxs-lookup"><span data-stu-id="c2e7f-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="c2e7f-112">Projektin kirjanpitäjän kokemukset perustuvat enimmäkseen Financeen.</span><span class="sxs-lookup"><span data-stu-id="c2e7f-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="c2e7f-113">Project Operationsin integrointi koostuu seuraavasta komponenttien integroinnista:</span><span class="sxs-lookup"><span data-stu-id="c2e7f-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="c2e7f-114">Project Operationsin määritysten ja määritystietojen integrointi</span><span class="sxs-lookup"><span data-stu-id="c2e7f-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="c2e7f-115">Projektin arviot ja toteutuneet kulut</span><span class="sxs-lookup"><span data-stu-id="c2e7f-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="c2e7f-116">Projektin laskut</span><span class="sxs-lookup"><span data-stu-id="c2e7f-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="c2e7f-117">Kulujen hallinta</span><span class="sxs-lookup"><span data-stu-id="c2e7f-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="c2e7f-118">Toimittajan lasku</span><span class="sxs-lookup"><span data-stu-id="c2e7f-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
