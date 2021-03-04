---
title: Manuaalisen proformalaskun luominen – lite
description: Tämä aihe tarjoaa tietoja Project Operationsin manuaalisen proformalaskun luomisesta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764499"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="16d09-103">Manuaalisen proformalaskun luominen – lite</span><span class="sxs-lookup"><span data-stu-id="16d09-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="16d09-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="16d09-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="16d09-105">Dynamics 365 Project Operationsissa proformalaskuja voidaan luoda manuaalisesti tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="16d09-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="16d09-106">Voit luoda proformalaskun manuaalisesti **Projektisopimuksen** luettelosivulta tai **Projektisopimuksen** tiedot-sivulta.</span><span class="sxs-lookup"><span data-stu-id="16d09-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="16d09-107">Projektisopimusten luettelosivu</span><span class="sxs-lookup"><span data-stu-id="16d09-107">Project Contracts list page</span></span>

<span data-ttu-id="16d09-108">Valitse **projektisopimusten** luettelosivulta vähintään yksi projektisopimus ja luo laskut kaikille valituille tietueille.</span><span class="sxs-lookup"><span data-stu-id="16d09-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="16d09-109">Järjestelmä tarkistaa, mikä valituista projektisopimuksista on **valmis laskutukseen**, joka on päivätty ennen kuluvan päivän päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="16d09-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="16d09-110">Näistä palvelusopimuksista järjestelmä luo luonnokset proformalaskuiksi.</span><span class="sxs-lookup"><span data-stu-id="16d09-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="16d09-111">Jos projektisopimuksessa on useita asiakkaita, asiakasta kohden voi olla yksi lasku ja useita laskuja projektisopimusta kohden.</span><span class="sxs-lookup"><span data-stu-id="16d09-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="16d09-112">Kaikki luodut projektilaskut ovat käytettävissä **Myynti**-alueen **laskutus**-osan **lasku**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="16d09-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="16d09-113">Projektisopimuksen tiedot-sivu</span><span class="sxs-lookup"><span data-stu-id="16d09-113">Project Contract details page</span></span>

<span data-ttu-id="16d09-114">Proformalasku voidaan luoda myös **Projektisopimuksen** tiedot -sivulta.</span><span class="sxs-lookup"><span data-stu-id="16d09-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="16d09-115">Järjestelmä tarkistaa, mikä projektisopimuksista on **valmis laskutukseen**, joka on päivätty ennen kuluvan päivän päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="16d09-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="16d09-116">Näistä palvelusopimuksista järjestelmä luo proformalaskujen luonnokset kunkin sopimusrivin asiakkaiden määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="16d09-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="16d09-117">Kun luodaan yksittäinen proformalasku, näkyviin tulee **lasku**-sivu.</span><span class="sxs-lookup"><span data-stu-id="16d09-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="16d09-118">Jos projektisopimuksesta luodaan useita laskuja, kaikki luodut laskut näkyvät **Laskut**-luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="16d09-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
