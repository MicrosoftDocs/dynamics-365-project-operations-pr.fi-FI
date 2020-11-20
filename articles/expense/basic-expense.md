---
title: Kulun merkintä (lite)
description: Tässä aiheessa on tietoja siitä, miten voit käsitellä kulumerkintöjä lite-ympäristössä.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121079"
---
# <a name="expense-entry-lite"></a>Kulun merkintä (lite)

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Basic- tai Lite-kulujen hallinta on mahdollisuus tallentaa yksinkertaisia kuluja. Voit kirjata kuluja projektiin, minkä jälkeen projektin hyväksyjä tarkistaa ne ja hyväksyy ne.

Lisätietoja Dynamics 365 Project Operationsin kuluominaisuuksista on ohjeaiheessa [kulujen yleiskuvaus](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Peruskulun sieppaaminen

Voit tallentaa kulut, jotta voit lähettää ne hyväksyjälle.

1. Siirry kohtaan **Kulut** ja valitse **Uusi**.
2. Kirjoita **Uusi kulu** -sivulla pakolliset kulutiedot ja valitse sitten **Tallenna**.

## <a name="submit-a-basic-expense"></a>Peruskulun lähettäminen

Kun olet lopettanut kaikkien kulujen tallentamisen ja olet valmis siirtymään hyväksymisvaiheeseen, sinun täytyy lähettää ne.

1. Siirry kohtaan **Kulut** ja valitse kulu. Voit myös valita kaikki kulut käyttämällä otsikon valintaruutua.
2. Valitse **Lähetä**. Järjestelmä käsittelee valitut tapahtumat ja luo sitten kulun hyväksyntäpyynnöt.

## <a name="recall-a-basic-expense"></a>Peruskulun peruttaaminen

Kun lähetät kulun vahingossa, voit peruuttaa sen. Kulumerkinnän peruutuksen edellyttämä aika määräytyy sen hyväksyntävaiheen mukaan.  Jos hyväksyjä ei ole vielä hyväksynyt merkintää, peruuttaminen voi tapahtua heti. Jos tapahtuma on kuitenkin jo hyväksytty, hyväksyjää pyydetään hyväksymään peruutus ja peruuttamaan tapahtumat.

1. Siirry kohtaan **Kulut** ja valitse sitten kulujen luettelosta peruutettava kulu.
2. Valitse **Peruuta**. Jos kulumerkintää ei ole vielä hyväksytty, järjestelmä palauttaa sen heti. Jos kulumerkintä on jo hyväksytty, järjestelmä luo palautus pyynnön, joka ilmoittaa hyväksyjälle, että haluat peruuttaa kulun. Hyväksyjä vahvistaa, että palautus voidaan tehdä, ja merkintä palautetaan.

## <a name="delete-a-basic-expense"></a>Peruskulun poistaminen

Kulut, joita ei ole vielä lähetetty, voidaan poistaa. Jos haluat poistaa jo lähetetyn kulun, sinun täytyy ensin peruuttaa se.

## <a name="see-also"></a>Katso myös

- [Hyväksyntöjen yleiskatsaus](../approvals/approvals-overview.md)
