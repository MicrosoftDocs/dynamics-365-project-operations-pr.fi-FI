---
title: Aikavyöhykkeiden hallinta
description: Kun projekti luodaan, sen aika vyöhyke perustuu käytettyyn työtuntimalliin määritettyyn aikavyöhykkeeseen.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075286"
---
# <a name="manage-time-zones"></a>Aikavyöhykkeiden hallinta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


## <a name="projects"></a>Projektit

Kun projekti luodaan, sen aika vyöhyke perustuu käytetyssä työtuntimallissa määritettyyn aikavyöhykkeeseen. **Projektissa** päivämäärät ovat aina suhteessa sen käyttäjän aikavyöhykkeeseen, joka on kirjautunut kuhunkin välilehteen **Tehtävä** -välilehteä lukuun ottamatta. Kun tarkastelet työrakennetta, päivämäärät näkyvät aina projektin aikavyöhykkeessä.

## <a name="tasks"></a>Tehtävät

Kun tehtävä luodaan, alkamisaikaa, päättymisaikaa ja tuntia/päivää ohjataan projektin työaikojen mukaan. Jos tehtävän on esimerkiksi luonut projekti, jonka aika vyöhyke on -8 PST ja jonka työaika on klo 9:00 – 17:00 maanantaista perjantaihin, mikä tahansa ilman delegointia luotu tehtävä noudattaa projektikalenterin alkamisaikaa ja päättymisaikaa.

## <a name="manage-resources-with-time-zones"></a>Resurssien hallinta aikavyöhykkeissä

Jotta saat tarkat ja ennustettavat tulokset, kun käytät **Laajenna varausta** -toimintoa, on täytettävä kaksi keskeistä edellytystä:  

- Käyttäjän on määritettävä laitteensa aikavyöhyke vastaamaan järjestelmän **mukautusasetuksissa** määritettyä aikavyöhykettä.
 
  ![Aikavyöhykeasetukset Windows 10:ssä](media/reconcile-assignments-03.png)

  ![Aikavyöhykeasetukset mukautusasetuksissa](media/reconcile-assignments-04.png)
 
- Varattavissa olevalla resurssilla on oltava vähintään yksi minuutti työaikaa, joka on päällekkäinen pyydetyn laajennuksen määrittämiseen käytettävien tietojen kanssa. Esimerkiksi seuraavat resurssit ovat työaikoja, jotka ovat välillä 9:00–19:00. 

  ![Resurssien muotojen vertailu](media/reconcile-assignments-05.png)

Seuraavassa taulukossa näkyy:

- Projektin kalenterimalli
- Resurssi A: Tällä resurssilla on sama kalenteri ja se on samassa aikavyöhykkeessä kuin projekti. Varausten alkamisaika on 9.00.
- Resurssi B: Tämä resurssi sijaitsee eri aikavyöhykkeellä kuin projekti, ja projekti alkaa klo 7:00 resurssin aikavyöhykkeessä. Varaukset alkavat kuitenkin alkaen klo 9.00, koska se on määritysmallin varhaisin alkamisaika.
- Resurssit C ja D: Resurssit sijaitsevat eri aikavyöhykkeillä, molemmat eri vyöhykkeillä verrattuna toisiinsa ja projektiin, ja resurssien varaukset alkavat aikaisintaan niiden käytettävissä olevina alkamisaikoina.

|Entiteetti  |Kalenteri  |
|-|-|
|Projektin kalenterimalli   | ![projektikalenteri](media/reconcile-assignments-06.png) |
|Resurssi A  | ![Resurssin A kalenteri](media/reconcile-assignments-06.png) |
|Resurssi B  |  ![Resurssin B kalenteri](media/reconcile-assignments-07.png) |
|Resurssi C  |  ![Resurssin C kalenteri](media/reconcile-assignments-08.png) |
|Resurssi D  | ![Resurssin D kalenteri](media/reconcile-assignments-09.png)  |
 
Kun siirryt **Täsmäytys** -näkymään, näkyviin tulevat resurssien delegoinnit ja niihin liittyvä varausvajeet.

![Täsmäytysnäkymä ennen laajentamista](media/reconcile-assignments-10.png)

Kun Laajenna varausta -toimintoa on käytetty kunkin resurssin kohdalla, varauksia laajennetaan onnistuneesti kullekin resurssille, koska kunkin resurssin työaika on päällekkäinen vajeen aikavälin kanssa.

![Täsmäytysnäkymä varauksen laajentamisen jälkeen](media/reconcile-assignments-11.png) 

Huomaa, että lähemmät tiedot varauksista osoittavat, miten varausten alkamisaika on erilainen. Varaus alkaa aikaisintaan delegoinnin aikavälin alussa ja aikaisintaan resurssin käytettävissäoloajan alkamisaikana.

![Resurssien uudet varaukset aikataulutaulukossa](media/reconcile-assignments-12.png)
