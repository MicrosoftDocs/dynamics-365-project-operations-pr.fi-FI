---
title: Tuoton kirjaamisen yleiskatsaus
description: Tässä aiheessa on tietoja tuoton kirjaamisesta Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531410"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="a78ac-103">Tuoton kirjaamisen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a78ac-103">Revenue recognition overview</span></span>

<span data-ttu-id="a78ac-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="a78ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a78ac-105">Dynamics 365 Project Operationsissa tuoton kirjaamisperiaatteet vaihtelevat projektin tai projektin osan valitun laskutustavan mukaan.</span><span class="sxs-lookup"><span data-stu-id="a78ac-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="a78ac-106">Tässä aiheessa on tietoja tuoton kirjaamisesta Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="a78ac-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="a78ac-107">Tapahtumat, joista pidetään kirjaa aika ja materiaalit -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="a78ac-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="a78ac-108">Kustannusten ja tuottojen kirjaaminen liittyvät toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="a78ac-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="a78ac-109">Tapahtumakustannukset ja laskuttamattomat myynnit kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="a78ac-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="a78ac-110">Projektin kustannus- ja tuottoprofiili määrittää, kirjataanko laskuttamattomia myyntitapahtumia kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="a78ac-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="a78ac-111">Jos **Kerrytä tuottoa** on valittuna, järjestelmä käyttää **Käynnissä oleva arvo** - ja **Kerrytetty tuoton myyntiarvo** -tilejä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a78ac-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="a78ac-112">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="a78ac-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="a78ac-113">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="a78ac-113">Transaction type</span></span> | <span data-ttu-id="a78ac-114">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="a78ac-114">Debit/Credit</span></span> | <span data-ttu-id="a78ac-115">Summa</span><span class="sxs-lookup"><span data-stu-id="a78ac-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="a78ac-116">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="a78ac-116">WIP Sales value</span></span> | <span data-ttu-id="a78ac-117">Debit</span><span class="sxs-lookup"><span data-stu-id="a78ac-117">Debit</span></span> | <span data-ttu-id="a78ac-118">100</span><span class="sxs-lookup"><span data-stu-id="a78ac-118">100</span></span> |
  | <span data-ttu-id="a78ac-119">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="a78ac-119">Accrued revenue sales value</span></span> | <span data-ttu-id="a78ac-120">Credit</span><span class="sxs-lookup"><span data-stu-id="a78ac-120">Credit</span></span> | <span data-ttu-id="a78ac-121">100</span><span class="sxs-lookup"><span data-stu-id="a78ac-121">100</span></span> |

- <span data-ttu-id="a78ac-122">Tuotto kirjataan laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a78ac-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="a78ac-123">Järjestelmä käyttää **Laskutettu tuotto** -tiliä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a78ac-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="a78ac-124">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="a78ac-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="a78ac-125">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="a78ac-125">Transaction type</span></span> | <span data-ttu-id="a78ac-126">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="a78ac-126">Debit/Credit</span></span> | <span data-ttu-id="a78ac-127">Summa</span><span class="sxs-lookup"><span data-stu-id="a78ac-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="a78ac-128">Asiakkaan saldo</span><span class="sxs-lookup"><span data-stu-id="a78ac-128">Customer balance</span></span> | <span data-ttu-id="a78ac-129">Debit</span><span class="sxs-lookup"><span data-stu-id="a78ac-129">Debit</span></span> | <span data-ttu-id="a78ac-130">120</span><span class="sxs-lookup"><span data-stu-id="a78ac-130">120</span></span> |
  | <span data-ttu-id="a78ac-131">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a78ac-131">Sales tax payable</span></span> | <span data-ttu-id="a78ac-132">Credit</span><span class="sxs-lookup"><span data-stu-id="a78ac-132">Credit</span></span> | <span data-ttu-id="a78ac-133">20</span><span class="sxs-lookup"><span data-stu-id="a78ac-133">20</span></span> |
  | <span data-ttu-id="a78ac-134">Laskutettu tuotto</span><span class="sxs-lookup"><span data-stu-id="a78ac-134">Invoiced Revenue</span></span> | <span data-ttu-id="a78ac-135">Credit</span><span class="sxs-lookup"><span data-stu-id="a78ac-135">Credit</span></span> | <span data-ttu-id="a78ac-136">100</span><span class="sxs-lookup"><span data-stu-id="a78ac-136">100</span></span> |

- <span data-ttu-id="a78ac-137">Jos tuottoa kerrytettiin, kun ei-laskutettu myynti kirjataan, järjestelmä peruuttaa kerrytetyn tuoton laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a78ac-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="a78ac-138">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="a78ac-138">Transaction type</span></span> | <span data-ttu-id="a78ac-139">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="a78ac-139">Debit/Credit</span></span> | <span data-ttu-id="a78ac-140">Summa</span><span class="sxs-lookup"><span data-stu-id="a78ac-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="a78ac-141">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="a78ac-141">WIP Sales value</span></span> | <span data-ttu-id="a78ac-142">Credit</span><span class="sxs-lookup"><span data-stu-id="a78ac-142">Credit</span></span> | <span data-ttu-id="a78ac-143">100</span><span class="sxs-lookup"><span data-stu-id="a78ac-143">100</span></span> |
  | <span data-ttu-id="a78ac-144">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="a78ac-144">Accrued revenue sales value</span></span> | <span data-ttu-id="a78ac-145">Debit</span><span class="sxs-lookup"><span data-stu-id="a78ac-145">Debit</span></span> | <span data-ttu-id="a78ac-146">100</span><span class="sxs-lookup"><span data-stu-id="a78ac-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="a78ac-147">Tapahtumat, joista pidetään kirjaa kiinteä hinta -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="a78ac-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="a78ac-148">Kustannusten ja tuottojen kirjaaminen ovat erillisiä.</span><span class="sxs-lookup"><span data-stu-id="a78ac-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="a78ac-149">Tapahtumakustannukset kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="a78ac-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="a78ac-150">Laskuttamattomia myyntitapahtumia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="a78ac-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="a78ac-151">Tuotto voidaan kirjata laskutuksen aikana, jos projektin kustannus- ja tuottoprofiilien **Projektin valmistumislaskelmiin käytetty periaate** on asetettu arvoksi **Ei käynnissä olevaa**.</span><span class="sxs-lookup"><span data-stu-id="a78ac-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="a78ac-152">Käytä tätä menetelmää vain lyhytaikaisia ja yksinkertaisia projekteja varten.</span><span class="sxs-lookup"><span data-stu-id="a78ac-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="a78ac-153">Tuotto voidaan kirjata käyttämällä kiinteähintaisia tuottoarvioita joko **Valmistunut sopimus** tai **Valmistumisprosenttiin perustuva tuoton kirjaaminen** -menetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="a78ac-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a78ac-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a78ac-154">Additional resources</span></span>
[<span data-ttu-id="a78ac-155">Laskutettavien projektien kirjanpidon määrittäminen -artikkeli</span><span class="sxs-lookup"><span data-stu-id="a78ac-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="a78ac-156">Kiinteähintaisen arvioidun myyntituoton projektit</span><span class="sxs-lookup"><span data-stu-id="a78ac-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="a78ac-157">Myyntituottoarvioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="a78ac-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="a78ac-158">Valmistumiskustannusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="a78ac-158">Cost to complete methods</span></span>](cost-complete-methods.md)
