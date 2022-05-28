---
title: Project Service Automationin integrointiparametrit
description: Tässä ohjeaiheessa kerrotaan, miten oletustiedot kirjataan, kun integroit Microsoft Dynamics 365 for Project Service Automationin Microsoft Dynamics 365 Financen kanssa.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 70dcf44c0948bfb8f17c51e052b6c76e029d35fd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683672"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automationin integrointiparametrit

[!include[banner](../includes/banner.md)]

Voit määrittää **Project Service Automation -integrointiparametrit** -sivulla, miten oletustiedot lisätään, kun integroit Dynamics 365 Project Service Automationin Dynamics 365 Financen kanssa. Jotta projektit voidaan synkronoida Project Service Automationista Financeen, sinun täytyy määrittää seuraavat kentät.

Avaa **Project Service Automationin integrointiparametrit** -sivu kohdasta **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Dynamics 365 for Project Service Automationin integrointiparametrit**. 

> [!NOTE]
> - Projektitehtävien integrointi, kulutapahtumien luokat, työaika-arviot, kuluarviot ja toimintojen lukitus ovat käytettävissä versiossa 8.0.
> - Toteutuneiden arvojen integrointi on käytettävissä alkaen versiosta 8.0.1 tai myöhempi.


| Välilehti                    | Kenttä                | Kuvaus |
|------------------------|----------------------|-------------|
| Yleistiedot                | Oletusprojektityyppi | Valitse oletusprojektityyppi. Kun projekteja synkronoidaan Project Service Automationista, tätä arvoa käytetään, jos et ole antanut oletusarvoa integrointimallissa. Synkronoinnin aikana uusien projektien **Projektityyppi**-kentän arvoksi määritetään tämä arvo. Arvo saatetaan kuitenkin päivittää, kun projektin sopimusrivit synkronoidaan Project Service Automationista. |
|                        | Aikaluokka        | Valitse oletusaikaluokka. Tätä arvoa käytetään, kun työaika-arviot synkronoidaan Project Service Automationista. Kun työaika-arvioita ja toteutuneita työaikoja synkronoidaan Project Service Automationista, uusien työaikaennusteiden **Luokka**-kentän arvoksi Financessa määritetään tämä arvo. |
|                        | Maksuluokka         | Valitse oletusmaksuluokka. Tätä arvoa käytetään, kun toteutuneet maksut synkronoidaan Project Service Automationista. Kun toteutuneita maksuja synkronoidaan Project Service Automationista, uusien maksutapahtumien **Luokka**-kentän arvoksi Financessa määritetään tämä arvo. |
| Projektiryhmän oletusarvot | Projektin tyyppi         | Valitse **Uusi**, kun haluat lisätä rivin, jolla voit valita projektityypin, jolle määritetään oletusarvoinen projektiryhmä. Tietty projektityyppi voidaan valita vain kerran määrityksessä. |
|                        | Projektiryhmä        | Valitse valitun projektityypin oletusprojektiryhmä. Kun uusia projekteja synkronoidaan Project Service Automationista, **Projektiryhmä**-kentän arvoksi määritetään projektiryhmän oletusarvo, jos et ole määrittänyt oletusarvoa integrointimallissa. |
| Laskutustyypin oletusravot  | Laskutustyyppi         | Valitse **Uusi**, kun haluat lisätä rivin, jolla voit valita laskutustyypin, jolle määritetään oletusarvoinen riviominaisuus. Tietty laskutustyyppi voidaan valita vain kerran määrityksessä. |
|                        | Riviominaisuus        | Valitse valitulle laskutustyypille oletusarvoinen riviominaisuus. Kun uusia työaika-arvioita, uusia kuluarvioita tai uusia toteutuneita arvoja synkronoidaan Project Service Automationista, **Riviominaisuus**-kentän arvoksi määritetään laskutustyypin oletusarvo. |
| Toimintojen lukitus  | Ei käytettävissä       | Valitse Financen toiminta, joka poistetaan käytöstä projekteilla ja sopimuksilla, jotka ovat peräisin Project Service Automationista. Voit esimerkiksi poistaa käytöstä mahdollisuuden muokata sopimuksia ja projekteja, luoda työrakenteita ja kirjata aikaraportteja Financessa. Kirjan pitoon liittyvät kentät ovat edelleen käytössä, vaikka ne eivät parametriasetuksen mukaan olisi käytettävissä. Kaikki toiminnot ovat oletusarvoisesti käytössä. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]