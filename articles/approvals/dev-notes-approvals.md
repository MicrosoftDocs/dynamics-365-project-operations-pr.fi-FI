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
# <a name="developer-notes-for-approvals"></a>Hyväksyntöjen kehittäjän huomautukset

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations sisältää vahvistuslogiikan, joka varmistaa, että oikea tietue etenee hyväksyntävaiheissa. Tietueen oikeat siirtyvät varmistavat seuraavat: 

  - Kaikki tukirivit luodaan liittyvissä taulukoissa, kuten kirjauskansioissa ja todellisissa arvoissa.
  - Hyväksyjä merkitään projektissa **projektin hyväksyjäksi** ennen jatkamista.
