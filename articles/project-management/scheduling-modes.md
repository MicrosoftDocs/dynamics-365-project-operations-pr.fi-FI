---
title: Aikataulutustilat
description: Tässä aiheessa on tietoja aikataulutustiloista.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981431"
---
# <a name="scheduling-modes"></a>Aikataulutustilat

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Dynamics 365 Project Operations tarjoaa organisaatioille mahdollisuuden määritellä, miten ne hallitsevat tehtävien keskeisten muuttujien muutoksia työrakenteessa. Projektipäälliköt voivat organisaation tarpeiden perusteella tehdä muutoksia aikataulutustilaan projektia luodessaan.

Project Operationsissa on käytettävissä kolme aikataulutustilaa:

  - Kiinteä kesto (tämä on oletustila)
  - Kiinteä työ
  - Kiinteät yksiköt

Tietyn aikataulutustilan määrityksen vaikutukset määräytyvät seuraavan kaavan mukaan:

  Työmäärä (*työ*) = Kesto x yksiköt

Kun määrität projektin aikataulutustilan, määrität yhden näistä arvoista, joita ei voi muuttaa. Jos tämä arvo pidetään asetinarvona, arvoksi tulee prioriteetti, joka ilmoittaa, että järjestelmä ei halua muuttaa arvoa, kun muut arvot muuttuvat. Seuraavassa taulukossa on tietoja tietyn tilan valitsemisen vaikutuksista.

| **Tässä tehtävässä**             | **Jos muutat yksiköitä**   | **Jos muutat kestoa** | **Jos muutat työmäärää**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Kiinteät yksikkötehtävät     | Kesto lasketaan uudelleen. | Työmäärä lasketaan uudelleen.    | Kesto lasketaan uudelleen. |
| Kiinteän työmäärän tehtävä    | Kesto lasketaan uudelleen. | Yksiköt lasketaan uudelleen.    | Kesto lasketaan uudelleen. |
| Kiinteän keston tehtävä  | Työmäärä lasketaan uudelleen.   | Työmäärä lasketaan uudelleen.    | Yksiköt lasketaan uudelleen.   |

Lisätietoja tietyn tilan vaikutuksista on ohjeaiheessa [Tehtävätyypin muuttaminen tarkempaa aikataulutusta varten](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Aiheessa **Työ**-termiä käytetään **Työmäärä**-termin sijaan.

## <a name="change-the-organizations-scheduling-mode"></a>Organisaation aikataulutustilan muuttaminen

Määritä organisaation aikataulutustila seuraavien vaiheiden mukaisesti.

1. Siirry kohtaan **Asetukset** \> **Yleiset** \> **Parametrit** ja valitse sitten projektin parametri. 
2. Valitse **Projektin parametrit** -sivulla organisaation oletusajoitustila ja määritä sitten projektipäällikölle mahdollisuus ohittaa asetus uutta projektia luotaessa.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Projektin aikataulutustilan asetuksen muuttaminen

Jos organisaatio sallii projektipäällikön ohittaa oletusajoitustilan, projektipäällikkö voi tehdä muutoksen uutta projektia luodessaan. Kun projekti on tallennettu, ajoitustilaa ei voi kuitenkaan muuttaa.

## <a name="copied-projects"></a>Kopioidut projektit

Koska projekti luodaan, kun kopiointitoiminto suoritetaan, projektipäällikkö ei voi asettaa ajoitustilaa. Kohdeprojektin oletusarvo on aina organisaatiotasolla määritetty tila.

## <a name="copied-tasks"></a>Kopioidut tehtävät

Kun tehtävä kopioidaan projektista toiseen, tehtävä perii kohdeprojektin aikataulutustilan.
