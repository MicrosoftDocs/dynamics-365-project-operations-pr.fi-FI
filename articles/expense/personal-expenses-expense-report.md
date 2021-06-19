---
title: Matkalaskun henkilökohtaisten kulujen käsittely
description: Tässä aiheessa on tietoja siitä, miten työntekijöiden työmatkoihin liittyvät henkilökohtaiset kulut voidaan käsitellä.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025680"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="f3ace-103">Matkalaskun henkilökohtaisten kulujen käsittely</span><span class="sxs-lookup"><span data-stu-id="f3ace-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="f3ace-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f3ace-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3ace-105">Työmatkalla työntekijä saattaa maksaa henkilökohtaisia kuluja yrityksen luottokortilla.</span><span class="sxs-lookup"><span data-stu-id="f3ace-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="f3ace-106">Jos henkilökohtaisten kulujen käsittelyä varten ei ole määritetty prosessia, kuluraportin hyväksyntäprosessi voi keskeytyä, kun työntekijä lähettää eritellyn kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="f3ace-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="f3ace-107">Työntekijän henkilökohtaiset kulut voidaan käsitellä kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="f3ace-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="f3ace-108">**Työntekijän maksama**: organisaatiosi ei maksa henkilökohtaisia kuluja, jotka näkyvät yrityksen luottokorttilaskussa.</span><span class="sxs-lookup"><span data-stu-id="f3ace-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="f3ace-109">Työntekijä maksaa kulut suoraan luottokortin toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="f3ace-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="f3ace-110">**Yrityksen maksama**: organisaatio maksaa yrityksen luottokorttilaskun kokonaan ja veloittaa sitten työntekijän tililtä henkilökohtaiset kulut.</span><span class="sxs-lookup"><span data-stu-id="f3ace-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="f3ace-111">Voit valita menetelmän, jota organisaatiosi käyttää **kulun hallinnan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f3ace-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="f3ace-112">Ota käyttöön kulujen jakotoiminto, kun henkilökohtaisen summan kentässä on arvo</span><span class="sxs-lookup"><span data-stu-id="f3ace-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="f3ace-113">**Ota käyttöön kulujen jakotoiminto, kun henkilökohtaisen summan kentässä on arvo** -ominaisuus koskee vain kuluraportteja, jotka on hyväksytty käyttämällä rivitason työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="f3ace-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="f3ace-114">Raportit hyväksytään kohdasta **Käsittele kuluraportit** > **Minulle liitetyt kuluraportit** > **Avaa kuluraportti**.</span><span class="sxs-lookup"><span data-stu-id="f3ace-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="f3ace-115">Jos haluat ottaa tämän ominaisuuden käyttöön, avaa **Työtilat** > **Ominaisuuksien hallinta**, valitse **Ota käyttöön kulujen jakotoiminto, kun henkilökohtaisen summan kentässä on arvo** ja valitse sitten **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="f3ace-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="f3ace-116">Kun ominaisuus on käytössä, tätä toimintoa käyttävät kulurivit luovat kaksi riviä, kun raportti lähetetään.</span><span class="sxs-lookup"><span data-stu-id="f3ace-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="f3ace-117">Nämä kaksi riviä luodaan, jotta hyväksyjä voit hyväksyä ne molemmat erikseen.</span><span class="sxs-lookup"><span data-stu-id="f3ace-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
