---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 12, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 12, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: fc92a5dcc111688159f9be5b2839b7c040404a3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119954"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="48eef-103">Project Service Automation -päivitysjulkaisu 12, V3</span><span class="sxs-lookup"><span data-stu-id="48eef-103">Project Service Automation Update Release 12, V3</span></span>
<span data-ttu-id="48eef-104">Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen.</span><span class="sxs-lookup"><span data-stu-id="48eef-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="48eef-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="48eef-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="48eef-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="48eef-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="48eef-107">Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle.</span><span class="sxs-lookup"><span data-stu-id="48eef-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="48eef-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="48eef-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="48eef-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 12.</span><span class="sxs-lookup"><span data-stu-id="48eef-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="48eef-110">Tällä versiolla on koontinumero V3.10.2.34 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä lokakuusta 2019 lähtien.</span><span class="sxs-lookup"><span data-stu-id="48eef-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="48eef-111">Päivitysjulkaisu 12</span><span class="sxs-lookup"><span data-stu-id="48eef-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="48eef-112">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="48eef-112">Bug fixes</span></span>

- <span data-ttu-id="48eef-113">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="48eef-113">Time and Expense</span></span>

    - <span data-ttu-id="48eef-114">Korjattu: aikamerkinnän virheviesteihin on päivitetty merkityksellisempiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="48eef-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="48eef-115">Korjattu: Aikamerkintöjen ruudukko ja aikataulu näyttävät pystysuuntaisen vierityspalkin tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="48eef-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="48eef-116">Korjattu: Lähetettyjä kulu- ja aikamerkintöjä voidaan hyväksyä.</span><span class="sxs-lookup"><span data-stu-id="48eef-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="48eef-117">Korjattu: Hyväksynnän peruuttamisen vahvistusvalintaikkunan sanoma on korjattu, jotta se vastaisi hyväksynnän tilaa, kun se muutetaan tilasta **Hyväksytty** tilaan **Lähetetty**.</span><span class="sxs-lookup"><span data-stu-id="48eef-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="48eef-118">Korjattu: **Hinta**- **Yksikkö**- ja **Määrä**-kentät on nyt lukittu kulutietueessa sen jälkeen, kun se on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="48eef-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="48eef-119">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="48eef-119">Project Management</span></span>

    - <span data-ttu-id="48eef-120">Korjattu: **Uusi**-toiminto **Ryhmän jäsen** -päälomakkeessa on poistettu.</span><span class="sxs-lookup"><span data-stu-id="48eef-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="48eef-121">Korjattu: Resurssivaraukset on päivitetty epätarkkojen pyöristysten virheiden vuoksi, jotka johtivat tehtävän päättymispäivän muutokseen.</span><span class="sxs-lookup"><span data-stu-id="48eef-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="48eef-122">Korjattu: Käyttäjä näkee tehtäväruudukossa oleelliset palvelinpuolen virheet.</span><span class="sxs-lookup"><span data-stu-id="48eef-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="48eef-123">Korjattu: ryhmän jäsenen nimi muodostetaan nyt tehtävän Henkilöt-valitsimella toimen nimen sijaan.</span><span class="sxs-lookup"><span data-stu-id="48eef-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="48eef-124">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="48eef-124">Resource Management</span></span>

    - <span data-ttu-id="48eef-125">Korjattu: Mallista luotujen projektien resurssitarvetiedot käyttävät nyt projektikalenteria.</span><span class="sxs-lookup"><span data-stu-id="48eef-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="48eef-126">Korjattu: Taidot ja kompetenssit siirtyvät nyt oletusarvon mukaan roolien päätiedoista kyseiselle roolille luodulle resurssitarpeelle.</span><span class="sxs-lookup"><span data-stu-id="48eef-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="48eef-127">Sales</span><span class="sxs-lookup"><span data-stu-id="48eef-127">Sales</span></span>

    - <span data-ttu-id="48eef-128">Korjattu: **Sopimus**-päälomakkeesta löytyi päällekkäisiä objektitunnuksia.</span><span class="sxs-lookup"><span data-stu-id="48eef-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="48eef-129">Korjattu: logiikka on päivitetty, jotta **Tarjousanalyysi** -välilehti näkyy siten, että se näyttää välilehden metatietomääritykset.</span><span class="sxs-lookup"><span data-stu-id="48eef-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="48eef-130">Korjattu: Todellisten arvojen tietueen kirjanpitopäivä on nyt peräisin ajan/kulun merkintäpäivämäärästä eikä hyväksynnän päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="48eef-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
