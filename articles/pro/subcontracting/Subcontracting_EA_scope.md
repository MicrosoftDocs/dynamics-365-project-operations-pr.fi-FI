---
title: Alihankinta lokakuun 2021 ennakkojulkaisussa
description: Tässä aiheessa on yleiskatsaus Project Operationsin alihankintatoimintoihin, jotka kuuluvat lokakuun 2021 ennakkojulkaisuun.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383691"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Alihankinta lokakuun 2021 ennakkojulkaisussa

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä aiheessa on yleiskatsaus Dynamics 365 Project Operationsin alihankintatoimintoihin, jotka kuuluvat lokakuun 2021 ennakkojulkaisuun. Tämä ominaisuusjoukko ei ole valmis tuotantoympäristöön tai live-ympäristöihin, joten ominaisuudet säilyvät ennakkojulkaisussa, kunnes valmis ominaisuusjoukko on julkaistu. On erittäin suositeltavaa, että et käytä alihankintatoimintoa live-tuotantoskenaarioissa ennen kuin esiversiopalkki on poistettu. 

Seuraavassa luettelossa on esitetty, mitä lokakuun 2021 ennakkojulkaisussa on tällä hetkellä saatavilla:

1. Projektipäällikkö luo alihankintasopimuksen toimittajan kanssa. Alihankintasopimuksessa käytetään oletusarvoisesti toimittajatietueeseen liitettyjä hinnastoja. Toimittajatilin suhdetyyppi on **Toimittaja** tai **Alihankkija**.

2. Projektipäällikkö voi määrittää kaikki ostot alihankkijan rivinimikkeiksi. Alihankkijarivit voivat olla ajan, kulujen tai tuotteiden rivejä. Kukin alihankintarivin tapahtumaluokka määrittää rivin.

3. Toimittajan asiakaspäällikkö ja projektipäällikkö voivat iteroita alihankkijan yli. Hinnoittelua voidaan säätää alihankintasopimukseen liitetyissä ostohinnoissa.

4. Tässä vaiheessa tai myöhemmin prosessin aikana, jos alihankintarivi on määräaikainen, toimittajien asiakkuuspäällikkö liittää toimittajan yhteyshenkilöt kuhunkin alihankintariviin. Tämä liitos antaa tietoja alihankintapäällikölle, joka laatii alihankintasopimusta. Kun toimittaja liitetään alihankintariviin, järjestelmä luo automaattisesti yhteyshenkilöltä varattavissa olevan resurssin, jos varaavaa resurssia ei vielä ole.

5. Kunkin alihankkijarivin laskutustapa voi olla **Kiinteä hinta** tai **Aika ja Materiaali**. Kiinteähintaisia alihankintarivejä varten määritetään välitavoitteeseen perustuva laskuaikataulu.

Jäljellä olevat alihankinnan liiketoimintaprosessin vaiheet, jotka kuvaillaan yleiskatsauksessa, eivät ole tällä hetkellä käytettävissä. Kun uusia toimintoja lisätään, tämä aihe päivitetään. 

Seuraavassa kuvassa näkyy alihankinnan ennakkojulkaisun vertailu päästä päähän-liiketoimintaprosessiin.

![Alihankintaprosessin työnkulku](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Määräpohjaisten alihankintarivien ja työpohjaisten alihankintarivien ennakkojulkaisu
Lokakuun 2021 ennakkojulkaisussa tuetaan vain määräpohjaisia alihankintarivejä. Tämä tarkoittaa sitä, että alihankintarivin avulla voidaan ostaa toimittajalta aikaa, kuluja tai materiaaleja, mutta ei koko työmäärää. Tämä tarkoittaa myös sitä, että alihankintarivillä ostettua määrää (aikayksiköitä, kuluja tai materiaalimäärää) voidaan käyttää missä tahansa järjestelmän projektissa.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
