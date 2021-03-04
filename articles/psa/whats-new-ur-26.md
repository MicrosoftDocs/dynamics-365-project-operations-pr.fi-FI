---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 26, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143554"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="603e0-103">Project Service Automation -päivitysjulkaisu 26, V3</span><span class="sxs-lookup"><span data-stu-id="603e0-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="603e0-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="603e0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="603e0-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="603e0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="603e0-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="603e0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="603e0-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="603e0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="603e0-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="603e0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="603e0-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin Päivitysjulkaisussa 26, V3.</span><span class="sxs-lookup"><span data-stu-id="603e0-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="603e0-110">Tämän version koontiversionumero on V3.10.44.59 ja se on yleisesti saatavilla omatoimipäivityksenä joulukuussa 2020.</span><span class="sxs-lookup"><span data-stu-id="603e0-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="603e0-111">Päivitysjulkaisu 26</span><span class="sxs-lookup"><span data-stu-id="603e0-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="603e0-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="603e0-112">Bug fixes</span></span>

<span data-ttu-id="603e0-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="603e0-113">**Time and Expense**</span></span>

<span data-ttu-id="603e0-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="603e0-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="603e0-115">Käyttäjät voivat muuttaa tehtävää hyväksytyssä/lähetetyssä aikamerkinnässä.</span><span class="sxs-lookup"><span data-stu-id="603e0-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="603e0-116">"Objektin viittausta ei ole määritetty" -virhe tallennettaessa aikamerkintää.</span><span class="sxs-lookup"><span data-stu-id="603e0-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="603e0-117">Aikamerkinnän tuonti resurssivarauksista luo aikamerkintöjä, joilla on väärät DateTime-arvot.</span><span class="sxs-lookup"><span data-stu-id="603e0-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="603e0-118">Kun Project Service Automation ja Field Service -sovellukset on molemmat asennettu, **Uusi**-painike näkyy kahdesti komentopalkissa Field Service -sovelluksen aikamerkinnöille.</span><span class="sxs-lookup"><span data-stu-id="603e0-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="603e0-119">**Salli yksikkö** ja **Yksikköryhmä** -solujen päivityksen toimivat nyt **Kuluarvio**-ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="603e0-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="603e0-120">**Päivitä aikamerkinnän muokkaus** -lomake sisältää **Aikajanan**.</span><span class="sxs-lookup"><span data-stu-id="603e0-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="603e0-121">Ajan hyväksyminen projektiin liittymättömille aikamerkinnöille tukkii järjestelmän, kun projektin hyväksyjän roolia etsitään.</span><span class="sxs-lookup"><span data-stu-id="603e0-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="603e0-122">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="603e0-122">**Resource Management**</span></span>

<span data-ttu-id="603e0-123">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="603e0-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="603e0-124">Lisätty oikeellisuustarkistus **PostProjectCreate**-laajennukseen tarkistamaan ensisijainen vaatimus ennen sellaisen luomista.</span><span class="sxs-lookup"><span data-stu-id="603e0-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="603e0-125">**Projektiryhmän jäsenen** pikaluontilomake luo tyhjäarvoisen viittauksen poikkeuksen, jos kentät poistetaan lomakkeesta.</span><span class="sxs-lookup"><span data-stu-id="603e0-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="603e0-126">Vaatimusten luonti 12 tuntua yli 1 vuoden epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="603e0-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="603e0-127">Parannettu virhesanoma tyhjäarvoisen viittauksen poikkeukselle resurssitarpeen luonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="603e0-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="603e0-128">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="603e0-128">**Project Management**</span></span>

<span data-ttu-id="603e0-129">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="603e0-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="603e0-130">Parannettu oikeellisuustarkistus korjaamaan tyhjäarvoisen viittauksen poikkeuksen **PreProjectUpdate**-laajennuksessa.</span><span class="sxs-lookup"><span data-stu-id="603e0-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="603e0-131">Microsoft Project Desktop -laajennuksen julkaisemat projektit poistavat delegoimattomat varaukset.</span><span class="sxs-lookup"><span data-stu-id="603e0-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="603e0-132">Lisätty uusi oikeellisuustarkistus, kun tehtävän projektiviittaus on virheellinen tyhjäarvoisen viittauksen poikkeuksesta johtuen **PreValidateProjectTaskUpdate**-laajennuksessa.</span><span class="sxs-lookup"><span data-stu-id="603e0-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="603e0-133">Ryhmän jäsen -ruudukko ei näytä erillisiä varauksia ryhmän jäsen -tietueessa.</span><span class="sxs-lookup"><span data-stu-id="603e0-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="603e0-134">Lisätty uusia tarkistus- ja virhesanomia, jotka johtuvat tyhjäarvoisen viittauksen poikkeuksesta **PreProjectTaskDelete**-laajennuksessa.</span><span class="sxs-lookup"><span data-stu-id="603e0-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="603e0-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="603e0-135">**Sales**</span></span>

<span data-ttu-id="603e0-136">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="603e0-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="603e0-137">Kun projektiin perustuva rivi valitaan tarjouksessa tai sopimuksessa, **Ehdotus**-painikkeen tulisi olla näkyvissä ainoastaan silloin, kun valitaan tuotteeseen perustuva rivi, joka liittyy olemassa olevaan tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="603e0-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="603e0-138">Erota **Create_Product** -oikeus **Create_ProjectContract**-oikeudesta.</span><span class="sxs-lookup"><span data-stu-id="603e0-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="603e0-139">Laskun rivin poistaminen aiheuttaa tyhdäarvoisen viittauksen epäonnistumisen kohteessa **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="603e0-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
