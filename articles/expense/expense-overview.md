---
title: Kulujen yleiskatsaus
description: Tämä aihe tarjoaa tietoja Project Operationsin kulutoiminnoista.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276569"
---
# <a name="expense-home-page"></a><span data-ttu-id="12cd0-103">Kulujen aloitussivu</span><span class="sxs-lookup"><span data-stu-id="12cd0-103">Expense home page</span></span>

<span data-ttu-id="12cd0-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="12cd0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="12cd0-105">Dynamics 365 Project Operations tukee mahdollisuutta käsitellä kuluja.</span><span class="sxs-lookup"><span data-stu-id="12cd0-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="12cd0-106">Kulujen käsittely tapahtuu projekteissa tai ilman projekteja, käyttämällä mukautettavaa käytäntöjen, tapahtumaluokkien ja hyväksyntöjen työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="12cd0-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="12cd0-107">Project Operationsissa on kaksi tuettua kulujen käyttöönoton mallia:</span><span class="sxs-lookup"><span data-stu-id="12cd0-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="12cd0-108">**Täysi**: Täysi käyttöönotto on käytettävissä seuraaville: **Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa** tai **Project Operations tuotantotilaukseen perustuvissa skenaarioissa**.</span><span class="sxs-lookup"><span data-stu-id="12cd0-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="12cd0-109">**Perusratkaisu**: Peruskäyttöönotto on käytettävissä seuraaville: **Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa** ja **Lite-käyttöönotto – kauppa proformalaskutukseen**.</span><span class="sxs-lookup"><span data-stu-id="12cd0-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="12cd0-110">Täydellinen</span><span class="sxs-lookup"><span data-stu-id="12cd0-110">Full</span></span> 
<span data-ttu-id="12cd0-111">Täysi kulujen käyttöönotto tarjoaa täydellisen käytännön täytäntöönpanon, joka sisältää mahdollisuuden luoda käytäntöjä, kuten:</span><span class="sxs-lookup"><span data-stu-id="12cd0-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="12cd0-112">Kululuokkien rajat</span><span class="sxs-lookup"><span data-stu-id="12cd0-112">Expense category limits</span></span>
  - <span data-ttu-id="12cd0-113">Matka</span><span class="sxs-lookup"><span data-stu-id="12cd0-113">Travel</span></span>
  - <span data-ttu-id="12cd0-114">Päiväraha</span><span class="sxs-lookup"><span data-stu-id="12cd0-114">Per diem</span></span>
  - <span data-ttu-id="12cd0-115">Luottokorttituonnit</span><span class="sxs-lookup"><span data-stu-id="12cd0-115">Credit card imports</span></span>
  - <span data-ttu-id="12cd0-116">Kuitin optinen merkkien tunnistus</span><span class="sxs-lookup"><span data-stu-id="12cd0-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="12cd0-117">Perustiedot</span><span class="sxs-lookup"><span data-stu-id="12cd0-117">Basic</span></span> 
<span data-ttu-id="12cd0-118">Kulujen peruskäyttöönottoskenaario mahdollistaa vain peruskulujen tallennuksen projektiin.</span><span class="sxs-lookup"><span data-stu-id="12cd0-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="12cd0-119">Lisätietoja on kohdassa [Kulumerkintä (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="12cd0-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="12cd0-120">Kulujen käyttöönoton määritys</span><span class="sxs-lookup"><span data-stu-id="12cd0-120">Determine your Expense deployment</span></span>
<span data-ttu-id="12cd0-121">Jos haluat selvittää, onko käytössä kulujen hallinnan peruskäyttöönotto, tarkista, että URL-osoite päättyy **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="12cd0-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]