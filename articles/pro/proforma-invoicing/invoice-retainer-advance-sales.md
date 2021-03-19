---
title: Ennakkomaksun tai ennakkomaksuun perustuvan maksun laskuttaminen
description: Tässä aiheessa on tietoja siitä, miten pidätyksiä tai ennakoita laskutetaan Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c53e39a8c6fb27deff5e7a05d5cca3a4215466
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274139"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Ennakkomaksun tai ennakon laskuttaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations tukee ennakkomaksuihin perustuvia sopimuksia ja kertaluonteisia ennakoita. Projektisopimuksessa voit kirjata maksuaikataulun tai kertaennakon. Projektisopimustasolla kirjaaminen ei kuitenkaan heti tee pidätystä tai ennakkoa käytettäväksi. Jos haluat käyttää pidätystä tai ennakkomaksua laskulle, joka tosiasiassa laskuttaa asiakasta, pidätyksen tai ennakon on oltava ensin laskutettuna.

Pidätyksen tai ennakon laskutus tapahtuu suorittamalla seuraavat vaiheet.

1. Valitse **myynti** > **laskutus** > **pidätykset ja ennakot**. 
2. **Valitse ennakot ja pidätykset** -sivulla suodattimesta tietty pidätys tai ennakkomaksu ja merkitse se **valmiiksi laskutettavaksi**.
3. Luo lasku joko manuaalisesti **Projektisopimus**-luettelosta tai tietosivulta. Pidätyksen tai ennakon esitys näkyy **lasku**-sivun **ennakko ja pidätys** -osassa.
4. Vahvista lasku. Tämä tekee pidätyksen tai ennakon käytettäväksi. Voit tarkistaa laskun **pidätykset ja ennakot** -luettelosivulla. Jos kyseessä on laskutettu ennakko tai pidätys, käytettävissä oleva summa näkyy ruudukossa.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Pidätyksen tai ennakon luominen laskun ruudukosta

Voit luoda pidätyksen tai ennakon suoraan laskuun.

1. Jos haluat luoda uuden **pidätyksen tai ennakon**, valitse laskun ennakkomaksut ja lisäasetukset -aliruudukossa **uusi**. 
2. Lisää tarvittavat tiedot **Pikaluonti**-sivulla ja valitse sitten **Tallenna**. Pidätys tai ennakkomaksu luodaan laskuun liittyvässä projektisopimuksessa. Pidätys tai ennakko merkitään automaattisesti **valmiiksi laskutettavaksi** ja lisätään sitten **Laskut**-sivun **Ennakot ja pidätykset** -aliruudukkoon.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Yhdistä laskutettu pidätys tai ennakko

Kun pidätys tai ennakko on laskutettu, sitä voidaan käyttää tai täsmäyttää laskuun ajan, kulujen, välitavoitteiden tai muiden projektipohjaisten kulujen perusteella. Asiakas näkee laskunsa laskun summalla, jota vähennetään laskussa käytetyn pidätyksen tai ennakon perusteella.

Kun projektisopimukselle, jolle on laskutettu pidätykset tai ennakot, luodaan lasku, projektitoiminto ottaa automaattisesti käyttöön laskun pidätyksen tai ennakon.

Tämän voi nähdä **Kohdistetut pidätykset ja ennakot** -ruudukossa **lasku**-sivulla. Seuraavassa taulukossa on tietoja **Projektilasku**-sivun **Käytössä olevat pidätykset ja ennakot** -ruudukon kentistä.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Kuvaus | **Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku**-sivulla |Tässä vain luku -kentässä on tässä laskussa käytetyn maksun tai ennakon kuvaus. Tätä arvoa ei voi muuttaa laskussa. Tämä arvo voidaan päivittää **projektisopimus**-sivun aliruudukossa. | Tämä kenttä voidaan näyttää asiakkaalle tulostetussa laskussa, joka ilmaisee, mitä pidätystä tai ennakkoa käytetään laskussa. |
| Toimituspäivä | **Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku**-sivulla  | Tässä vain luku -kentässä on tässä laskussa käytetyn pidätyksen tai ennakon laskupäivämäärä. Tätä arvoa ei voi muuttaa laskussa. Tämä arvo voidaan päivittää **projektisopimus**-sivun aliruudukossa. | Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan päivämäärä, jolloin pidätys tai ennakko laskutettiin ensimmäisen kerran asiakkaalta. |
| Summa | **Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku**-sivulla  | Tässä vain luku -kentässä on tässä laskussa käytetyn pidätyksen tai ennakon määrä. Tätä arvoa ei voi muuttaa laskussa. Tämä arvo voidaan päivittää **projektisopimus**-sivun aliruudukossa. | Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan pidätyksen tai ennakon alkuperäinen määrä, jonka asiakas maksoi. |
| Käytetty summa | **Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku**-sivulla  | Tässä vain luku -kentässä on laskettu arvo, joka sisältää yhteenvedon siitä, kuinka paljon ennakkomaksua on käytetty. | Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan pidätyksen tai ennakon määrä, joka on jo käytetty. |
| Koko summa | **Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku**-sivulla  | Tässä muokattavassa kentässä on tässä projektilaskussa käytössä oleva pidätyksen tai ennakon määrä. Tämä summa ei voi olla suurempi kuin se, joka on käytettävissä etukäteen. Järjestelmä laskee tämän automaattisesti ruudukon **summa**- ja **käytetty summa** -kenttien erotuksena. Voit pienentää tätä määrää, jos haluat käyttää vähemmän kuin mitä on käytettävissä, mutta et voi kasvattaa määrää, joka käyttää enemmän kuin mitä on käytettävissä. | Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan pidätyksen tai ennakon määrä, joka on jo käytössä laskussa. |
| Saldon ennakkomaksusumma. | **Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku**-sivulla  | Tämä vain luku -kenttä sisältää arvon siitä, kuinka paljon maksun pidätystä tai ennakkoa jää laskun vahvistuksen jälkeen. | Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan summa, joka jää jäljelle tästä pidätyksestä tai ennakosta laskun vahvistamisen ja maksamisen jälkeen. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]