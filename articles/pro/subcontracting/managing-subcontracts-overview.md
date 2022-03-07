---
title: Alihankintasopimusten hallinta Project Operationsissa
description: Tämä aihe tarjoaa yleiskatsauksen alihankintojen hallintaprosessista Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994227"
---
# <a name="subcontract-management-in-project-operations"></a>Alihankintasopimusten hallinta Project Operationsissa

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsin alihankinta tukee seuraavia liiketoimintaprosessien työnkulkuja.

![Alihankintaprosessin työnkulku](../media/SubcontractingProcessFlow.png)

Tässä on alihankintaprosessin vaiheittainen kuvaus.

1. Projektipäällikkö luo alihankintasopimuksen toimittajan kanssa. Alihankintasopimuksessa käytetään oletusarvoisesti toimittajatietueeseen liitettyjä hinnastoja. Toimittajatilin suhdetyyppi on **Toimittaja** tai **Alihankkija**.
2. Projektipäällikkö voi määrittää kaikki ostot alihankkijan rivinimikkeiksi. Alihankkijarivit voivat olla ajan, kulujen tai tuotteiden rivejä. Kullakin alihankkijarivillä valittu tapahtumaluokka määrittää rivin.
3. Toimittajan asiakaspäällikkö ja projektipäällikkö voivat iteroita alihankkijan yli. Hinnoittelua voidaan säätää alihankintasopimukseen liitetyissä ostohinnoissa.
4. Tässä vaiheessa tai myöhemmin prosessin aikana, jos alihankkijarivi on määräaikainen, toimittajien asiakkuuspäällikkö liittää yhteyshenkilöt kuhunkin alihankkijariviin. Tämä liitos antaa tietoja alihankintapäällikölle, joka laatii alihankintasopimusta. Kun yhteyshenkilö liitetään alihankkijariviin, järjestelmä luo automaattisesti yhteyshenkilöltä varattavissa olevan resurssin, jos varaavaa resurssia ei vielä ole.
5. Kunkin alihankkijarivin laskutustapa voi olla **Kiinteä hinta** tai **Aika ja Materiaali**. Kiinteähintaisia alihankkijarivejä varten voit määrittää välitavoitteeseen perustuvan laskuaikataulun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
