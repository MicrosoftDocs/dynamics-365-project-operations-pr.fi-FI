---
title: suojausmalli
description: Tämä aihe tarjoaa tietoja Dynamics 365 Project Operationsin suojausmallista.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e875d1765b5038e60830d626abb5bcd61749ece1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075233"
---
# <a name="security-model"></a>Suojausmalli

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Microsoft Dynamics 365 Project Operations sisältää yksilöllisen suojausmallin, joka mahdollistaa roolipohjaisen liiketoiminnan suojausmallin, joka toimii yhteistyössä Microsoft Office -ryhmien kanssa. 


## <a name="security-roles"></a>Käyttöoikeusroolit
Project Operationsin edustatoiminnot sisältävät seuraavat roolit:

| Rooli                          | Kuvaus                                                                                                                                                                 | Laajuus |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Toiminnon johtaja              | Tukee projektien välisiä raportteja.                                                                                                            | Liiketoimintayksikkö              |
| Projektin hyväksyjä              | Hyväksyy ajan ja kulut projektissa.                                                                                                                              | Liiketoimintayksikkö |
| Projektiaskutuksen järjestelmänvalvoja | Luo laskuehdotuksen.                                                                                                                                                 | Liiketoimintayksikkö |
| Projektipäällikkö               | Luo projektisuunnitelman ja pyytää resursseja.                                                                                                                              | Liiketoimintayksikkö |
| Projektiresurssi              | Ryhmän jäsenet, jotka voidaan varata ja jotka voivat raportoida aikaa.                                                                                                          | Liiketoimintayksikkö|
| Reusrssipäällikkö              | Kaikki resurssienhallintatoiminnot, kuten resurssipyyntöjen ja varauksien toteuttaminen, erotetaan toisistaan tukemaan hybridiä projektipäällikkö + resurssipäällikkö -kokoonpanoa ja keskitettyä resurssipäällikkö -roolia. | Liiketoimintayksikkö |


Microsoft Project -verkkoversio sisältää seuraavat roolit:

| Rooli           | Kuvaus                                                                                                        | Laajuus  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projektikäyttäjä   | Projektin yhteistyökäyttäjä, joka voi luoda omia projektejaan ja tarkastella projekteja, jotka on jaettu hänen kanssaan. | Käyttäjä   |
| Projektijärjestelmä | Sovelluskontekstissa käytettävä rooli. Asiakkaat eivät saa käyttää tätä järjestelmäroolia.                                    | Yleiset |

## <a name="security-enforcement"></a>Suojauksen pakotus
Projektitasolla suoritettavat toiminnot suoritetaan kirjautuneen käyttäjän kontekstissa. Tämä tarkoittaa sitä, että jos haluat luoda, avata tai poistaa projektin, käyttäjällä on oltava käyttöoikeus CDS:ssä. CDS-käyttöoikeus voidaan myöntää millä tahansa ympäristöön sisältyvillä mahdollisilla mekanismeilla. Esimerkiksi, käyttäjä, jolla on suurempi vaikutusalue, voi käyttää projektia tai myös siinä tapauksessa, että on suoritettu erillinen projektin jakotoiminto, joka myöntää käyttöoikeudet käyttäjälle.

On tärkeää huomioida tämä, kun projekteja luodaan Project Operationsissa.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderni ryhmän yhteistyö Project Operationsissa
Project-verkkoversio ja Project Operations tukevat moderneja yhteistyöryhmiä. Käyttäjät, jotka on lisätty projektiin ryhmän kautta, voivat muokata projektisuunnitelmaa.

Project-verkkoversio lisää käyttäjät ryhmään automaattisesti delegoinnin yhteydessä.

Ryhmät sallivat projektin käyttöoikeudet ja tukevat yhteistyöartefaktien käsittelyä yhteistyönä. Seuraavassa kaaviossa on kuvattu ryhmän delegointiprosessin aikana tapahtuvat tapahtumat ja tilan muutokset.

Project Operations ei luo ryhmää implisiittisen toiminnon kautta, vaan se tapahtuu vain, jos painat Ryhmät-näppäintä.

Ryhmän jäsenen haku **Ryhmän hallinta** -valintaikkunassa rajoittuu niihin, jotka on määritetty osana ympäristön suojausryhmää. Lisätietoja: [Ympäristön käyttöoikeuksien hallinta: käyttöoikeusroolit ja käyttöoikeudet](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Ryhmätila](./media/groupsmode.png)

1. Projekti luodaan ja sen omistaa projektin luonut käyttäjä.
2. Projektin omistaja päivitetään ryhmään.
3. Omistajaryhmä on yhdistetty määritettyyn tai luotuun Office-ryhmään.
4. Projektin alkuperäinen omistaja on lisätty Office-ryhmään.

## <a name="deployment-recommendation"></a>Käyttöönottosuositukset
Kun Office-ryhmän yhteiskäyttömalli kehittyy, toiminnallisuutta lisätään, jotta aikaa voidaan hallita tarkemmin. Asiakkaita, jotka ottavat tänään käyttöön Project Operationsin, kehotetaan käyttämään perinteistä Microsoft Dynamics 365 -suojausmallia.

Lisätietoja: [Common Data Servicen suojaus](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operationsin ja Microsoft Dynamics 365 Financen suojaus
Project Operations sisältää seuraavat roolit:

- Projektipäällikkö
- Projektin kirjanpitäjä

Lisätietoja Financen suojauksesta on aiheessa [Roolipohjainen suojaus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


