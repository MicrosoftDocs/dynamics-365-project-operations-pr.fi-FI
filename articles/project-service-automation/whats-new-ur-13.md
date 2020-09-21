---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 13, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 13, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751174"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="d207d-103">Project Service Automation V3, päivitysjulkaisu 13</span><span class="sxs-lookup"><span data-stu-id="d207d-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="d207d-104">Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen.</span><span class="sxs-lookup"><span data-stu-id="d207d-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d207d-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="d207d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d207d-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="d207d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d207d-107">Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle.</span><span class="sxs-lookup"><span data-stu-id="d207d-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d207d-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d207d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d207d-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 13.</span><span class="sxs-lookup"><span data-stu-id="d207d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="d207d-110">Tällä versiolla on koontinumero V3.10.3.18 ja se on saatavilla seuraavan aikataulun mukaan:</span><span class="sxs-lookup"><span data-stu-id="d207d-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="d207d-111">**Yleinen saatavuus (itsepäivitys):** marraskuu 2019</span><span class="sxs-lookup"><span data-stu-id="d207d-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="d207d-112">**Automaattinen päivitys:** joulukuu 2019</span><span class="sxs-lookup"><span data-stu-id="d207d-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="d207d-113">Päivitysjulkaisu 13</span><span class="sxs-lookup"><span data-stu-id="d207d-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="d207d-114">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="d207d-114">Bug fixes</span></span>

- <span data-ttu-id="d207d-115">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="d207d-115">Time and Expense</span></span>

     - <span data-ttu-id="d207d-116">Korjattu: **Kulun hyväksyntä** -sivun hakutoiminto ei toimi, kun haetaan kulun tarkoituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d207d-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="d207d-117">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="d207d-117">Resource Management</span></span>

     - <span data-ttu-id="d207d-118">Korjattu: Täsmäytyksessä numerot on päivitetty oikealle tasatuiksi.</span><span class="sxs-lookup"><span data-stu-id="d207d-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="d207d-119">Korjattu: Nimettyjä resursseja ei voi delegoida tehtäviin **Ajoitus**-välilehden kautta.</span><span class="sxs-lookup"><span data-stu-id="d207d-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="d207d-120">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="d207d-120">Project Management</span></span>

     - <span data-ttu-id="d207d-121">Korjattu: Poikkeus null-viittauksesta, kun määritetään ryhmän jäsentä, kun **TransactionType** puuttuu **Unit**- ja **DefaultGroup**-tiedoista.</span><span class="sxs-lookup"><span data-stu-id="d207d-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="d207d-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d207d-122">Sales</span></span>

     - <span data-ttu-id="d207d-123">Korjattu: päällekkäiset tapahtumatyyppitietueet palauttavat virheen, kun roolien hintatietueita luodaan.</span><span class="sxs-lookup"><span data-stu-id="d207d-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="d207d-124">Korjattu: Yilmääräiset **Uusi mahdollisuus**-, **Tarjous**-, **Tilausrivi**- ja **Lisää tuote** -painikkeet näkyvät Mahdollisuudet-, Tarjoukset- ja Tilaa tuotteita -kohtien komennoissa sekä projektipohjaisten rivien aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="d207d-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


