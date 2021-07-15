---
title: Yritysten välisen laskutuksen yleiskatsaus
description: Tässä aiheessa on tietoja ja esimerkkejä yritysten välisistä laskuista projekteissa.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369372"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="1a427-103">Yritysten välisen laskutuksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1a427-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="1a427-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="1a427-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1a427-105">Organisaatiolla voi olla useita osastoja, tytäryhtiöitä ja muita juridisia kohteita, jotka siirtävät tuotteita ja palveluja toisiinsa projekteissa.</span><span class="sxs-lookup"><span data-stu-id="1a427-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="1a427-106">Palvelua tai tuotetta tarjoava yritys on nimeltään *lainaa antava yritys*.</span><span class="sxs-lookup"><span data-stu-id="1a427-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="1a427-107">Palvelun tai tuotteen vastaanottava yritys on nimeltään *lainaa ottava yritys*.</span><span class="sxs-lookup"><span data-stu-id="1a427-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="1a427-108">Seuraavassa kuvassa on esitetty tyypillinen skenaario, jossa kaksi yritystä, Contoso Robotics USA (lainaa ottava yritys) ja Contoso Robotics UK (lainaa antava yritys) jakavat resursseja keskenään toimittaakseen projektin asiakkaalle, eli Adventure Worksille.</span><span class="sxs-lookup"><span data-stu-id="1a427-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="1a427-109">Tässä skenaariossa Contoso Robotics USA on palkattu toimittamaan työ Adventure Worksille.</span><span class="sxs-lookup"><span data-stu-id="1a427-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Konsernin sisäinen laskutus](./media/IntercompanyScenario.png) 

<span data-ttu-id="1a427-111">Dynamics 365 Project Operations käyttää seuraavaa työnkulkua yritysten välisten tapahtumien käsittelyyn:</span><span class="sxs-lookup"><span data-stu-id="1a427-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="1a427-112">Resurssit lainaa antavasta yrityksestä kirjaavat yritysten väliset aika- tai kulutapahtumat merkitsemällä aikaa tai kuluja lainaa ottavan yrityksen projekteihin.</span><span class="sxs-lookup"><span data-stu-id="1a427-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="1a427-113">Ajan ja kulujen kustannukset kirjataan lainaa antavaan yritykseen käyttämällä lainaa ottavan yrityksen yksikkökustannushinnastoa.</span><span class="sxs-lookup"><span data-stu-id="1a427-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="1a427-114">Yritysten väliset laskuttamattomat myyntitapahtumat kirjataan lainaa antavaan yritykseen käyttämällä lainaa ottavan yrityksen yksikkökustannushinnastoa.</span><span class="sxs-lookup"><span data-stu-id="1a427-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="1a427-115">Laskuttamaton tuotto kirjataan lainaa ottavaan yritykseen käyttäen projektisopimuksen myyntihinnastoa.</span><span class="sxs-lookup"><span data-stu-id="1a427-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="1a427-116">Asiakasta voidaan laskuttaa, kun laskuttamaton tuotto kirjataan.</span><span class="sxs-lookup"><span data-stu-id="1a427-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="1a427-117">Asiakkaan ei tarvitse odottaa, kunnes yritysten välisen laskun käsittely on valmis.</span><span class="sxs-lookup"><span data-stu-id="1a427-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="1a427-118">Yritysten väliset asiakaslaskut luodaan säännöllisin väliajoin lainaa antavassa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1a427-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="1a427-119">Laskut luodaan manuaalisesti tai käyttämällä kausittaista automatisoitua prosessia.</span><span class="sxs-lookup"><span data-stu-id="1a427-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="1a427-120">Kullekin lainaa ottavalle yritykselle voidaan luoda yksittäinen lasku, tai voidaan luoda erilliset, projektikohtaiset laskut.</span><span class="sxs-lookup"><span data-stu-id="1a427-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="1a427-121">Kun yritysten välinen asiakaslasku kirjataan lainaa antavassa yrityksessä, sitä vastaava, odottava toimittajan lasku luodaan lainaa ottavassa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1a427-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="1a427-122">Odottavan toimittajan laskun kustannukset tallennetaan projektin alikirjauksiin, kun lasku kirjataan.</span><span class="sxs-lookup"><span data-stu-id="1a427-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="1a427-123">Seuraavassa kaaviossa on kuvattu yritysten välinen laskutus siltä osin, kun se liittyy kirjanpitotapahtumiin ja odotettuihin yleisen tapahtumarekisterin kirjauksiin.</span><span class="sxs-lookup"><span data-stu-id="1a427-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Yritysten välinen työnkulku](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="1a427-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1a427-125">Additional resources</span></span>

- [<span data-ttu-id="1a427-126">Yritysten välisen laskutuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1a427-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="1a427-127">Yritysten välisten tapahtumien tallentaminen</span><span class="sxs-lookup"><span data-stu-id="1a427-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="1a427-128">Yritysten välisten asiakas- ja toimittajalaskujen luominen</span><span class="sxs-lookup"><span data-stu-id="1a427-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]