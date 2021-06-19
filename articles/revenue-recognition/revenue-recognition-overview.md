---
title: Tuoton kirjaamisen yleiskatsaus
description: Tässä aiheessa on tietoja tuoton kirjaamisesta Project Operationsissa.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013752"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="349e7-103">Tuoton kirjaamisen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="349e7-103">Revenue recognition overview</span></span>

<span data-ttu-id="349e7-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="349e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="349e7-105">Dynamics 365 Project Operationsissa tuoton kirjaamisperiaatteet vaihtelevat projektin tai projektin osan valitun laskutustavan mukaan.</span><span class="sxs-lookup"><span data-stu-id="349e7-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="349e7-106">Tässä aiheessa on tietoja tuoton kirjaamisesta Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="349e7-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="349e7-107">Tapahtumat, joista pidetään kirjaa aika ja materiaalit -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="349e7-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="349e7-108">Kustannusten ja tuottojen kirjaaminen liittyvät toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="349e7-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="349e7-109">Tapahtumakustannukset ja laskuttamattomat myynnit kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="349e7-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="349e7-110">Projektin kustannus- ja tuottoprofiili määrittää, kirjataanko laskuttamattomia myyntitapahtumia kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="349e7-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="349e7-111">Jos **Kerrytä tuottoa** on valittuna, järjestelmä käyttää **Käynnissä oleva arvo** - ja **Kerrytetty tuoton myyntiarvo** -tilejä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="349e7-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="349e7-112">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="349e7-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="349e7-113">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="349e7-113">Transaction type</span></span> | <span data-ttu-id="349e7-114">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="349e7-114">Debit/Credit</span></span> | <span data-ttu-id="349e7-115">Summa</span><span class="sxs-lookup"><span data-stu-id="349e7-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="349e7-116">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="349e7-116">WIP Sales value</span></span> | <span data-ttu-id="349e7-117">Debit</span><span class="sxs-lookup"><span data-stu-id="349e7-117">Debit</span></span> | <span data-ttu-id="349e7-118">100</span><span class="sxs-lookup"><span data-stu-id="349e7-118">100</span></span> |
  | <span data-ttu-id="349e7-119">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="349e7-119">Accrued revenue sales value</span></span> | <span data-ttu-id="349e7-120">Credit</span><span class="sxs-lookup"><span data-stu-id="349e7-120">Credit</span></span> | <span data-ttu-id="349e7-121">100</span><span class="sxs-lookup"><span data-stu-id="349e7-121">100</span></span> |

- <span data-ttu-id="349e7-122">Tuotto kirjataan laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="349e7-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="349e7-123">Järjestelmä käyttää **Laskutettu tuotto** -tiliä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="349e7-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="349e7-124">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="349e7-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="349e7-125">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="349e7-125">Transaction type</span></span> | <span data-ttu-id="349e7-126">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="349e7-126">Debit/Credit</span></span> | <span data-ttu-id="349e7-127">Summa</span><span class="sxs-lookup"><span data-stu-id="349e7-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="349e7-128">Asiakkaan saldo</span><span class="sxs-lookup"><span data-stu-id="349e7-128">Customer balance</span></span> | <span data-ttu-id="349e7-129">Debit</span><span class="sxs-lookup"><span data-stu-id="349e7-129">Debit</span></span> | <span data-ttu-id="349e7-130">120</span><span class="sxs-lookup"><span data-stu-id="349e7-130">120</span></span> |
  | <span data-ttu-id="349e7-131">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="349e7-131">Sales tax payable</span></span> | <span data-ttu-id="349e7-132">Credit</span><span class="sxs-lookup"><span data-stu-id="349e7-132">Credit</span></span> | <span data-ttu-id="349e7-133">20</span><span class="sxs-lookup"><span data-stu-id="349e7-133">20</span></span> |
  | <span data-ttu-id="349e7-134">Laskutettu tuotto</span><span class="sxs-lookup"><span data-stu-id="349e7-134">Invoiced Revenue</span></span> | <span data-ttu-id="349e7-135">Credit</span><span class="sxs-lookup"><span data-stu-id="349e7-135">Credit</span></span> | <span data-ttu-id="349e7-136">100</span><span class="sxs-lookup"><span data-stu-id="349e7-136">100</span></span> |

- <span data-ttu-id="349e7-137">Jos tuottoa kerrytettiin, kun ei-laskutettu myynti kirjataan, järjestelmä peruuttaa kerrytetyn tuoton laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="349e7-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="349e7-138">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="349e7-138">Transaction type</span></span> | <span data-ttu-id="349e7-139">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="349e7-139">Debit/Credit</span></span> | <span data-ttu-id="349e7-140">Summa</span><span class="sxs-lookup"><span data-stu-id="349e7-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="349e7-141">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="349e7-141">WIP Sales value</span></span> | <span data-ttu-id="349e7-142">Credit</span><span class="sxs-lookup"><span data-stu-id="349e7-142">Credit</span></span> | <span data-ttu-id="349e7-143">100</span><span class="sxs-lookup"><span data-stu-id="349e7-143">100</span></span> |
  | <span data-ttu-id="349e7-144">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="349e7-144">Accrued revenue sales value</span></span> | <span data-ttu-id="349e7-145">Debit</span><span class="sxs-lookup"><span data-stu-id="349e7-145">Debit</span></span> | <span data-ttu-id="349e7-146">100</span><span class="sxs-lookup"><span data-stu-id="349e7-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="349e7-147">Tapahtumat, joista pidetään kirjaa kiinteä hinta -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="349e7-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="349e7-148">Kustannusten ja tuottojen kirjaaminen ovat erillisiä.</span><span class="sxs-lookup"><span data-stu-id="349e7-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="349e7-149">Tapahtumakustannukset kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="349e7-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="349e7-150">Laskuttamattomia myyntitapahtumia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="349e7-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="349e7-151">Tuotto voidaan kirjata laskutuksen aikana, jos projektin kustannus- ja tuottoprofiilien **Projektin valmistumislaskelmiin käytetty periaate** on asetettu arvoksi **Ei käynnissä olevaa**.</span><span class="sxs-lookup"><span data-stu-id="349e7-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="349e7-152">Käytä tätä menetelmää vain lyhytaikaisia ja yksinkertaisia projekteja varten.</span><span class="sxs-lookup"><span data-stu-id="349e7-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="349e7-153">Tuotto voidaan kirjata käyttämällä kiinteähintaisia tuottoarvioita joko **Valmistunut sopimus** tai **Valmistumisprosenttiin perustuva tuoton kirjaaminen** -menetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="349e7-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="349e7-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="349e7-154">Additional resources</span></span>
[<span data-ttu-id="349e7-155">Laskutettavien projektien kirjanpidon määrittäminen -artikkeli</span><span class="sxs-lookup"><span data-stu-id="349e7-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="349e7-156">Kiinteähintaisen arvioidun myyntituoton projektit</span><span class="sxs-lookup"><span data-stu-id="349e7-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="349e7-157">Myyntituottoarvioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="349e7-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="349e7-158">Valmistumiskustannusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="349e7-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]