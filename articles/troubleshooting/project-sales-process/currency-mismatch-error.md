---
title: Valuutan vastaavuuden virhe
description: Tässä aiheessa on vianmääritystietoja valuutan vastaavuuden virheestä, joka ilmenee, kun tallennat tiettyjä tietuetyyppejä.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589744"
---
# <a name="currency-mismatch-error"></a>Valuutan vastaavuuden virhe 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun tallennat projektia, sopimusta, tarjousta tai varattavaa resurssia, voit saada virheen: **Omistavan yrityksen valuutta ei vastaa sopimusyksikön valuuttaa. Jatka valitsemalla toinen omistava yritys tai sopimusyksikkö**. Tämä johtuu siitä, että tietueen sopimusyksikön valuutan ja omistavan yrityksen valuutan välillä on valuutan vastaavuuden virhe.


## <a name="resolution"></a>Ratkaisujen määrä

Voit ratkaista ongelman seuraavasti:
- Vahvista tämän tietueen sopimusyksikön valuutta. Näet valuutan avaamalla organisaatioyksikön tietueen ja vahvistamalla arvon **Yleiset**-välilehden **Valuutta**-kentässä.
- Tarkista omistavan yrityksen valuutta. Näet valuutan siirtymällä yrityksen tietueen kohtaan **Liittyvät** > **Kirjaukset**. Kaksoisnapsauta kirjaustietuetta, joka on liitetty yritykseen, ja vahvista arvo **Yleiset**-välilehden **Kirjanpitovaluutta**-kentässä.

Jos valuutat sopimusyksikössä ja kirjaustietueessa eivät vastaa toisiaan, muuta määrityksiä tai valitse eri arvot, kun tallennat tietueen. Järjestelmä edellyttää, että nämä tietueet vastaavat toisiaan, jotta yritysten väliset laskutusvirrat toimivat oikein. Lisätietoja yritysten välisistä määrityksistä löytyy kohdasta [Yritysten välisten tapahtumien luominen](../../project-accounting/create-intercompany-transactions.md).

Jos yritystietueeseen ei ole liitetty kirjaustietuetta, tämä osoittaa, että ympäristön määrityksestä puutuu konfiguraatio. Järjestelmäjärjestelmän on korjattava konfiguraatio. Järjestelmänvalvojan on siirryttävä kohtaan **Kaksoiskirjoituksen määritykset** sekä pysäytettävä ja käynnistettävä uudelleen **Kirjauksien kaksoiskirjoituksen yhdistäminen** kyseisen yhdistämisen alkuperäisen synkronoinnin ja sen edellytysten kanssa. Lisätietoja on ohjeaiheessa [Project Operationsin kaksoiskirjoituksen yhdistämisversiot](../../environment/resource-dual-write-maps.md).
