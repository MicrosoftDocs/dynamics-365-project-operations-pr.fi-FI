---
title: Kulujen yleiskatsaus
description: Tämä aihe tarjoaa tietoja Project Operationsin kulutoiminnoista.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075228"
---
# <a name="expense-home-page"></a><span data-ttu-id="5c7f6-103">Kulujen aloitussivu</span><span class="sxs-lookup"><span data-stu-id="5c7f6-103">Expense home page</span></span>

<span data-ttu-id="5c7f6-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="5c7f6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5c7f6-105">Dynamics 365 Project Operations tukee mahdollisuutta käsitellä kuluja.</span><span class="sxs-lookup"><span data-stu-id="5c7f6-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="5c7f6-106">Kulujen käsittely tapahtuu projekteissa tai ilman projekteja, käyttämällä mukautettavaa käytäntöjen, tapahtumaluokkien ja hyväksyntöjen työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="5c7f6-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="5c7f6-107">Project Operationsissa on kaksi tuettua kulujen käyttöönoton mallia:</span><span class="sxs-lookup"><span data-stu-id="5c7f6-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="5c7f6-108">**Täysi** : Täysi käyttöönotto on käytettävissä seuraaville: **Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa** tai **Project Operations tuotantotilaukseen perustuvissa skenaarioissa**.</span><span class="sxs-lookup"><span data-stu-id="5c7f6-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="5c7f6-109">**Perusratkaisu** : Peruskäyttöönotto on käytettävissä seuraaville: **Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa** ja **Lite-käyttöönotto – kauppa proformalaskutukseen**.</span><span class="sxs-lookup"><span data-stu-id="5c7f6-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="5c7f6-110">Täydellinen</span><span class="sxs-lookup"><span data-stu-id="5c7f6-110">Full</span></span> 
<span data-ttu-id="5c7f6-111">Täysi kulujen käyttöönotto tarjoaa täydellisen käytännön pakottamisen, joka sisältää mahdollisuuden luoda käytäntöjä, kuten:</span><span class="sxs-lookup"><span data-stu-id="5c7f6-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="5c7f6-112">Kululuokkien rajat</span><span class="sxs-lookup"><span data-stu-id="5c7f6-112">Expense category limits</span></span>
  - <span data-ttu-id="5c7f6-113">Matka</span><span class="sxs-lookup"><span data-stu-id="5c7f6-113">Travel</span></span>
  - <span data-ttu-id="5c7f6-114">Päiväraha</span><span class="sxs-lookup"><span data-stu-id="5c7f6-114">Per diem</span></span>
  - <span data-ttu-id="5c7f6-115">Luottokorttituonnit</span><span class="sxs-lookup"><span data-stu-id="5c7f6-115">Credit card imports</span></span>
  - <span data-ttu-id="5c7f6-116">Kuitin optinen merkkien tunnistus</span><span class="sxs-lookup"><span data-stu-id="5c7f6-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="5c7f6-117">Perustiedot</span><span class="sxs-lookup"><span data-stu-id="5c7f6-117">Basic</span></span> 
<span data-ttu-id="5c7f6-118">Kulujen peruskäyttöönottoskenaario mahdollistaa vain peruskulujen tallennuksen projektiin.</span><span class="sxs-lookup"><span data-stu-id="5c7f6-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="5c7f6-119">Lisätietoja on kohdassa [Kulumerkintä (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="5c7f6-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="5c7f6-120">Kulujen käyttöönoton määritys</span><span class="sxs-lookup"><span data-stu-id="5c7f6-120">Determine your Expense deployment</span></span>
<span data-ttu-id="5c7f6-121">Jos haluat selvittää, onko käytössä kulujen hallinnan peruskäyttöönotto, tarkista, että URL-osoite päättyy **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="5c7f6-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
