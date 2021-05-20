---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 24, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 956dcd2a06fad1eec488ad81bec2de4bd0550e82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948911"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="08200-103">Project Service Automation -päivitysjulkaisu 24, V3</span><span class="sxs-lookup"><span data-stu-id="08200-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="08200-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="08200-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="08200-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="08200-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="08200-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="08200-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="08200-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="08200-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="08200-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="08200-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="08200-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 24.</span><span class="sxs-lookup"><span data-stu-id="08200-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="08200-110">Tällä versiolla on koontinumero V3.10.42.43 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä lokakuusta 2020 lähtien.</span><span class="sxs-lookup"><span data-stu-id="08200-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="08200-111">Päivitysjulkaisu 24</span><span class="sxs-lookup"><span data-stu-id="08200-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="08200-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="08200-112">Bug fixes</span></span>

<span data-ttu-id="08200-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="08200-113">**Sales**</span></span>

<span data-ttu-id="08200-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="08200-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="08200-115">Ongelma määritettäessä oletushinnastoa tuotteille.</span><span class="sxs-lookup"><span data-stu-id="08200-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="08200-116">Tarjouksen voiton suorituskyky on hidas, koska upotettu hinnasto ja roolien hintatietueet kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="08200-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="08200-117">**Projektisopimus/myyntikeskus** > **Tuoterivinimike/Tilausrivimäärä** pyöristetään automaattisesti lähimpään kokonaislukuun.</span><span class="sxs-lookup"><span data-stu-id="08200-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="08200-118">Korota järjestelmäoikeuksiin, kun luetaan hinnastoja.</span><span class="sxs-lookup"><span data-stu-id="08200-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="08200-119">Kopioi asiakkaan osoitekentät **address1_freighttermscode** ja **address1_shippingmethodcode** tarjoukseen/tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="08200-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="08200-120">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="08200-120">**Time and Expense**</span></span>

<span data-ttu-id="08200-121">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="08200-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="08200-122">**Aikamerkintä-ruudukko** ei tue **Vain päivämäärä** -aikatoiminnallisuutta.</span><span class="sxs-lookup"><span data-stu-id="08200-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="08200-123">**Aikamerkintä** ei päivity automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="08200-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="08200-124">Manuaalinen päivitys vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="08200-124">A manual refresh is required.</span></span>
- <span data-ttu-id="08200-125">Aikatietoja ei voi tuoda tehtävästä silloin, kun resurssin tehtävissä on tauko (0 tuntia).</span><span class="sxs-lookup"><span data-stu-id="08200-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="08200-126">Kun luodaan aikamerkintää, määritä aloitukseksi sama kuin **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="08200-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="08200-127">Ota aikamerkinnän joukkomuokkaus uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="08200-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="08200-128">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="08200-128">**Resource Management**</span></span>

<span data-ttu-id="08200-129">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="08200-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="08200-130">Jos yritetään päivittää päivän sisäisen varauksen tilaa ilman tarvetta, toiminto heittää null-ref -poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="08200-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="08200-131">Virhe **täsmäytysnäkymän** lataamisessa.</span><span class="sxs-lookup"><span data-stu-id="08200-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="08200-132">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="08200-132">**Project Management**</span></span>

<span data-ttu-id="08200-133">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="08200-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="08200-134">Kun siirrytään **projektiaikataulussa** **manuaalisesta** **automaattiseen**, automaattinen tallennus ei valmistu.</span><span class="sxs-lookup"><span data-stu-id="08200-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="08200-135">Kulukustannuksia ei pitäisi laskea **Projektin seuranta -ruudukon** varianssia kohti.</span><span class="sxs-lookup"><span data-stu-id="08200-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="08200-136">**Arvioiden tunniste** -sarakkeiden epäjohdonmukainen toiminta latauksen aikana verrattuna **aikavaihe**-tyypin vaihtamiseen.</span><span class="sxs-lookup"><span data-stu-id="08200-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="08200-137">Projektin todelliset kustannukset eivät ehkä vastaa **toteutuneiden arvojen** summaa.</span><span class="sxs-lookup"><span data-stu-id="08200-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="08200-138">**Yhteenveto**-välilehden **Arvioitu päättymispäivä** ei vastaa **Työrakenne-aikataulua**.</span><span class="sxs-lookup"><span data-stu-id="08200-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="08200-139">**Päivitä todelliset tunnit** ei toimi oikein, kun ulonnetaan.</span><span class="sxs-lookup"><span data-stu-id="08200-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="08200-140">Projektipäällikkö, joka ei ole **pääliiketoimintayksikössä**, ei voi luoda projektia.</span><span class="sxs-lookup"><span data-stu-id="08200-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="08200-141">**Kuluarvioiden** tehtävän tai luokan muutokset eivät säily.</span><span class="sxs-lookup"><span data-stu-id="08200-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="08200-142">**Sopimuksen kopio** kopioi laskutusaikataulut ja suoritustilan.</span><span class="sxs-lookup"><span data-stu-id="08200-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="08200-143">**Päivitä toteutuneet** -painike laskee yhteenvetotehtävät virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="08200-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="08200-144">Microsoft Project -apuohjelma: Korjaa null-viittausvirhe, jos jollain ryhmän jäsenellä on tyhjä resursointiyksikkö.</span><span class="sxs-lookup"><span data-stu-id="08200-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]