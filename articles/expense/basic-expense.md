---
title: Kulun merkintä (lite)
description: Tässä aiheessa on tietoja siitä, miten voit käsitellä kulumerkintöjä lite-ympäristössä.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e75a61c25be06a9db121e8165e8ccd25d4719d08
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002187"
---
# <a name="expense-entry-lite"></a>Kulun merkintä (lite)

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Basic- tai Lite-kulujen hallinta on mahdollisuus tallentaa yksinkertaisia kuluja. Voit kirjata kuluja projektiin, minkä jälkeen projektin hyväksyjä tarkistaa ne ja hyväksyy ne.

Lisätietoja kuluominaisuuksista Dynamics 365 Project Operationsissa on aiheessa [Kulujen yleiskatsaus](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Peruskulun sieppaaminen

Voit tallentaa kulut, jotta voit lähettää ne hyväksyjälle.

1. Siirry kohtaan **Kulut** ja valitse **Uusi**.
2. Kirjoita **Uusi kulu** -sivulla pakolliset kulutiedot ja valitse sitten **Tallenna**.

## <a name="submit-a-basic-expense"></a>Peruskulun lähettäminen

Kun olet lopettanut kaikkien kulujen tallentamisen ja olet valmis siirtymään hyväksymisvaiheeseen, sinun täytyy lähettää ne.

1. Siirry kohtaan **Kulut** ja valitse kulu. Voit myös valita kaikki kulut käyttämällä otsikon valintaruutua.
2. Valitse **Lähetä**. Järjestelmä käsittelee valitut tapahtumat ja luo sitten kulun hyväksyntäpyynnöt.

## <a name="add-an-attachment"></a>Lisää liite

Sinun on ehkä annettava hyväksyjälle lisäasiakirjoja kuluistasi. Voit liittää kuitin kulutapahtuman aikajanaan. Valitse **Muokkaa** ja sitten **Aikajana**-osassa paperiliitinkuvake kuittisi liittämiseksi.

## <a name="recall-a-basic-expense"></a>Peruskulun peruttaaminen

Kun lähetät kulun vahingossa, voit peruuttaa sen. Kulumerkinnän peruutuksen edellyttämä aika määräytyy sen hyväksyntävaiheen mukaan.  Jos hyväksyjä ei ole vielä hyväksynyt merkintää, peruuttaminen voi tapahtua heti. Jos tapahtuma on kuitenkin jo hyväksytty, hyväksyjää pyydetään hyväksymään peruutus ja peruuttamaan tapahtumat.

1. Siirry kohtaan **Kulut** ja valitse sitten kulujen luettelosta peruutettava kulu.
2. Valitse **Peruuta**. Jos kulumerkintää ei ole vielä hyväksytty, järjestelmä palauttaa sen heti. Jos kulumerkintä on jo hyväksytty, järjestelmä luo palautus pyynnön, joka ilmoittaa hyväksyjälle, että haluat peruuttaa kulun. Hyväksyjä vahvistaa, että palautus voidaan tehdä, ja merkintä palautetaan.

## <a name="delete-a-basic-expense"></a>Peruskulun poistaminen

Kulut, joita ei ole vielä lähetetty, voidaan poistaa. Jos haluat poistaa jo lähetetyn kulun, sinun täytyy ensin peruuttaa se.

## <a name="see-also"></a>Katso myös

- [Hyväksyntöjen yleiskatsaus](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]