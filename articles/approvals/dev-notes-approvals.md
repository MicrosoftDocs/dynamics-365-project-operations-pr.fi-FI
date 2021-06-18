---
title: Hyväksyntöjen kehittäjän huomautukset
description: Tässä aiheessa on lisää kehittäjälle tarkoitettuja tietoja hyväksyntöjen käyttämisestä.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996787"
---
# <a name="developer-notes-for-approvals"></a>Hyväksyntöjen kehittäjän huomautukset

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations sisältää vahvistuslogiikan, joka varmistaa, että oikea tietue etenee hyväksyntävaiheissa. Tietueen oikeat siirtyvät varmistavat seuraavat: 

  - Kaikki tukirivit luodaan liittyvissä taulukoissa, kuten kirjauskansioissa ja todellisissa arvoissa.
  - Hyväksyjä merkitään projektissa **projektin hyväksyjäksi** ennen jatkamista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]