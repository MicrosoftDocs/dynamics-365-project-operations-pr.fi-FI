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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122114"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="63918-103">Miksi toteutuneen kulun kustannusten oletushinta on nolla?</span><span class="sxs-lookup"><span data-stu-id="63918-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="63918-104">Nämä usein kysytyt kysymykset koskevat toteutuneita kuluja, joissa tapahtuman luokaksi on määritetty Kulu ja tapahtumatyypiksi Kustannus.</span><span class="sxs-lookup"><span data-stu-id="63918-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="63918-105">Toteutuneen kulun kustannuksen kustannushintojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="63918-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="63918-106">Siirry liittyvään kulumerkintään ja varmista, että kulumerkinnän kentässä on summa.</span><span class="sxs-lookup"><span data-stu-id="63918-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="63918-107">Jos alkuperäisen kulumerkinnän kenttään ei ole annettu summaa, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="63918-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="63918-108">Voit ratkaista tämän ongelman luomalla kulumerkinnän, jolla on sallittu summa, ja hyväksymällä sen.</span><span class="sxs-lookup"><span data-stu-id="63918-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
