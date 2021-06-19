---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 16, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006777"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="4b92e-103">Project Service Automation -päivitysjulkaisu 16, V3</span><span class="sxs-lookup"><span data-stu-id="4b92e-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4b92e-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="4b92e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4b92e-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="4b92e-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="4b92e-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="4b92e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4b92e-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="4b92e-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="4b92e-108">Lisätietoja on aiheessa [Ensisijaisen ratkaisun asentaminen tai päivittäminen](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="4b92e-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="4b92e-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 16.</span><span class="sxs-lookup"><span data-stu-id="4b92e-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="4b92e-110">Tällä versiolla on koontinumero V3.10.6.34 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä tammikuusta 2020 lähtien.</span><span class="sxs-lookup"><span data-stu-id="4b92e-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="4b92e-111">Päivitysjulkaisu 16</span><span class="sxs-lookup"><span data-stu-id="4b92e-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4b92e-112">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="4b92e-112">Bug fixes</span></span>

-   <span data-ttu-id="4b92e-113">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="4b92e-113">Time and Expense</span></span>

    -   <span data-ttu-id="4b92e-114">Korjattu: Käyttäjät, jotka yrittävät lähettää poistettuja aika- ja kulumerkintöjä hyväksyttäväksi, näkevät nyt asiaankuuluvat virhesanomat.</span><span class="sxs-lookup"><span data-stu-id="4b92e-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="4b92e-115">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="4b92e-115">Project Management</span></span>

    -   <span data-ttu-id="4b92e-116">Korjattu: Malleissa ryhmän jäsenille määritettyjä resursointiyksiköitä noudatetaan ja malleja sovelletaan uuteen projektiin.</span><span class="sxs-lookup"><span data-stu-id="4b92e-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="4b92e-117">Korjattu: Parannettu tietueiden omistajuuden uudelleenkohdistuksen käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="4b92e-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="4b92e-118">Korjattu: Projekteja, joita kopioidaan parhaillaan, ei voi kopioida ennen kuin kaikki kopiointitoiminnot on suoritettu loppuun.</span><span class="sxs-lookup"><span data-stu-id="4b92e-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="4b92e-119">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="4b92e-119">Resource Management</span></span>

    -   <span data-ttu-id="4b92e-120">Korjattu: Laajennetut varaukset käsittelevät nyt lyhyet kestot oikein eivätkä luo nollatunteja laajennetuille varauksille.</span><span class="sxs-lookup"><span data-stu-id="4b92e-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="4b92e-121">Korjattu: Täsmäytysnäkymä muodostetaan nyt, kun projektin aikavyöhyke on +5:30 GMT ja käyttäjän aikavyöhyke on jokin muu.</span><span class="sxs-lookup"><span data-stu-id="4b92e-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="4b92e-122">Sales</span><span class="sxs-lookup"><span data-stu-id="4b92e-122">Sales</span></span>

    -   <span data-ttu-id="4b92e-123">Korjattu: Kun sopimusriviin yhdistetty projekti poistetaan ja uusi projekti yhdistetään, uuden projektin todellisten tietueita ei arvioitu uudelleen sopimusrivillä määritettyjen laskutus- ja hinnoittelusääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4b92e-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="4b92e-124">Tämä on korjattu tässä julkaisussa.</span><span class="sxs-lookup"><span data-stu-id="4b92e-124">This has been fixed in this release.</span></span> <span data-ttu-id="4b92e-125">Uuden yhdistetyn projektin hinnoittelu ja todelliset tietueet palautetaan ja luodaan uudelleen oikein sopimusrivin hinnoittelu- ja laskutussääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4b92e-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="4b92e-126">Myös yhdistämättömän projektin todelliset tietueet arvioidaan ja luodaan uudelleen tämän seurauksena.</span><span class="sxs-lookup"><span data-stu-id="4b92e-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="4b92e-127">Korjattu: Arviorivin **Summa**-kenttään lisätty lisätarkistus, joka varmistaa, että null-arvot eivät säily.</span><span class="sxs-lookup"><span data-stu-id="4b92e-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="4b92e-128">Korjattu: Kun projektin todelliset arvot on päivitetty, projektin päälomakkeeseen on lisätty päivityspainike, jotta käyttäjät voivat synkronoida todelliset arvot uudelleen.</span><span class="sxs-lookup"><span data-stu-id="4b92e-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="4b92e-129">Korjattu: Kun käyttäjät päivittävät versiosta 2.X versioon 3.X, projektit, joiden nimi on NULL, ovat sallittuja.</span><span class="sxs-lookup"><span data-stu-id="4b92e-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]