---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 18, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119864"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="bce24-103">Project Service Automation -päivitysjulkaisu 18, V3</span><span class="sxs-lookup"><span data-stu-id="bce24-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="bce24-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="bce24-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bce24-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="bce24-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bce24-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="bce24-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bce24-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="bce24-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="bce24-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bce24-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bce24-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 18.</span><span class="sxs-lookup"><span data-stu-id="bce24-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="bce24-110">Tämän version koontiversion numero on V 3.10.8.12, ja se on yleisesti saatavana itsepäivittyvänä huhtikuussa 2020.</span><span class="sxs-lookup"><span data-stu-id="bce24-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="bce24-111">Päivitysjulkaisu 18</span><span class="sxs-lookup"><span data-stu-id="bce24-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bce24-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="bce24-112">Bug fixes</span></span>

<span data-ttu-id="bce24-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="bce24-113">**Time and Expense**</span></span>

- <span data-ttu-id="bce24-114">Korjattu: **Palautus**-, **Pyyntö**- ja **Peruuta hyväksyntä** -työnkulut aiheuttavat poikkeuksen, joiden virhesanoma on epäselvä.</span><span class="sxs-lookup"><span data-stu-id="bce24-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="bce24-115">Korjattu: kun **Peruuta hyväksyntä** epäonnistuu kulun osalta, se ei aiheuta siihen liittyvää poikkeusta.</span><span class="sxs-lookup"><span data-stu-id="bce24-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="bce24-116">Korjattu: Aikamerkintä-ruudukko käsittelee Australian muut kuin työpäivät virheellisesti lokakuussa tapahtuvan talviaikaan siirtymisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bce24-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="bce24-117">Korjattu: virheellinen oletuslogiikka estää kulujen lähettämisen.</span><span class="sxs-lookup"><span data-stu-id="bce24-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="bce24-118">Korjattu: kun aikamerkinnän hyväksyntä epäonnistuu, hyväksyntä pysyy **Odottaa**-tilana.</span><span class="sxs-lookup"><span data-stu-id="bce24-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="bce24-119">Korjattu: joukkohyväksymisten SQL-virheet (lukkiutuminen/aikakatkaisu).</span><span class="sxs-lookup"><span data-stu-id="bce24-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="bce24-120">Korjattu: ryhmän jäsenten päivittäminen aikamerkintöjä hyväksyttäessä aiheuttaa merkittäviä käyttökokemuksen suorituskykyongelmia.</span><span class="sxs-lookup"><span data-stu-id="bce24-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="bce24-121">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="bce24-121">**Project Management**</span></span>

- <span data-ttu-id="bce24-122">Korjattu: aikavyöhykeilmoitus siirrettiin **Täsmäytys**-näkymästä **Projekti**-päälomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="bce24-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="bce24-123">Korjattu: kalenterimallissa ei käytetä oikeita oletusarvoja, kun uusi projektilomake avautuu.</span><span class="sxs-lookup"><span data-stu-id="bce24-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="bce24-124">Korjattu: chromium-pohjaisten selainten käyttäjillä ei ole helppoa tapaa valita poistettavia edeltäjän tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="bce24-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="bce24-125">Korjattu: kun **projektin tyhjää mallia** käytetään luontiin tai kopiointiin, noudettavat tehtävät eivät liity siihen.</span><span class="sxs-lookup"><span data-stu-id="bce24-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="bce24-126">Korjattu: joissakin reunan palvelupyynnöissä uuden määrityksen luonti tehtäväruudukossa aiheuttaa tietueiden kaksoiskappaleiden luonnin.</span><span class="sxs-lookup"><span data-stu-id="bce24-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="bce24-127">Korjattu: käyttäjät eivät voi päivittää manuaalisessa tilassa tehtävän alkamispäiviä nykyistä tallennettua päivämäärää myöhäisemmäksi.</span><span class="sxs-lookup"><span data-stu-id="bce24-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="bce24-128">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="bce24-128">**Resource Management**</span></span>

- <span data-ttu-id="bce24-129">Korjattu: **Täsmäytys**-näkymän välisummarivi laskee varausten eron virheellisesti varausten laajennusten jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bce24-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="bce24-130">Korjattu: **Täsmäytys**-näkymä näyttää resurssimääritykset virheellisesti, kun varattavissa olevalla resurssilla on kalenteri, joka ei vastaa projektikalenteria.</span><span class="sxs-lookup"><span data-stu-id="bce24-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="bce24-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bce24-131">**Sales**</span></span>

- <span data-ttu-id="bce24-132">Korjattu: kun aikamerkinnät hyväksytään uudelleen (**Hyväksy > Peruuta >** hyväksyntä uudelleen), todellisen ei-veloitettavan kaksoiskappale luodaan.</span><span class="sxs-lookup"><span data-stu-id="bce24-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
