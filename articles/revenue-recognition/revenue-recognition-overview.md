---
title: Tuoton kirjaamisen yleiskatsaus
description: Tässä aiheessa on tietoja tuoton kirjaamisesta Project Operationsissa.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368022"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="80ba4-103">Tuoton kirjaamisen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="80ba4-103">Revenue recognition overview</span></span>

<span data-ttu-id="80ba4-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="80ba4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="80ba4-105">Dynamics 365 Project Operationsissa tuoton kirjaamisperiaatteet vaihtelevat projektin tai projektin osan valitun laskutustavan mukaan.</span><span class="sxs-lookup"><span data-stu-id="80ba4-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="80ba4-106">Tässä aiheessa on tietoja tuoton kirjaamisesta Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="80ba4-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="80ba4-107">Tapahtumat, joista pidetään kirjaa aika ja materiaalit -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="80ba4-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="80ba4-108">Kustannusten ja tuottojen kirjaaminen liittyvät toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="80ba4-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="80ba4-109">Tapahtumakustannukset ja laskuttamattomat myynnit kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="80ba4-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="80ba4-110">Projektin kustannus- ja tuottoprofiili määrittää, kirjataanko laskuttamattomia myyntitapahtumia kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="80ba4-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="80ba4-111">Jos **Kerrytä tuottoa** on valittuna, järjestelmä käyttää **Käynnissä oleva arvo** - ja **Kerrytetty tuoton myyntiarvo** -tilejä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="80ba4-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="80ba4-112">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="80ba4-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="80ba4-113">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="80ba4-113">Transaction type</span></span> | <span data-ttu-id="80ba4-114">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="80ba4-114">Debit/Credit</span></span> | <span data-ttu-id="80ba4-115">Summa</span><span class="sxs-lookup"><span data-stu-id="80ba4-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="80ba4-116">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="80ba4-116">WIP Sales value</span></span> | <span data-ttu-id="80ba4-117">Debit</span><span class="sxs-lookup"><span data-stu-id="80ba4-117">Debit</span></span> | <span data-ttu-id="80ba4-118">100</span><span class="sxs-lookup"><span data-stu-id="80ba4-118">100</span></span> |
  | <span data-ttu-id="80ba4-119">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="80ba4-119">Accrued revenue sales value</span></span> | <span data-ttu-id="80ba4-120">Credit</span><span class="sxs-lookup"><span data-stu-id="80ba4-120">Credit</span></span> | <span data-ttu-id="80ba4-121">100</span><span class="sxs-lookup"><span data-stu-id="80ba4-121">100</span></span> |

- <span data-ttu-id="80ba4-122">Tuotto kirjataan laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="80ba4-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="80ba4-123">Järjestelmä käyttää **Laskutettu tuotto** -tiliä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="80ba4-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="80ba4-124">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="80ba4-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="80ba4-125">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="80ba4-125">Transaction type</span></span> | <span data-ttu-id="80ba4-126">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="80ba4-126">Debit/Credit</span></span> | <span data-ttu-id="80ba4-127">Summa</span><span class="sxs-lookup"><span data-stu-id="80ba4-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="80ba4-128">Asiakkaan saldo</span><span class="sxs-lookup"><span data-stu-id="80ba4-128">Customer balance</span></span> | <span data-ttu-id="80ba4-129">Debit</span><span class="sxs-lookup"><span data-stu-id="80ba4-129">Debit</span></span> | <span data-ttu-id="80ba4-130">120</span><span class="sxs-lookup"><span data-stu-id="80ba4-130">120</span></span> |
  | <span data-ttu-id="80ba4-131">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="80ba4-131">Sales tax payable</span></span> | <span data-ttu-id="80ba4-132">Credit</span><span class="sxs-lookup"><span data-stu-id="80ba4-132">Credit</span></span> | <span data-ttu-id="80ba4-133">20</span><span class="sxs-lookup"><span data-stu-id="80ba4-133">20</span></span> |
  | <span data-ttu-id="80ba4-134">Laskutettu tuotto</span><span class="sxs-lookup"><span data-stu-id="80ba4-134">Invoiced Revenue</span></span> | <span data-ttu-id="80ba4-135">Credit</span><span class="sxs-lookup"><span data-stu-id="80ba4-135">Credit</span></span> | <span data-ttu-id="80ba4-136">100</span><span class="sxs-lookup"><span data-stu-id="80ba4-136">100</span></span> |

- <span data-ttu-id="80ba4-137">Jos tuottoa kerrytettiin, kun ei-laskutettu myynti kirjataan, järjestelmä peruuttaa kerrytetyn tuoton laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="80ba4-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="80ba4-138">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="80ba4-138">Transaction type</span></span> | <span data-ttu-id="80ba4-139">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="80ba4-139">Debit/Credit</span></span> | <span data-ttu-id="80ba4-140">Summa</span><span class="sxs-lookup"><span data-stu-id="80ba4-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="80ba4-141">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="80ba4-141">WIP Sales value</span></span> | <span data-ttu-id="80ba4-142">Credit</span><span class="sxs-lookup"><span data-stu-id="80ba4-142">Credit</span></span> | <span data-ttu-id="80ba4-143">100</span><span class="sxs-lookup"><span data-stu-id="80ba4-143">100</span></span> |
  | <span data-ttu-id="80ba4-144">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="80ba4-144">Accrued revenue sales value</span></span> | <span data-ttu-id="80ba4-145">Debit</span><span class="sxs-lookup"><span data-stu-id="80ba4-145">Debit</span></span> | <span data-ttu-id="80ba4-146">100</span><span class="sxs-lookup"><span data-stu-id="80ba4-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="80ba4-147">Tapahtumat, joista pidetään kirjaa kiinteä hinta -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="80ba4-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="80ba4-148">Kustannusten ja tuottojen kirjaaminen ovat erillisiä.</span><span class="sxs-lookup"><span data-stu-id="80ba4-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="80ba4-149">Tapahtumakustannukset kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="80ba4-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="80ba4-150">Laskuttamattomia myyntitapahtumia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="80ba4-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="80ba4-151">Tuotto voidaan kirjata laskutuksen aikana, jos projektin kustannus- ja tuottoprofiilien **Projektin valmistumislaskelmiin käytetty periaate** on asetettu arvoksi **Ei käynnissä olevaa**.</span><span class="sxs-lookup"><span data-stu-id="80ba4-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="80ba4-152">Käytä tätä menetelmää vain lyhytaikaisia ja yksinkertaisia projekteja varten.</span><span class="sxs-lookup"><span data-stu-id="80ba4-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="80ba4-153">Tuotto voidaan kirjata käyttämällä kiinteähintaisia tuottoarvioita joko **Valmistunut sopimus** tai **Valmistumisprosenttiin perustuva tuoton kirjaaminen** -menetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="80ba4-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80ba4-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="80ba4-154">Additional resources</span></span>
[<span data-ttu-id="80ba4-155">Laskutettavien projektien kirjanpidon määrittäminen -artikkeli</span><span class="sxs-lookup"><span data-stu-id="80ba4-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="80ba4-156">Kiinteähintaisen arvioidun myyntituoton projektit</span><span class="sxs-lookup"><span data-stu-id="80ba4-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="80ba4-157">Myyntituottoarvioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="80ba4-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="80ba4-158">Valmistumiskustannusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="80ba4-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]