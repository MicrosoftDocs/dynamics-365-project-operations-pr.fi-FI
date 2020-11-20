---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 21, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126704"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="b55ec-103">Project Service Automation -päivitysjulkaisu 21, V3</span><span class="sxs-lookup"><span data-stu-id="b55ec-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="b55ec-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="b55ec-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b55ec-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="b55ec-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b55ec-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="b55ec-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b55ec-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="b55ec-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b55ec-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b55ec-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b55ec-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 21.</span><span class="sxs-lookup"><span data-stu-id="b55ec-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="b55ec-110">Tämän version koontiversion numero on V 3.10.32.50, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2020.</span><span class="sxs-lookup"><span data-stu-id="b55ec-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="b55ec-111">Päivitysjulkaisu 21</span><span class="sxs-lookup"><span data-stu-id="b55ec-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b55ec-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="b55ec-112">Bug fixes</span></span>

<span data-ttu-id="b55ec-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="b55ec-113">**Time and Expense**</span></span>

<span data-ttu-id="b55ec-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="b55ec-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b55ec-115">Kun **Aikamerkinnän ruudukko -ohjausobjekti** on käytössä koontinäytössä, ruudukko ei käytä koontinäytön ruudukkosäilön koko leveyttä.</span><span class="sxs-lookup"><span data-stu-id="b55ec-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="b55ec-116">**Aikamerkinnän ruudukko** -ohjausobjekti ei näytä tietueita tietyillä aikavyöhykkeillä.</span><span class="sxs-lookup"><span data-stu-id="b55ec-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="b55ec-117">Kello 21.00 jälkeiset aikamerkit näkyvät vääränä päivänä.</span><span class="sxs-lookup"><span data-stu-id="b55ec-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="b55ec-118">Käyttäjät eivät voi lähettää kuluja, jos kululuokassa **Kulun kuitti pakollinen** ei ole arvoa.</span><span class="sxs-lookup"><span data-stu-id="b55ec-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="b55ec-119">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="b55ec-119">**Resource Management**</span></span>

<span data-ttu-id="b55ec-120">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="b55ec-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="b55ec-121">Passiiviset varaukset näkyvät **Täsmäytys**-näkymässä.</span><span class="sxs-lookup"><span data-stu-id="b55ec-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="b55ec-122">Yleisestä resurssin toteutuksesta puuttui vahvistus, jolla varmistettiin, että varauksella on kelvollinen tila.</span><span class="sxs-lookup"><span data-stu-id="b55ec-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="b55ec-123">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="b55ec-123">**Project Management**</span></span>

<span data-ttu-id="b55ec-124">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="b55ec-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="b55ec-125">**Projekti**-lomakeruudukoita (**Resurssien delegointi**, **Tehtävä**, **Täsmäytys**-näkymä, **Kuluarviot**) ovat muokattavissa, vaikka projekti ei ole aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="b55ec-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="b55ec-126">Asiakkaiden kaksoiskappaleita ei voi yhdistää asiakkaisiin, jotka on linkitetty vahvistettuihin projektisopimuksiin.</span><span class="sxs-lookup"><span data-stu-id="b55ec-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="b55ec-127">Jos resurssiin ei ole lisätty kelvollista kalenteria, järjestelmä ei palauta käyttäjäystävällistä virhesanomaa.</span><span class="sxs-lookup"><span data-stu-id="b55ec-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="b55ec-128">Tehtäväruudukon **Lisää tehtävä** -painike on otettu käyttöön, kun projekti on linkitetty **Microsoft Project -apuohjelmaan**.</span><span class="sxs-lookup"><span data-stu-id="b55ec-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="b55ec-129">Työmäärä kasvaa hallitsemattomasti, kun luokan sisältävä tehtävä delegoidaan resurssille, jonka rooliin on määritetty kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="b55ec-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="b55ec-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b55ec-130">**Sales**</span></span>

<span data-ttu-id="b55ec-131">Seuraavat parannukset on tehty:</span><span class="sxs-lookup"><span data-stu-id="b55ec-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="b55ec-132">**Laskutustiheys**- ja **Laskutuksen aloitus** on siirretty **Laskutusaikataulu**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="b55ec-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="b55ec-133">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="b55ec-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="b55ec-134">**Luokan** **Myyntihinta yhteensä** on nolla (0), vaikka **roolin** myyntihinta yhteensä ei ole nolla.</span><span class="sxs-lookup"><span data-stu-id="b55ec-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="b55ec-135">Asiakkaat eivät voi muuttaa **Laskun tila** -kentän arvoksi **Valmis laskutukseen**, kun toinen mukautettu prosessi päivittää lisäkenttää.</span><span class="sxs-lookup"><span data-stu-id="b55ec-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="b55ec-136">**Päivitä laskurivit** -painike voi luoda useita rivien kaksoiskappaleita, jos se valitaan toistuvasti.</span><span class="sxs-lookup"><span data-stu-id="b55ec-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="b55ec-137">**Päivitä hinnat** -painike ei toimi **Pikanäkymä**-lomakkeen **Roolin hinnat** -aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="b55ec-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="b55ec-138">**Myyntihinnaston ratkaisun** logiikka käsittelee aikavyöhykkeitä virheellisesti, jolloin tuloksena on hinnastojen virheellinen valinta.</span><span class="sxs-lookup"><span data-stu-id="b55ec-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="b55ec-139">Projektin **Todelliset kulut yhteensä** voi olla murto-osan väärässä yhden aikamerkinnän hyväksynnän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b55ec-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="b55ec-140">**Hinnan ratkaisun** logiikka ei anna käyttäjäystävällistä virhesanomaa, jos **Noudettu roolihinta** -arvoja ei ole **Ensisijainen yksikkö**- ja **Hinta ensisijaisessa yksikössä** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="b55ec-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>