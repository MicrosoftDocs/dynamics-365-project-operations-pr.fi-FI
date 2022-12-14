---
title: Projektin mahdollisuusrivit
description: Tässä artikkelissa on tietoja projektipohjaisista mahdollisuusriveistä. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e4f67bd9b7d51559e2942e9005b8f5f9187b1f78
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824951"
---
# <a name="project-opportunity-lines"></a>Projektin mahdollisuusrivit 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektin mahdollisuusivit ovat käytettävissä vain projektipohjaisissa mahdollisuuksissa. Projektipohjaisissa mahdollisuustietueissa on **Tyyppi**-kentän arvoksi on määritetty **Työperusteinen**.

Projektipn mahdollisuusrivit ovat riviimikkeitä, jotka toimitetaan asiakkaalle käyttämällä projektia. Projektia ei voi kuitenkaan sitoa projektipohjaiseen mahdollisuusriviin. Projektit voidaan sitoa rivinimikkeisiin **Tarjous**-vaiheesta eteenpäin, koska mahdollisuus on yleensä jo varhaisessa vaiheessa kaupan elinkaaren aikana. Sen määrittäminen, kuinka monta projektia asiakkaan työn toimittamiseen käytetään, on päätös, joka tehdään myöhemmin myyntivaiheessa. Voit käyttää mahdollisuusvaihetta asiakkaan erillisten toimituskomponenttien määrittämiseen. Näiden komponenttien toimittamiseen käytettävien projektien todellista määrää koskevat päätökset voidaan siirtää eteenpäin, kunnes itse työstä tiedetään enemmän.

Alla ovat projektipohjaisen mahdollisuusrivin kentät:

| **Field** | **Location** | **Description** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Tuotetyyppi | Yleiset-välilehti (piilotettu) | Voit valita jonkin seuraavista vaihtoehdoista:</br>- Projektipohjainen palvelu (käytettävissä vain kun Dynamics 365 Project Operations on asennettu)</br>- Tuotepohjainen (käytettävissä vain, kun Project Operations ja Dynamics 365 Sales on asennettu) | Tämän kentän arvoksi määritetään **Projektipohjainen palvelu**, kun luot projektipohjaisen mahdollisuusrivin mahdollisuuden projektipohjaisten rivien ruudukosta. <br> Jos muutat tai korvaat tämän arvon, projektin toimintoja ei voi ottaa käyttöön projektipohjaisissa rivinimikkeissä. |
| Mahdollisuus | Yleiset-välilehti | Tämä kenttä on vain luku -tilassa, ja se viittaa ylätason mahdollisuustietueeseen, johon tämä rivinimike kuuluu. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Nimi | Yleiset-välilehti | Tätä muokattavaa tekstikenttää voidaan käyttää lyhyen nimen antamiseen rivinimikkeelle. | Tämä arvo siirretään tarjousriville, kun luot tarjouksen tästä mahdollisuudesta. |
| Asiakasbudjetti | Yleiset-välilehti | Tämän muokattavan valuuttakentän avulla voit seurata summaa, jonka asiakas on halukas käyttämään tälle rivinimikkeelle. | Tämä arvo siirretään tarjousrivin vastaavaan kenttään, kun luot tarjouksen tästä mahdollisuudesta. |
| Laskutustapa | Yleiset-välilehti | Tällä muokattavalla kentällä on seuraavat arvot:</br>- Aika ja materiaali</br>- Kiinteä hinta | Tämä arvo siirretään tarjousrivin vastaavaan kenttään, kun luot tarjouksen tästä mahdollisuudesta. Kun tarjousrivi on luotu, kenttä on lukittu, eikä sitä voi muuttaa. Määritä tämän kentän arvo mahdollisimman tarkasti. Jos tämän kentän arvoa on muutettava tarjousrivillä, poista tarjousrivi ja luo se uudelleen. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
