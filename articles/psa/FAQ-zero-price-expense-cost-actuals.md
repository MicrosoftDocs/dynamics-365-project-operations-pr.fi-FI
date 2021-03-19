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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285839"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="3007d-103">Miksi toteutuneen kulun kustannusten oletushinta on nolla?</span><span class="sxs-lookup"><span data-stu-id="3007d-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3007d-104">Nämä usein kysytyt kysymykset koskevat toteutuneita kuluja, joissa tapahtuman luokaksi on määritetty Kulu ja tapahtumatyypiksi Kustannus.</span><span class="sxs-lookup"><span data-stu-id="3007d-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="3007d-105">Toteutuneen kulun kustannuksen kustannushintojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="3007d-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="3007d-106">Siirry liittyvään kulumerkintään ja varmista, että kulumerkinnän kentässä on summa.</span><span class="sxs-lookup"><span data-stu-id="3007d-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="3007d-107">Jos alkuperäisen kulumerkinnän kenttään ei ole annettu summaa, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="3007d-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="3007d-108">Voit ratkaista tämän ongelman luomalla kulumerkinnän, jolla on sallittu summa, ja hyväksymällä sen.</span><span class="sxs-lookup"><span data-stu-id="3007d-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]