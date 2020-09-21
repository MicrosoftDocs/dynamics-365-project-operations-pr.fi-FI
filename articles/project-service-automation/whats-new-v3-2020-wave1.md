---
title: Uutuudet ja muutokset Project Service Automation -versiossa 3.x vuoden 2020 1. julkaisuaallossa
description: Tässä aiheessa on tietoja Project Service Automation -version 3 uusista ja muuttuneista ominaisuuksista vuoden 2020 1. julkaisuaallossa.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751170"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="d08dc-103">Uutuudet ja muutokset Project Service Automation -versiossa 3 vuoden 2020 1. julkaisuaallossa</span><span class="sxs-lookup"><span data-stu-id="d08dc-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="d08dc-104">Aihe korostaa tärkeitä päivitysnäkökohtia, kun siirrytään uusimpaan Project Service Automation (PSA) -versioon 3.x vuoden 2020 1. julkaisuaallossa.</span><span class="sxs-lookup"><span data-stu-id="d08dc-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="d08dc-105">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="d08dc-105">Time entry</span></span>
<span data-ttu-id="d08dc-106">Ajan syöttökokemusta on laajennettu siten, että se antaa mahdollisuuden pidentää aikamerkintöjä asiakasskenaarioille.</span><span class="sxs-lookup"><span data-stu-id="d08dc-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="d08dc-107">Tähän sisältyy mahdollisuus lisätä merkintätyyppejä, jotka nyt toimivat eri tavoilla perustuen **Aikamerkinnän asetukset** -malliin, joka näytetään **ajan lähteenä**.</span><span class="sxs-lookup"><span data-stu-id="d08dc-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="d08dc-108">Päivityksessä huomioon otettavia seikkoja</span><span class="sxs-lookup"><span data-stu-id="d08dc-108">Upgrade consideration</span></span>
<span data-ttu-id="d08dc-109">Tämän toiminnon tueksi PSA-järjestelmän roolit on päivitetty siten, että ne sisältävät uusia oikeuksia.</span><span class="sxs-lookup"><span data-stu-id="d08dc-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="d08dc-110">Nämä oikeudet myöntävät lukuoikeuden uuteen entiteettiin nimeltä **Aikamerkinnän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="d08dc-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="d08dc-111">Käyttäjille, jotka tarvitsevat mahdollisuuden kirjata aikoja, on annettava käyttäjärooli **Aikamerkinnän käyttäjä** aiemmin annettujen roolien lisäksi.</span><span class="sxs-lookup"><span data-stu-id="d08dc-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="d08dc-112">Tämä rooli sisältää uudet toiminnot ja varmistaa, että ajan syöttö toimii edelleen.</span><span class="sxs-lookup"><span data-stu-id="d08dc-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="d08dc-113">Tällä hetkellä pidennetyt aikamerkinnän muutokset</span><span class="sxs-lookup"><span data-stu-id="d08dc-113">Currently extended time entry changes</span></span>
<span data-ttu-id="d08dc-114">Jotta aikamerkinnän nykyiseen käyttöön vaikutettaisiin mahdollisimman vähän, tämä roolien muutos on ainoa perusvaatimus, jota tarvitaan, jotta aikamerkintöjä voidaan jatkaa.</span><span class="sxs-lookup"><span data-stu-id="d08dc-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="d08dc-115">Jos olet luonut mukautettuja näkymiä tai erillisiä ajansyöttökokemuksia, määritä **Aikamerkinnän asetukset** -kentille oikeat PSA-arvot.</span><span class="sxs-lookup"><span data-stu-id="d08dc-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
