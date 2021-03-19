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
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278864"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="f05ba-103">Tuoton kirjaamisen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f05ba-103">Revenue recognition overview</span></span>

<span data-ttu-id="f05ba-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="f05ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f05ba-105">Dynamics 365 Project Operationsissa tuoton kirjaamisperiaatteet vaihtelevat projektin tai projektin osan valitun laskutustavan mukaan.</span><span class="sxs-lookup"><span data-stu-id="f05ba-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="f05ba-106">Tässä aiheessa on tietoja tuoton kirjaamisesta Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="f05ba-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="f05ba-107">Tapahtumat, joista pidetään kirjaa aika ja materiaalit -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="f05ba-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="f05ba-108">Kustannusten ja tuottojen kirjaaminen liittyvät toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="f05ba-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="f05ba-109">Tapahtumakustannukset ja laskuttamattomat myynnit kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="f05ba-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="f05ba-110">Projektin kustannus- ja tuottoprofiili määrittää, kirjataanko laskuttamattomia myyntitapahtumia kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="f05ba-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="f05ba-111">Jos **Kerrytä tuottoa** on valittuna, järjestelmä käyttää **Käynnissä oleva arvo** - ja **Kerrytetty tuoton myyntiarvo** -tilejä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="f05ba-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="f05ba-112">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="f05ba-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="f05ba-113">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="f05ba-113">Transaction type</span></span> | <span data-ttu-id="f05ba-114">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="f05ba-114">Debit/Credit</span></span> | <span data-ttu-id="f05ba-115">Summa</span><span class="sxs-lookup"><span data-stu-id="f05ba-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f05ba-116">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="f05ba-116">WIP Sales value</span></span> | <span data-ttu-id="f05ba-117">Debit</span><span class="sxs-lookup"><span data-stu-id="f05ba-117">Debit</span></span> | <span data-ttu-id="f05ba-118">100</span><span class="sxs-lookup"><span data-stu-id="f05ba-118">100</span></span> |
  | <span data-ttu-id="f05ba-119">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="f05ba-119">Accrued revenue sales value</span></span> | <span data-ttu-id="f05ba-120">Credit</span><span class="sxs-lookup"><span data-stu-id="f05ba-120">Credit</span></span> | <span data-ttu-id="f05ba-121">100</span><span class="sxs-lookup"><span data-stu-id="f05ba-121">100</span></span> |

- <span data-ttu-id="f05ba-122">Tuotto kirjataan laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="f05ba-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="f05ba-123">Järjestelmä käyttää **Laskutettu tuotto** -tiliä kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="f05ba-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="f05ba-124">Seuraava on esimerkki tästä menetelmästä.</span><span class="sxs-lookup"><span data-stu-id="f05ba-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="f05ba-125">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="f05ba-125">Transaction type</span></span> | <span data-ttu-id="f05ba-126">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="f05ba-126">Debit/Credit</span></span> | <span data-ttu-id="f05ba-127">Summa</span><span class="sxs-lookup"><span data-stu-id="f05ba-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f05ba-128">Asiakkaan saldo</span><span class="sxs-lookup"><span data-stu-id="f05ba-128">Customer balance</span></span> | <span data-ttu-id="f05ba-129">Debit</span><span class="sxs-lookup"><span data-stu-id="f05ba-129">Debit</span></span> | <span data-ttu-id="f05ba-130">120</span><span class="sxs-lookup"><span data-stu-id="f05ba-130">120</span></span> |
  | <span data-ttu-id="f05ba-131">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="f05ba-131">Sales tax payable</span></span> | <span data-ttu-id="f05ba-132">Credit</span><span class="sxs-lookup"><span data-stu-id="f05ba-132">Credit</span></span> | <span data-ttu-id="f05ba-133">20</span><span class="sxs-lookup"><span data-stu-id="f05ba-133">20</span></span> |
  | <span data-ttu-id="f05ba-134">Laskutettu tuotto</span><span class="sxs-lookup"><span data-stu-id="f05ba-134">Invoiced Revenue</span></span> | <span data-ttu-id="f05ba-135">Credit</span><span class="sxs-lookup"><span data-stu-id="f05ba-135">Credit</span></span> | <span data-ttu-id="f05ba-136">100</span><span class="sxs-lookup"><span data-stu-id="f05ba-136">100</span></span> |

- <span data-ttu-id="f05ba-137">Jos tuottoa kerrytettiin, kun ei-laskutettu myynti kirjataan, järjestelmä peruuttaa kerrytetyn tuoton laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="f05ba-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="f05ba-138">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="f05ba-138">Transaction type</span></span> | <span data-ttu-id="f05ba-139">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="f05ba-139">Debit/Credit</span></span> | <span data-ttu-id="f05ba-140">Summa</span><span class="sxs-lookup"><span data-stu-id="f05ba-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f05ba-141">Käynnissä oleva myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="f05ba-141">WIP Sales value</span></span> | <span data-ttu-id="f05ba-142">Credit</span><span class="sxs-lookup"><span data-stu-id="f05ba-142">Credit</span></span> | <span data-ttu-id="f05ba-143">100</span><span class="sxs-lookup"><span data-stu-id="f05ba-143">100</span></span> |
  | <span data-ttu-id="f05ba-144">Kerrytetyn tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="f05ba-144">Accrued revenue sales value</span></span> | <span data-ttu-id="f05ba-145">Debit</span><span class="sxs-lookup"><span data-stu-id="f05ba-145">Debit</span></span> | <span data-ttu-id="f05ba-146">100</span><span class="sxs-lookup"><span data-stu-id="f05ba-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="f05ba-147">Tapahtumat, joista pidetään kirjaa kiinteä hinta -laskutustapaa käyttäen</span><span class="sxs-lookup"><span data-stu-id="f05ba-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="f05ba-148">Kustannusten ja tuottojen kirjaaminen ovat erillisiä.</span><span class="sxs-lookup"><span data-stu-id="f05ba-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="f05ba-149">Tapahtumakustannukset kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="f05ba-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="f05ba-150">Laskuttamattomia myyntitapahtumia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="f05ba-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="f05ba-151">Tuotto voidaan kirjata laskutuksen aikana, jos projektin kustannus- ja tuottoprofiilien **Projektin valmistumislaskelmiin käytetty periaate** on asetettu arvoksi **Ei käynnissä olevaa**.</span><span class="sxs-lookup"><span data-stu-id="f05ba-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="f05ba-152">Käytä tätä menetelmää vain lyhytaikaisia ja yksinkertaisia projekteja varten.</span><span class="sxs-lookup"><span data-stu-id="f05ba-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="f05ba-153">Tuotto voidaan kirjata käyttämällä kiinteähintaisia tuottoarvioita joko **Valmistunut sopimus** tai **Valmistumisprosenttiin perustuva tuoton kirjaaminen** -menetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="f05ba-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f05ba-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f05ba-154">Additional resources</span></span>
[<span data-ttu-id="f05ba-155">Laskutettavien projektien kirjanpidon määrittäminen -artikkeli</span><span class="sxs-lookup"><span data-stu-id="f05ba-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="f05ba-156">Kiinteähintaisen arvioidun myyntituoton projektit</span><span class="sxs-lookup"><span data-stu-id="f05ba-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="f05ba-157">Myyntituottoarvioiden hallinta</span><span class="sxs-lookup"><span data-stu-id="f05ba-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="f05ba-158">Valmistumiskustannusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="f05ba-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]