---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 13, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 13, V3:n uusista ominaisuuksista.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c328821064065e19938406856d327f690f577e7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000297"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="8789a-103">Project Service Automation -päivitysjulkaisu 13, V3</span><span class="sxs-lookup"><span data-stu-id="8789a-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8789a-104">Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen.</span><span class="sxs-lookup"><span data-stu-id="8789a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="8789a-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="8789a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8789a-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="8789a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8789a-107">Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle.</span><span class="sxs-lookup"><span data-stu-id="8789a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="8789a-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8789a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8789a-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 13.</span><span class="sxs-lookup"><span data-stu-id="8789a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="8789a-110">Tällä versiolla on koontinumero V3.10.3.18 ja se on saatavilla seuraavan aikataulun mukaan:</span><span class="sxs-lookup"><span data-stu-id="8789a-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="8789a-111">**Yleinen saatavuus (itsepäivitys):** marraskuu 2019</span><span class="sxs-lookup"><span data-stu-id="8789a-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="8789a-112">**Automaattinen päivitys:** joulukuu 2019</span><span class="sxs-lookup"><span data-stu-id="8789a-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="8789a-113">Päivitysjulkaisu 13</span><span class="sxs-lookup"><span data-stu-id="8789a-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="8789a-114">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="8789a-114">Bug fixes</span></span>

- <span data-ttu-id="8789a-115">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="8789a-115">Time and Expense</span></span>

     - <span data-ttu-id="8789a-116">Korjattu: **Kulun hyväksyntä** -sivun hakutoiminto ei toimi, kun haetaan kulun tarkoituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="8789a-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="8789a-117">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="8789a-117">Resource Management</span></span>

     - <span data-ttu-id="8789a-118">Korjattu: Täsmäytyksessä numerot on päivitetty oikealle tasatuiksi.</span><span class="sxs-lookup"><span data-stu-id="8789a-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="8789a-119">Korjattu: Nimettyjä resursseja ei voi delegoida tehtäviin **Ajoitus**-välilehden kautta.</span><span class="sxs-lookup"><span data-stu-id="8789a-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="8789a-120">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="8789a-120">Project Management</span></span>

     - <span data-ttu-id="8789a-121">Korjattu: Poikkeus null-viittauksesta, kun määritetään ryhmän jäsentä, kun **TransactionType** puuttuu **Unit**- ja **DefaultGroup**-tiedoista.</span><span class="sxs-lookup"><span data-stu-id="8789a-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="8789a-122">Sales</span><span class="sxs-lookup"><span data-stu-id="8789a-122">Sales</span></span>

     - <span data-ttu-id="8789a-123">Korjattu: päällekkäiset tapahtumatyyppitietueet palauttavat virheen, kun roolien hintatietueita luodaan.</span><span class="sxs-lookup"><span data-stu-id="8789a-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="8789a-124">Korjattu: **Uusi mahdollisuus**-, **Tarjous**-, **Tilausrivi**- ja **Lisää tuotteet** -lisäpainikkeet näkyvät mahdollisuuksien, tarjousten, tilaustuotteiden ja projektipohjaisten rivien aliruudukon komennoissa.</span><span class="sxs-lookup"><span data-stu-id="8789a-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]