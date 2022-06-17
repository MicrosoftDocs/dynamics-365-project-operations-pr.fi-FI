---
title: Project Operationsin liiketoimintatapahtumat
description: Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Project Operationsin liiketoimintatapahtumista.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923276"
---
# <a name="business-transactions-in-project-operations"></a>Project Operationsin liiketoimintatapahtumat

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsissa *liiketoimintatapahtuma* on abstrakti konsepti, jota ei edusta mikään entiteetti. Jotkut entiteettien yhteiset kentät ja prosessit kuitenkin käyttävät liiketoimintatapahtumien konseptia. Seuraavat entiteetit käyttävät tätä abstraktia konseptia:

- Tarjousrivin tiedot
- Sopimusrivin tiedot
- Arviorivit
- Kirjauskansion rivit
- Todelliset arvot

Näistä entiteeteistä Tarjousrivin tiedot, Sopimusrivin tiedot ja Arviorivit yhdistetään projektin elinkaaren *arviointivaiheeseen*. Kirjauskansiorivit ja Todellisten arvojen entiteetit yhdistetään projektin elinkaaren *suoritusvaiheeseen*.

Project Operations käsittelee kaikkien näiden viiden entiteetin tietueita liiketoimintatapahtumina. Ainoana erona on, että arviointivaiheeseen yhdistettävien entiteettien (Tarjousrivin tiedot, Sopimusrivin tiedot ja Arviorivit) tietueet katsotaan *talousennusteiksi*, kun taas suoritusvaiheeseen yhdistettävien entiteettien (Kirjauskansiorivit ja Todelliset arvot) tietueet katsotaan *taloudellisiksi tosiasioiksi*, jotka ovat jo todelliset.

Lisätietoja on aiheissa [Arviot](../project-management/estimating-projects-overview.md) ja [todelliset arvot.](actuals-overview.md)

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konseptit, joita käytetään vain liiketoimintatapahtumissa

Seuraavia konsepteja käytetään vain liiketoimintatapahtumien konseptissa:

- Tapahtumatyyppi
- Tapahtumaluokka
- Tapahtuman alkuperä
- Tapahtuman yhteys

### <a name="transaction-type"></a>Tapahtumatyyppi

Tapahtumatyyppi edustaa projektiin kohdistuvan taloudellisen vaikutuksen ajoitusta ja kontekstia. Sen määrittää asetusjoukko, jolla on Project Operationsissa seuraavat tuetut arvot:

- Kustannus
- Projektisopimus
- Laskuttamaton myynti
- Laskutettu myynti
- Organisaatioiden välinen myynti
- Resursointiyksikön kustannus

### <a name="transaction-class"></a>Tapahtumaluokka

Tapahtumaluokka edustaa erilaisia kustannustyyppejä, joita projekteissa esiintyy. Sen määrittää asetusjoukko, jolla on Project Operationsissa seuraavat tuetut arvot:

- Aika
- Kulu
- Materiaali
- Maksu
- Välitavoite
- Vero

> [!NOTE]
> Liiketoimintalogiikka käyttää arvoa **Välitavoite** yleensä kiinteähintaiseen laskutukseen Project Operationsissa.

### <a name="transaction-origin"></a>Tapahtuman alkuperä

Tapahtumien alkuperä on entiteetti, joka tallentaa kunkin liiketoimintatapahtuman alkuperän, mikä helpottaa raportointia ja jäljitettävyyttä. Kun projektin toteuttaminen alkaa, jokainen liiketoimintatapahtuma luo toisen liiketoimintatapahtuman, joka puolestaan luo toisen liiketoimintatapahtuman ja niin edelleen.

### <a name="transaction-connection"></a>Tapahtuman yhteys

Tapahtuman yhteys on entiteetti, joka tallentaa kahden samankaltaisen liiketoimintatapahtuman välisen suhteen. Tällaisia ovat esimerkiksi kustannukset ja niihin liittyvät myynnin todelliset arvot tai tapahtumien palautukset, jotka perustuvat laskutustoimiin, kuten laskujen vahvistamiseen tai laskujen korjaamiseen.

Yhdessä entiteetit Tapahtuman alkuperä ja Tapahtuman yhteys auttavat liiketoimintatapahtumien välisten suhteiden ja tietyn liiketoimintatapahtuman luomiseen johtavien toimien seuraamisessa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
