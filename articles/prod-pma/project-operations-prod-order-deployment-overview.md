---
title: Project Operationsin varastoitavien ja tuotantopohjaisten skenaarioiden käyttöönoton yleiskatsaus
description: Tässä aiheessa on tietoja käyttöönottotyypistä, Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ffbcb326e5cd86c49b3b3b27ce7d68404a6842b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289230"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="dd0fc-103">Project Operationsin varastoitavien ja tuotantopohjaisten skenaarioiden käyttöönoton yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="dd0fc-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="dd0fc-104">_**Koskee:** Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="dd0fc-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="dd0fc-105">Tällä käyttötyypillä on seuraavat projektipohjaisten yritysten ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="dd0fc-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="dd0fc-106">[Työrakennetta](work-breakdown-structures.md) käyttävä projektisuunnittelu</span><span class="sxs-lookup"><span data-stu-id="dd0fc-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="dd0fc-107">Projektien varastoitujen varastojen hankkiminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="dd0fc-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="dd0fc-108">Projektipohjaisen myynnin hallinta käyttämällä Dynamics 365 Finance and Operations -sovelluksen **Myynti ja markkinointi** -moduulia.</span><span class="sxs-lookup"><span data-stu-id="dd0fc-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="dd0fc-109">Projektin hinnoittelu ja kustannuslaskenta käyttämällä Finance and Operations -sovellusten kustannushinnan ja laskutushinnan määrityksiä</span><span class="sxs-lookup"><span data-stu-id="dd0fc-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="dd0fc-110">Projektien resurssien hallinta Finance and Operations -sovelluksissa</span><span class="sxs-lookup"><span data-stu-id="dd0fc-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="dd0fc-111">Projektin edistymisen ja ajan seuranta Finance and Operations -sovelluksissa</span><span class="sxs-lookup"><span data-stu-id="dd0fc-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="dd0fc-112">Projektikulujen ja muiden kuin projektikulujen kulujen hallintakokemus kuittien sieppaamisen avulla käyttämällä OCR-ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="dd0fc-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="dd0fc-113">Laskutus käyttämällä yritysluokan arvonlisäveroa ja voimassaolopäivämäärän vaihtokurssijärjestelmää</span><span class="sxs-lookup"><span data-stu-id="dd0fc-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="dd0fc-114">Keskeneräisen työn kirjanpidon ja jaksotusten määritettävät projektiryhmät</span><span class="sxs-lookup"><span data-stu-id="dd0fc-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="dd0fc-115">Projektin tuloutus</span><span class="sxs-lookup"><span data-stu-id="dd0fc-115">Project revenue recognition</span></span>

<span data-ttu-id="dd0fc-116">Tämä käyttöönottotyyppi lisäksi laajentaa Dynamics 365 Finance- ja Dynamics 365 Supply Chain Management -sovellusten toimintoja.</span><span class="sxs-lookup"><span data-stu-id="dd0fc-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="dd0fc-117">Valitse käyttöönottotyyppi, joka käyttää Dynamics 365 Project Operationsia koko projektin elinkaaren ajan ja jossa on oltava seuraavat keskeiset edellytykset:</span><span class="sxs-lookup"><span data-stu-id="dd0fc-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="dd0fc-118">Kattava projektinhallintajärjestelmä, jolla hallitaan inventoituja nimikkeitä sekä aikataulujen ja taloushallinnon sisäisten ja laskutettavien projektien työn tai tuotantotilauksen kustannuslaskenta.</span><span class="sxs-lookup"><span data-stu-id="dd0fc-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="dd0fc-119">Organisaatiossa on jo Dynamics 365 Finance- tai Dynamics 365 Supply Chain and Manufacturing -sovelluksia ja projektipohjaisten tapahtumien integrointi yksinkertaistaa tietojen käyttöä ja raportointitarpeita.</span><span class="sxs-lookup"><span data-stu-id="dd0fc-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="dd0fc-120">Täysin toimiva kulujenhallintajärjestelmä, joka sisältää projektin ja muiden kuin projektin kulujen seurannan käytäntövalvonnan ja korvaukset.</span><span class="sxs-lookup"><span data-stu-id="dd0fc-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="dd0fc-121">Yritysluokan arvonlisävero- ja vaihtokurssimoduuli tarvitaan projektin asiakkaille suunnattujen laskujen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="dd0fc-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="dd0fc-122">Kansainvälisten tilinpäätösstandardien (IFRS) mukainen projektin kirjanpito- ja tuloutusjärjestelmä.</span><span class="sxs-lookup"><span data-stu-id="dd0fc-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]