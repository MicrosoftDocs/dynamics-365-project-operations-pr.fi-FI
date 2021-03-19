---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 20, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 20, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: db416343ac9ac2591007e83be80493a48f9ae904
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280664"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="bed00-103">Project Service Automation -päivitysjulkaisu 20, V3</span><span class="sxs-lookup"><span data-stu-id="bed00-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bed00-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="bed00-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bed00-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="bed00-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bed00-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="bed00-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bed00-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="bed00-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bed00-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bed00-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bed00-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 20.</span><span class="sxs-lookup"><span data-stu-id="bed00-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="bed00-110">Tämän version koontiversion numero on V 3.10.31.37, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2020.</span><span class="sxs-lookup"><span data-stu-id="bed00-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="bed00-111">Päivitysjulkaisu 20</span><span class="sxs-lookup"><span data-stu-id="bed00-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bed00-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="bed00-112">Bug fixes</span></span>

<span data-ttu-id="bed00-113">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="bed00-113">**Project Management**</span></span>

<span data-ttu-id="bed00-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="bed00-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bed00-115">Kun projektiryhmän jäseniä tuodaan käyttämällä kohdistusmenetelmää, joka edellyttää tunteja, tuloksena on epäselvä virhesanoma, kun määritetyt tunnit ovat nolla.</span><span class="sxs-lookup"><span data-stu-id="bed00-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="bed00-116">Käyttäjät saavat virheellisen virheen, kun projektitehtävän **Kuvaus**-kenttään on syötetty enimmäismäärä merkkejä.</span><span class="sxs-lookup"><span data-stu-id="bed00-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="bed00-117">**Microsoft Dynamics 365 Project Service Automation-apuohjelman lataussivu** ohjaa englanninkieliseen lataussivuun, kun käyttäjän kieliasetukset on määritetty japaninkielisiksi.</span><span class="sxs-lookup"><span data-stu-id="bed00-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="bed00-118">Kun palvelinvirhe ilmenee, **Projektit**-lomakkeen **Aikataulu**-välilehden synkronoinnin selite säilyy joskus.</span><span class="sxs-lookup"><span data-stu-id="bed00-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="bed00-119">Tarpeettomia tehtävien päivityksiä lähetetään palvelimeen, kun tehtävää muokataan.</span><span class="sxs-lookup"><span data-stu-id="bed00-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="bed00-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bed00-120">**Sales**</span></span>

<span data-ttu-id="bed00-121">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="bed00-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="bed00-122">Kun kaksoisnapsautat **Palvelusopimus**-lomakkeessa **Luo lasku** -painiketta, se luo kaksi laskua yksittäiselle toteutuneiden arvojen tietueelle.</span><span class="sxs-lookup"><span data-stu-id="bed00-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="bed00-123">Internet Explorer 11 -käyttäjät eivät voi luoda kulumerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="bed00-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="bed00-124">Kulujen peruutusta ja laskuttamattoman myynnin toteutuneita arvoja ei linkitetä.</span><span class="sxs-lookup"><span data-stu-id="bed00-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="bed00-125">**Projekti**-lomakkeen **Päivitä toteutuneet** - painike ei päivitä **tehtävän todellisia tunteja**.</span><span class="sxs-lookup"><span data-stu-id="bed00-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="bed00-126">**PreValidateProjectTeamMemberCreate** -laajennus voi luoda kaksoiskappaleisia yleisiä varattavissa olevia resursseja, kun määritteen **msdyn_isgenericresourceprojectscoped** arvo on **False**.</span><span class="sxs-lookup"><span data-stu-id="bed00-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="bed00-127">**Laske uudelleen** -toiminto tyhjentää tuotepohjaisten tarjousrivien ja sopimusrivin tietojen laskutettavat kustannukset.</span><span class="sxs-lookup"><span data-stu-id="bed00-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="bed00-128">Tietyissä tilanteissa **PostEstimateLineUpdate**-laajennus näyttää null-viittauksen poikkeusvirheen.</span><span class="sxs-lookup"><span data-stu-id="bed00-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="bed00-129">**Kannattavuusanalyysikaavion** ajanjakson kesto ei vastaa kustannusten kestoa tarjouksen kiinteähintaisella tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="bed00-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="bed00-130">Yksikkö- ja yksikköryhmäarvot eivät oletusarvon mukaan ole oikein **Sopimusrivin tiedot**- ja **Tarjousrivin tiedot** -lomakkeiden kululuokille.</span><span class="sxs-lookup"><span data-stu-id="bed00-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="bed00-131">**Organisaation yksikkökustannushinta** -luettelot sallivat päivämäärän voimassaolon päällekkäisyydet.</span><span class="sxs-lookup"><span data-stu-id="bed00-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="bed00-132">Käyttäjät eivät voi muuttaa **organisaatioyksikköä**, kun järjestystyyppi ei ole työpohjainen, koska se johtaa null-viittauksen poikkeusvirheeseen.</span><span class="sxs-lookup"><span data-stu-id="bed00-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="bed00-133">Kun yrität siirtyä **Tarjousrivin tiedot** -lomakkeesta takaisin **Tarjous**-välilehteen, lomake päivittyy ja näyttää **Yhteenveto**-välilehden.</span><span class="sxs-lookup"><span data-stu-id="bed00-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]