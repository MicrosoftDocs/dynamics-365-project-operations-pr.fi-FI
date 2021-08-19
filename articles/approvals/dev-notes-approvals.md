---
title: Hyväksyntöjen kehittäjän huomautukset
description: Tässä aiheessa on lisää kehittäjälle tarkoitettuja tietoja hyväksyntöjen käyttämisestä.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991662"
---
# <a name="developer-notes-for-approvals"></a>Hyväksyntöjen kehittäjän huomautukset

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations sisältää vahvistuslogiikan, joka varmistaa, että oikea tietue etenee hyväksyntävaiheissa. Tietueen oikeat siirtyvät varmistavat seuraavat: 

  - Kaikki tukirivit luodaan liittyvissä taulukoissa, kuten kirjauskansioissa ja todellisissa arvoissa.
  - Hyväksyjä merkitään projektissa **projektin hyväksyjäksi** ennen jatkamista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]