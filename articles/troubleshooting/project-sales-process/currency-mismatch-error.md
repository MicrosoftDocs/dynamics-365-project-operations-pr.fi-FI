---
title: Valuutan vastaavuuden virhe
description: Tässä artikkelissa on vianmääritystietoja valuutan vastaavuuden virheestä, joka ilmenee, kun tiettyjä tietuetyyppejä tallennetaan.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914720"
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
