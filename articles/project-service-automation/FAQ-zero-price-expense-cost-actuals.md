---
title: Miksi toteutuneen kulun kustannusten oletushinta on nolla?
description: Tee vianmääritys ja selvitä, miksi toteutuneen kulun kustannuksen hinnan oletusarvo on 0.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751167"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="940e7-103">Miksi toteutuneen kulun kustannusten oletushinta on nolla?</span><span class="sxs-lookup"><span data-stu-id="940e7-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="940e7-104">Nämä usein kysytyt kysymykset koskevat toteutuneita kuluja, joissa tapahtuman luokaksi on määritetty Kulu ja tapahtumatyypiksi Kustannus.</span><span class="sxs-lookup"><span data-stu-id="940e7-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="940e7-105">Toteutuneen kulun kustannuksen kustannushintojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="940e7-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="940e7-106">Siirry liittyvään kulumerkintään ja varmista, että kulumerkinnän kentässä on summa.</span><span class="sxs-lookup"><span data-stu-id="940e7-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="940e7-107">Jos alkuperäisen kulumerkinnän kenttään ei ole annettu summaa, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="940e7-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="940e7-108">Voit ratkaista tämän ongelman luomalla kulumerkinnän, jolla on sallittu summa, ja hyväksymällä sen.</span><span class="sxs-lookup"><span data-stu-id="940e7-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
