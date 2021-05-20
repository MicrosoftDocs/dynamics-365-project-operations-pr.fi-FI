---
title: Ei-varastoivien materiaalien ostaminen käyttämällä odottavaa toimittajan laskua
description: Tässä aihe, miten odottavat toimittajan laskut tallennetaan.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880638"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="4dce3-103">Ei-varastoivien materiaalien ostaminen käyttämällä odottavaa toimittajan laskua</span><span class="sxs-lookup"><span data-stu-id="4dce3-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="4dce3-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="4dce3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4dce3-105">Kun yritys hankkii ei-varastoitavaa materiaalia projektia varten, kustannukset voidaan kirjata projektiin heti.</span><span class="sxs-lookup"><span data-stu-id="4dce3-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="4dce3-106">Esimerkiksi Contoso Robotics US on suorittamassa laitteiden uusimisprojektia, ja se tarvitsee ohjelmiston käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="4dce3-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="4dce3-107">Nämä käyttöoikeudet hankitaan ulkopuoliselta toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="4dce3-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="4dce3-108">Dynamics 365 Financen avulla ostoreskontra kirjaa odottavan toimittajan laskuasiakirjan ja määrittää käyttöoikeuskustannukset suoraan välineiden uusimisprojektiin.</span><span class="sxs-lookup"><span data-stu-id="4dce3-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4dce3-109">Ennen kuin käytät tässä aiheessa kuvattuja toimintoja, tarkista ja ota käyttöön tarvittavat määritykset.</span><span class="sxs-lookup"><span data-stu-id="4dce3-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="4dce3-110">Lisätietoja on ohjeaiheessa [Ei-varastoivien materiaalien ja odottavien toimittajan laskujen ottaminen käyttöön](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="4dce3-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="4dce3-111">Projektiin liittyvän odottavan toimittajan laskun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="4dce3-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="4dce3-112">Odottavat toimittajan laskut voidaan tallentaa **Odottavat toimittajan laskut** -sivulle (**Ostoreskontra** > **laskut** > **odottavat toimittajan laskut**).</span><span class="sxs-lookup"><span data-stu-id="4dce3-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="4dce3-113">Kirjaa projektiin liittyvä odottava toimittajan lasku seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="4dce3-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="4dce3-114">Siirry kohtaan **Ostoreskontra** > **laskut** ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4dce3-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="4dce3-115">Valitse **Laskutili**-kentässä toimittaja ja kirjoita **Numero**-kenttään toimittajan laskun tunnus.</span><span class="sxs-lookup"><span data-stu-id="4dce3-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="4dce3-116">Lisää rivi toimittajan laskuun ja valitse **Nimikenumero**-kentässä toimittajalta ostettu ei-varastoitu nimike.</span><span class="sxs-lookup"><span data-stu-id="4dce3-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4dce3-117">Projektiin ei voi kirjata toimittajan laskun rivejä, jotka perustuvat hankintaluokkaan.</span><span class="sxs-lookup"><span data-stu-id="4dce3-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="4dce3-118">Lisää ostettu määrä.</span><span class="sxs-lookup"><span data-stu-id="4dce3-118">Add the quantity purchased.</span></span> <span data-ttu-id="4dce3-119">Järjestelmä täyttää yksikköhinnan ei-varastoidun yksikköhinnan määrityksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4dce3-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="4dce3-120">Tarkista kokonaissumma ja muut rivin pakolliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="4dce3-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="4dce3-121">Valitse rivin tiedoista **Projekti**-välilehdestä sen projektin tunnus, jonne tämä kohde tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="4dce3-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="4dce3-122">Voit myös valita aktiviteetin numeron ja päivittää projektin luokan ja rivin ominaisuuden.</span><span class="sxs-lookup"><span data-stu-id="4dce3-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="4dce3-123">Kirjaa odottava toimittajan lasku.</span><span class="sxs-lookup"><span data-stu-id="4dce3-123">Post pending vendor invoice.</span></span> <span data-ttu-id="4dce3-124">Kun lasku kirjataan, järjestelmä kirjaa seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="4dce3-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="4dce3-125">Toimittajan saldon summa.</span><span class="sxs-lookup"><span data-stu-id="4dce3-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="4dce3-126">Arvonlisäveron summa.</span><span class="sxs-lookup"><span data-stu-id="4dce3-126">The sales tax amount.</span></span>
    - <span data-ttu-id="4dce3-127">Projektiin kohdistuvat kustannukset kirjataan integrointia varten integrointitilille.</span><span class="sxs-lookup"><span data-stu-id="4dce3-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="4dce3-128">Projektin todellinen tapahtuma kohteessa Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4dce3-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="4dce3-129">Tätä tapahtumaa käsitellään lisää [Project Operations Integration -kirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="4dce3-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="4dce3-130">Tämän kirjauksen kirjaaminen siirtää summan integroinnin lisäkulutililtä projektikustannustilille.</span><span class="sxs-lookup"><span data-stu-id="4dce3-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
