---
title: Hyväksyntöjen yleiskatsaus
description: Tämä aihe tarjoaa tietoja hyväksymisten käsittelemisestä Project Operationsissa.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075208"
---
# <a name="approvals-overview"></a>Hyväksyntöjen yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ajan ja kulujen lähetykset siirtyvät hyväksymisen työnkulun läpi. Kun tapahtumat on hyväksytty, tapahtumat kirjataan toteutuneisiin tai aika varataan aikataulussa.

## <a name="approvals-workflow"></a>Hyväksyntätyönkulku
Kun luot ja lähetät aika- tai kulutapahtuman, järjestelmä luo hyväksymismerkinnän. Projektin hyväksyjä tai esimies tarkistaa ja hyväksyy merkinnän. Jos merkintä liittyy projektiin, todelliset arvot luodaan, kun se on hyväksytty. Tämä sallii kustannusten ja laskutuksen seurannan. 

## <a name="approve-an-entry"></a>Merkinnän hyväksyminen
**Hyväksynnät** -lomakkeen avulla voit siirtyä eri näkymien välillä niin, että voit tarkastella eri hyväksyntöjen tyyppejä.
  
1. Siirry **Hyväksynnät** -lomakkeeseen ja valitse **Kulut** , **Aika** tai **Peruutukset**.
2. Tarkista kukin hyväksyntä ja valitse ne, jotka haluat hyväksyä.
3. Hyväksy valitut tapahtumat valitsemalla **Hyväksy**.
Järjestelmä käsittelee nämä merkinnät ja luo toteutuneet arvot tai varauksen.

## <a name="reject-an-entry"></a>Tietueen hylkääminen
Projektin hyväksyjänä sinun täytyy ehkä lähettää tapahtuma uudelleen käyttäjälle korjausta varten.
  
1. Siirry **Hyväksynnät** -lomakkeeseen ja valitse hylättävä tapahtuma. 
2. Valitse **Hylkää**.
3. Valinnainen – Voit lisätä kommentin **Hylkäyksen kommentit** -valintaikkunaan ja ilmoittaa käyttäjälle, miksi merkintä hylätään.
4. Valitse **OK**. Tapahtuma palautetaan käyttäjälle.
  
## <a name="recall-entries"></a>Merkintöjen peruuttaminen
Jossakin vaiheessa on ehkä peruutettava lähetetty tapahtuma. Jos tapahtumaa ei ole hyväksytty, se palautetaan heti. Hyväksytyllä tapahtumalla voi kuitenkin olla merkittävä vaikutus. Projektin hyväksyjän on hyväksyttävä peruutus, jotta tapahtuma voidaan palauttaa toteutuneissa arvoissa.

## <a name="specify-project-approvers"></a>Määritä projektin hyväksyjät
Kullakin projektilla on useita projektiryhmän jäseniä. Voit määrittää, mitkä ryhmän jäsenet ovat myös projektin hyväksyjiä.

1. Siirry **Projektit** -lomakkeeseen ja avaa projekti luettelosta.
2. Valitse **Ryhmä** -välilehdestä ryhmän jäsen, josta tulee projektin hyväksyjä, ja valitse sitten **Muokkaa**.
3. Valitse **Projektin hyväksyjä** -kentässä **Kyllä**.
4. Valitse **Tallenna**.
5. Lisää projektin hyväksyjiä toistamalla vaiheet 2–4.

## <a name="configure-the-users-manager"></a>Käyttäjän esimiehen määrittäminen

1. Valitse **Asetukset** > **Suojaus** > **Käyttäjät**.
2. Valitse käyttäjä, jolle delegoit esimiehen, ja valitse **Organisaation tiedot** -alueessa esimies luettelosta. 
3. Valitse **Tallenna**.


