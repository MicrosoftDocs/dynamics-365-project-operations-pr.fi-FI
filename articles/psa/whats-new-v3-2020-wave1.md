---
title: Uutuudet ja muutokset Project Service Automation -versiossa 3.x vuoden 2020 1. julkaisuaallossa
description: Tässä aiheessa on tietoja Project Service Automation -version 3 uusista ja muuttuneista ominaisuuksista vuoden 2020 1. julkaisuaallossa.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280169"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="c81f4-103">Uutuudet ja muutokset Project Service Automation -versiossa 3 vuoden 2020 1. julkaisuaallossa</span><span class="sxs-lookup"><span data-stu-id="c81f4-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c81f4-104">Aihe korostaa tärkeitä päivitysnäkökohtia, kun siirrytään uusimpaan Project Service Automation (PSA) -versioon 3.x vuoden 2020 1. julkaisuaallossa.</span><span class="sxs-lookup"><span data-stu-id="c81f4-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="c81f4-105">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="c81f4-105">Time entry</span></span>
<span data-ttu-id="c81f4-106">Ajan syöttökokemusta on laajennettu siten, että se antaa mahdollisuuden pidentää aikamerkintöjä asiakasskenaarioille.</span><span class="sxs-lookup"><span data-stu-id="c81f4-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="c81f4-107">Tähän sisältyy mahdollisuus lisätä merkintätyyppejä, jotka nyt toimivat eri tavoilla perustuen **Aikamerkinnän asetukset** -malliin, joka näytetään **ajan lähteenä**.</span><span class="sxs-lookup"><span data-stu-id="c81f4-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="c81f4-108">Tähän toimintoon on lisätty uusi ratkaisu, jonka nimi on aika, kulut, tilat ja hyväksynnät (TESA).</span><span class="sxs-lookup"><span data-stu-id="c81f4-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="c81f4-109">Päivityksessä huomioon otettavia seikkoja</span><span class="sxs-lookup"><span data-stu-id="c81f4-109">Upgrade consideration</span></span>
<span data-ttu-id="c81f4-110">Tämän toiminnon tueksi PSA-järjestelmän roolit on päivitetty siten, että ne sisältävät uusia oikeuksia.</span><span class="sxs-lookup"><span data-stu-id="c81f4-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="c81f4-111">Nämä oikeudet myöntävät lukuoikeuden uuteen entiteettiin nimeltä **Aikamerkinnän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="c81f4-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="c81f4-112">Käyttäjille, jotka tarvitsevat mahdollisuuden kirjata aikoja, on annettava käyttäjärooli **Aikamerkinnän käyttäjä** aiemmin annettujen roolien lisäksi.</span><span class="sxs-lookup"><span data-stu-id="c81f4-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="c81f4-113">Tämä rooli sisältää uudet toiminnot ja varmistaa, että ajan syöttö toimii edelleen.</span><span class="sxs-lookup"><span data-stu-id="c81f4-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="c81f4-114">Jos sinulla on myös mukautettuja sovellusmoduuleja, jotka sisältävät kaikki aikamerkintäkohteen lomakkeet, sinun on poistettava **TESA-aikamerkinnän pikaluontilomake** moduulista.</span><span class="sxs-lookup"><span data-stu-id="c81f4-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="c81f4-115">Tällä hetkellä pidennetyt aikamerkinnän muutokset</span><span class="sxs-lookup"><span data-stu-id="c81f4-115">Currently extended time entry changes</span></span>
<span data-ttu-id="c81f4-116">Jotta aikamerkinnän nykyiseen käyttöön vaikutettaisiin mahdollisimman vähän, tämä roolien muutos on ainoa perusvaatimus, jota tarvitaan, jotta aikamerkintöjä voidaan jatkaa.</span><span class="sxs-lookup"><span data-stu-id="c81f4-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="c81f4-117">Jos olet luonut mukautettuja näkymiä tai erillisiä ajansyöttökokemuksia, määritä **Aikamerkinnän asetukset** -kentille oikeat PSA-arvot.</span><span class="sxs-lookup"><span data-stu-id="c81f4-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]