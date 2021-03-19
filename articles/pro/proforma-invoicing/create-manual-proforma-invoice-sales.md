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
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274184"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="f54fe-103">Manuaalisen proformalaskun luominen – lite</span><span class="sxs-lookup"><span data-stu-id="f54fe-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="f54fe-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f54fe-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f54fe-105">Dynamics 365 Project Operationsissa proformalaskuja voidaan luoda manuaalisesti tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f54fe-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="f54fe-106">Voit luoda proformalaskun manuaalisesti **Projektisopimuksen** luettelosivulta tai **Projektisopimuksen** tiedot-sivulta.</span><span class="sxs-lookup"><span data-stu-id="f54fe-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="f54fe-107">Projektisopimusten luettelosivu</span><span class="sxs-lookup"><span data-stu-id="f54fe-107">Project Contracts list page</span></span>

<span data-ttu-id="f54fe-108">Valitse **projektisopimusten** luettelosivulta vähintään yksi projektisopimus ja luo laskut kaikille valituille tietueille.</span><span class="sxs-lookup"><span data-stu-id="f54fe-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="f54fe-109">Järjestelmä tarkistaa, mikä valituista projektisopimuksista on **valmis laskutukseen**, joka on päivätty ennen kuluvan päivän päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="f54fe-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="f54fe-110">Näistä palvelusopimuksista järjestelmä luo luonnokset proformalaskuiksi.</span><span class="sxs-lookup"><span data-stu-id="f54fe-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="f54fe-111">Jos projektisopimuksessa on useita asiakkaita, asiakasta kohden voi olla yksi lasku ja useita laskuja projektisopimusta kohden.</span><span class="sxs-lookup"><span data-stu-id="f54fe-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="f54fe-112">Kaikki luodut projektilaskut ovat käytettävissä **Myynti**-alueen **laskutus**-osan **lasku**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f54fe-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="f54fe-113">Projektisopimuksen tiedot-sivu</span><span class="sxs-lookup"><span data-stu-id="f54fe-113">Project Contract details page</span></span>

<span data-ttu-id="f54fe-114">Proformalasku voidaan luoda myös **Projektisopimuksen** tiedot -sivulta.</span><span class="sxs-lookup"><span data-stu-id="f54fe-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="f54fe-115">Järjestelmä tarkistaa, mikä projektisopimuksista on **valmis laskutukseen**, joka on päivätty ennen kuluvan päivän päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="f54fe-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="f54fe-116">Näistä palvelusopimuksista järjestelmä luo proformalaskujen luonnokset kunkin sopimusrivin asiakkaiden määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="f54fe-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="f54fe-117">Kun luodaan yksittäinen proformalasku, näkyviin tulee **lasku**-sivu.</span><span class="sxs-lookup"><span data-stu-id="f54fe-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="f54fe-118">Jos projektisopimuksesta luodaan useita laskuja, kaikki luodut laskut näkyvät **Laskut**-luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="f54fe-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]