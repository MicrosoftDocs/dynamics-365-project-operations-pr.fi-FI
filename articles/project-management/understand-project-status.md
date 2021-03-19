---
title: Tietoja projektin tilasta
description: Tässä aiheessa on tietoja Dynamics 365 Project Operationsin projekteille määritetystä tilasta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286469"
---
# <a name="understand-project-status"></a><span data-ttu-id="a325a-103">Tietoja projektin tilasta</span><span class="sxs-lookup"><span data-stu-id="a325a-103">Understand project status</span></span>

<span data-ttu-id="a325a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a325a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a325a-105">**Projekti-entiteetti**-sivun **Tila**-osassa on projektin kunnon yhteenveto kustannusten ja työmäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="a325a-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="a325a-106">Tilan yhteenvetokentät</span><span class="sxs-lookup"><span data-stu-id="a325a-106">Status summary fields</span></span>

- <span data-ttu-id="a325a-107">**Projektin kokonaistila** -kenttä on muokattava kenttä, joka näyttää projektin kokonaistilan.</span><span class="sxs-lookup"><span data-stu-id="a325a-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="a325a-108">Tämä kenttä käyttää värikoodausta, kuten vihreää, keltaista ja punaista, osoittamaan lisääntyvää riskiä.</span><span class="sxs-lookup"><span data-stu-id="a325a-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="a325a-109">**Kommentit** -kentän avulla projektipäällikkö voi syöttää tilaan liittyviä kommentteja.</span><span class="sxs-lookup"><span data-stu-id="a325a-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="a325a-110">**Tila päivitetty** -kenttää ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="a325a-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="a325a-111">Tämän kentän arvo on aikaleima, joka ilmaisee, milloin tila on viimeksi päivitetty.</span><span class="sxs-lookup"><span data-stu-id="a325a-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="a325a-112">**Aikataulun tehokkuus**- ja **Kustannustehokkuus**-kentät määritetään seurantaruudukossa.</span><span class="sxs-lookup"><span data-stu-id="a325a-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="a325a-113">Kun pääsolmun aikataulu ja kustannusten ero **Työmäärän seuranta** -näkymässä ovat positiivisia, näiden kenttien arvoksi päivitetään **Edellä**.</span><span class="sxs-lookup"><span data-stu-id="a325a-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="a325a-114">Kun pääsolmun aikataulu ja kustannusten ero ovat negatiivisia, näiden kenttien arvoksi määritetään **Jäljessä**.</span><span class="sxs-lookup"><span data-stu-id="a325a-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]