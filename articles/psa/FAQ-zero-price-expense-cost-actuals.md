---
title: Miksi toteutuneen kulun kustannusten oletushinta on nolla?
description: Tee vianmääritys ja selvitä, miksi toteutuneen kulun kustannuksen hinnan oletusarvo on 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146344"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="e4ab8-103">Miksi toteutuneen kulun kustannusten oletushinta on nolla?</span><span class="sxs-lookup"><span data-stu-id="e4ab8-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e4ab8-104">Nämä usein kysytyt kysymykset koskevat toteutuneita kuluja, joissa tapahtuman luokaksi on määritetty Kulu ja tapahtumatyypiksi Kustannus.</span><span class="sxs-lookup"><span data-stu-id="e4ab8-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="e4ab8-105">Toteutuneen kulun kustannuksen kustannushintojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e4ab8-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="e4ab8-106">Siirry liittyvään kulumerkintään ja varmista, että kulumerkinnän kentässä on summa.</span><span class="sxs-lookup"><span data-stu-id="e4ab8-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="e4ab8-107">Jos alkuperäisen kulumerkinnän kenttään ei ole annettu summaa, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="e4ab8-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="e4ab8-108">Voit ratkaista tämän ongelman luomalla kulumerkinnän, jolla on sallittu summa, ja hyväksymällä sen.</span><span class="sxs-lookup"><span data-stu-id="e4ab8-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
