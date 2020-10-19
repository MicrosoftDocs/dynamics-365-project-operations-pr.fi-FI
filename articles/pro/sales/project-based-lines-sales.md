---
title: Projektipohjaiset mahdollisuusrivit (Pro)
description: Tässä aiheessa on tietoja projektipohjaisista mahdollisuusriveistä. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896367"
---
# <a name="project-based-opportunity-lines-pro"></a>Projektipohjaiset mahdollisuusrivit (Pro)

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektipohjaiset mahdollisuusivit ovat käytettävissä vain projektipohjaisissa mahdollisuuksissa. Projektipohjaisissa mahdollisuustietueissa on **Tyyppi**-kentän arvoksi on määritetty **Työperusteinen**.

Projektipohjaiset mahdollisuusrivit ovat riviimikkeitä, jotka toimitetaan asiakkaalle käyttämällä projektia. Projektia ei voi kuitenkaan sitoa projektipohjaiseen mahdollisuusriviin. Projektit voidaan sitoa rivinimikkeisiin **Tarjous**-vaiheesta eteenpäin, koska mahdollisuus on yleensä jo varhaisessa vaiheessa kaupan elinkaaren aikana. Sen määrittäminen, kuinka monta projektia asiakkaan työn toimittamiseen käytetään, on päätös, joka tehdään myöhemmin myyntivaiheessa. Voit käyttää mahdollisuusvaihetta asiakkaan erillisten toimituskomponenttien määrittämiseen. Näiden komponenttien toimittamiseen käytettävien projektien todellista määrää koskevat päätökset voidaan siirtää eteenpäin, kunnes itse työstä tiedetään enemmän.

Alla on projektipohjaisen mahdollisuusrivin kentät:

| **Kenttä** | **Sijainti** | **Relevanssi, tarkoitus ja opastus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Tuotetyyppi | Yleiset-välilehti (piilotettu) | Voit valita jonkin seuraavista vaihtoehdoista:</br>– Projektipohjainen palvelu (käytettävissä vain, kun Dynamics 365 Project Operations on asennettu)</br>– Tuotepohjainen (käytettävissä vain, kun Project Operations ja Dynamics 365 Sales on asennettu) | Tämän kentän arvoksi määritetään **Projektipohjainen palvelu**, kun luot projektipohjaisen mahdollisuusrivin mahdollisuuden projektipohjaisten rivien ruudukosta. <br> Jos muutat tai korvaat tämän arvon, projektin toimintoja ei voi ottaa käyttöön projektipohjaisissa rivinimikkeissä. |
| Mahdollisuus | Yleiset-välilehti | Tämä kenttä on vain luku -tilassa, ja se viittaa ylätason mahdollisuustietueeseen, johon tämä rivinimike kuuluu. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Nimi | Yleiset-välilehti | Tätä muokattavaa tekstikenttää voidaan käyttää lyhyen nimen antamiseen rivinimikkeelle. | Tämä arvo siirretään tarjousriville, kun luot tarjouksen tästä mahdollisuudesta. |
| Asiakasbudjetti | Yleiset-välilehti | Tämän muokattavan valuuttakentän avulla voit seurata summaa, jonka asiakas on halukas käyttämään tälle rivinimikkeelle. | Tämä arvo siirretään tarjousrivin vastaavaan kenttään, kun luot tarjouksen tästä mahdollisuudesta. |
| Laskutustapa | Yleiset-välilehti | Tällä muokattavalla kentällä on seuraavat arvot:</br>– Aika ja materiaali</br>– Kiinteä hinta | Tämä arvo siirretään tarjousrivin vastaavaan kenttään, kun luot tarjouksen tästä mahdollisuudesta. Kun tarjousrivi on luotu, kenttä on lukittu, eikä sitä voi muuttaa. Määritä tämän kentän arvo mahdollisimman tarkasti. Jos tämän kentän arvoa on muutettava tarjousrivillä, poista tarjousrivi ja luo se uudelleen. |
