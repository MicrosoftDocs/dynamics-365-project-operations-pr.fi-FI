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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483944"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="c89d0-103">Hyväksyntöjen kehittäjän huomautukset</span><span class="sxs-lookup"><span data-stu-id="c89d0-103">Developer notes for Approvals</span></span>

<span data-ttu-id="c89d0-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c89d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c89d0-105">Dynamics 365 Project Operations sisältää vahvistuslogiikan, joka varmistaa, että oikea tietue etenee hyväksyntävaiheissa.</span><span class="sxs-lookup"><span data-stu-id="c89d0-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="c89d0-106">Tietueen oikeat siirtyvät varmistavat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="c89d0-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="c89d0-107">Kaikki tukirivit luodaan liittyvissä taulukoissa, kuten kirjauskansioissa ja todellisissa arvoissa.</span><span class="sxs-lookup"><span data-stu-id="c89d0-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="c89d0-108">Hyväksyjä merkitään projektissa **projektin hyväksyjäksi** ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="c89d0-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
