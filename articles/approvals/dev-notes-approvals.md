---
title: Hyväksyntöjen kehittäjän huomautukset
description: Tässä aiheessa on lisää kehittäjälle tarkoitettuja tietoja hyväksyntöjen käyttämisestä.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290265"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="8d05c-103">Hyväksyntöjen kehittäjän huomautukset</span><span class="sxs-lookup"><span data-stu-id="8d05c-103">Developer notes for Approvals</span></span>

<span data-ttu-id="8d05c-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="8d05c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d05c-105">Dynamics 365 Project Operations sisältää vahvistuslogiikan, joka varmistaa, että oikea tietue etenee hyväksyntävaiheissa.</span><span class="sxs-lookup"><span data-stu-id="8d05c-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="8d05c-106">Tietueen oikeat siirtyvät varmistavat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="8d05c-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="8d05c-107">Kaikki tukirivit luodaan liittyvissä taulukoissa, kuten kirjauskansioissa ja todellisissa arvoissa.</span><span class="sxs-lookup"><span data-stu-id="8d05c-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="8d05c-108">Hyväksyjä merkitään projektissa **projektin hyväksyjäksi** ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="8d05c-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]