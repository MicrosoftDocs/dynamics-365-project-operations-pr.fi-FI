---
title: Hyväksyntöjen kehittäjän huomautukset
description: Tässä artikkelissa on lisää kehittäjälle tarkoitettuja tietoja hyväksyntöjen käyttämisestä.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924748"
---
# <a name="developer-notes-for-approvals"></a>Hyväksyntöjen kehittäjän huomautukset

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations sisältää vahvistuslogiikan, joka varmistaa, että oikea tietue etenee hyväksyntävaiheissa. Tietueen oikeat siirtyvät varmistavat seuraavat: 

  - Kaikki tukirivit luodaan liittyvissä taulukoissa, kuten kirjauskansioissa ja todellisissa arvoissa.
  - Hyväksyjä merkitään projektissa **projektin hyväksyjäksi** ennen jatkamista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]