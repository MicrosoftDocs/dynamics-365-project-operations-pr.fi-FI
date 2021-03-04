---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 14, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 14, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147154"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="07448-103">Project Service Automation -päivitysjulkaisu 14, V3</span><span class="sxs-lookup"><span data-stu-id="07448-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="07448-104">Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen.</span><span class="sxs-lookup"><span data-stu-id="07448-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="07448-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="07448-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="07448-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="07448-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="07448-107">Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle.</span><span class="sxs-lookup"><span data-stu-id="07448-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="07448-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="07448-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="07448-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 14.</span><span class="sxs-lookup"><span data-stu-id="07448-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="07448-110">Tällä versiolla on koontinumero V3.10.4.21 ja se on saatavilla seuraavan aikataulun mukaan:</span><span class="sxs-lookup"><span data-stu-id="07448-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="07448-111">**Yleinen saatavuus (itsepäivitys):** tammikuu 2020</span><span class="sxs-lookup"><span data-stu-id="07448-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="07448-112">**Automaattinen päivitys:** 2020 helmikuu</span><span class="sxs-lookup"><span data-stu-id="07448-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="07448-113">Päivitysjulkaisu 14</span><span class="sxs-lookup"><span data-stu-id="07448-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="07448-114">Parannukset</span><span class="sxs-lookup"><span data-stu-id="07448-114">Enhancements</span></span>

- <span data-ttu-id="07448-115">Sales</span><span class="sxs-lookup"><span data-stu-id="07448-115">Sales</span></span>

     - <span data-ttu-id="07448-116">Mukautettujen kenttien arvot kopioidaan **Tarjousrivin tiedot** -kohdasta **Projektisopimusrivin tiedot** -kohtaan, kun tarjouksen tilaksi päivitetään **Suljettu voitettuna**.</span><span class="sxs-lookup"><span data-stu-id="07448-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="07448-117">Vahvistetut projektit voidaan muuttaa tilaan **Suljettu hävittynä**.</span><span class="sxs-lookup"><span data-stu-id="07448-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="07448-118">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="07448-118">Resource Management</span></span>

     - <span data-ttu-id="07448-119">Kun varauksia laajennetaan, käyttäjille näytetään vahvistusvalintaikkuna, jossa on varauksen tulosten yhteenveto ja linkki varausten ylläpitämiseen.</span><span class="sxs-lookup"><span data-stu-id="07448-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="07448-120">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="07448-120">Bug fixes</span></span>

- <span data-ttu-id="07448-121">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="07448-121">Time and Expense</span></span>

     - <span data-ttu-id="07448-122">Korjattu: käyttäjien kokemusta parannettu, kun käyttäjä ei ole valinnut korjattavia merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="07448-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="07448-123">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="07448-123">Resource Management</span></span>

     - <span data-ttu-id="07448-124">Korjattu: Resurssin varaus useaan kertaan ylittää varattavissa olevan resurssin nimen.</span><span class="sxs-lookup"><span data-stu-id="07448-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="07448-125">Sales</span><span class="sxs-lookup"><span data-stu-id="07448-125">Sales</span></span>

     - <span data-ttu-id="07448-126">Korjattu: kokonaismyyntihintaa ei lasketa, ennen kuin käyttäjä syöttää myös kustannushinnan projektin kuluarvioihin.</span><span class="sxs-lookup"><span data-stu-id="07448-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="07448-127">Korjattu: Tarjouksen sulkeminen tilassa **Voitettu** epäonnistuu, jos liittyvä projektisopimus ei ole tilassa **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="07448-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

