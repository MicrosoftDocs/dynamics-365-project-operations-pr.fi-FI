---
title: Project Operationsin resursseihin ja ei-varastoitaviin perustuvien skenaarioiden käyttöönoton yleiskatsaus
description: Tässä aiheessa on tietoja käyttöönottotyypistä, Project Operationsin resursseihin ja ei-varastoitaviin perustuvista skenaarioista.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 770947835af41bd06c02ca08b6ed8e810b9bdcf8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289950"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="69fa5-103">Project Operationsin resursseihin ja ei-varastoitaviin perustuvien skenaarioiden käyttöönoton yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="69fa5-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="69fa5-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="69fa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="69fa5-105">Käyttöönottotyypissä Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvat skenaariot on seuraavat projektipohjaisten yritysten ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="69fa5-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="69fa5-106">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="69fa5-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="69fa5-107">Työresurssien moniulotteinen hinnoittelu ja kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="69fa5-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="69fa5-108">Kululuokkien luokkapohjainen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="69fa5-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="69fa5-109">Projektipohjainen myynnin hallinta Dynamics 365 Salesin ominaisuuksien avulla</span><span class="sxs-lookup"><span data-stu-id="69fa5-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="69fa5-110">Universal Resource Scheduling integroituu muiden sovellusten, kuten Dynamics 365 Field Servicen ja Dynamics 365 Customer Servicen, kanssa</span><span class="sxs-lookup"><span data-stu-id="69fa5-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="69fa5-111">Projektin edistymisen ja ajan seuranta</span><span class="sxs-lookup"><span data-stu-id="69fa5-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="69fa5-112">Projektikulujen ja muiden kuin projektikulujen, mukaan lukien kuittien sieppaaminen OCR-ominaisuuksien avulla, perustasoiset ja täydet kulujen hallintakokemukset.</span><span class="sxs-lookup"><span data-stu-id="69fa5-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="69fa5-113">Laskutus, joka laajentuu proformalaskutuksesta asiakkaalle suunnattuun laskutukseen ja joka perustuu yritysluokan arvonlisäveroon ja voimassaolopäivän vaihtokurssijärjestelmään.</span><span class="sxs-lookup"><span data-stu-id="69fa5-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="69fa5-114">Keskeneräisen työn kirjanpidon ja jaksotusten määritettävät projektikustannukset, tuottoprofiilit ja säännöt</span><span class="sxs-lookup"><span data-stu-id="69fa5-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="69fa5-115">Projektin tuloutus</span><span class="sxs-lookup"><span data-stu-id="69fa5-115">Project revenue recognition</span></span>
- <span data-ttu-id="69fa5-116">Laajennettavuus Power Platformin kautta</span><span class="sxs-lookup"><span data-stu-id="69fa5-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="69fa5-117">Tämä käyttöönottotyyppi laajentaa Dynamics 365 Finance- ja Dynamics 365 Supply Chain Management -sovellusten toimintoja.</span><span class="sxs-lookup"><span data-stu-id="69fa5-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="69fa5-118">Tämä käyttöönotto valitaan, jos Project Operationsin odotetaan käyttävän koko projektin elinkaaren, joka sisältää seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="69fa5-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="69fa5-119">Mahdollisuus hallita projektipohjaista myyntiä muiden myyntityyppien avulla käyttämällä Sales-sovelluksen ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="69fa5-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="69fa5-120">Integroitu projektinhallintajärjestelmä, joka hallitsee aikataulujen ja taloustietojen sisäisiä ja laskutettavia projekteja projektimyynnistä kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="69fa5-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="69fa5-121">Kulujenhallintajärjestelmä, joka sisältää projektin ja muiden kuin projektin kulujen seurannan käytäntövalvonnan ja korvaukset.</span><span class="sxs-lookup"><span data-stu-id="69fa5-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="69fa5-122">Monipuolinen yritysluokan arvonlisävero- ja vaihtokurssimoduuli tarvitaan projektin asiakkaille suunnattujen laskujen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="69fa5-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="69fa5-123">Kansainvälisten tilinpäätösstandardien (IFRS) mukainen projektin kirjanpito- ja tuloutusjärjestelmä.</span><span class="sxs-lookup"><span data-stu-id="69fa5-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="69fa5-124">Finance- tai Supply Chain Management -sovellukset ja projektipohjaisten tapahtumien integrointi.</span><span class="sxs-lookup"><span data-stu-id="69fa5-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]