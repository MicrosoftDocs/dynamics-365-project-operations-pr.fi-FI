---
title: Materiaalikäytön kirjaaminen projekteihin ja projektitehtäviin
description: Tässä aiheessa on tietoja siitä, miten materiaalin käyttö kirjataan projekteihin ja projektitehtäviin.
author: rumant
manager: AnnBe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab431ce4c18a4283cd887de9afcba0dd556d2567
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852848"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Materiaalikäytön kirjaaminen projekteihin ja projektitehtäviin

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Projektiryhmä käy läpi projektiin liittyvät tehtävät, ja he kuluttavat tai käyttävät materiaaleja. Materiaalin käyttölokin avulla voidaan kirjata tämä käyttö, jotta projektipäällikkö voi hyväksyä sen ja lopulta laskuttaa sen asiakkaalta. 

Voit kirjata luettelon tai käsin syötettyjen materiaalien käytön ja lähettää ne hyväksyjälle seuraavasti: 

1. Valitse siirtymisruudusta **Materiaalin käyttö** ja valitse sitten **Uusi**.
2. Syötä **Uusi materiaalin käyttö** -sivulla tarvittavat materiaalin käyttötiedot ja valitse sitten **Tallenna**.

Seuraavassa taulukossa on tietoja **Materiaalin käyttöloki** -sivun kentistä. 

| **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- |
| Kuvaus | Tietyn materiaalin käytön kuvaus. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Päivämäärä | Päivämäärä, jona materiaalia on tarkoitus käyttää. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Project | Luettelo aktiivisista projekteista. | Projektin valitseminen materiaalin käyttölokille vaikuttaa **Tehtävä**-kenttään, joka näyttää vain projektissa olevat tehtävät. |
| Tehtävä | Projektin tehtäväluettelo, jossa on yhteenveto ja lehtisolmujen tehtävät. | Kun materiaalin käyttölokille valitaan tehtävä, se vaikuttaa tehtävän todellisiin materiaalikustannuksiin ja todelliseen materiaalimyyntiin. Jos tämä kenttä on tyhjä, vastaavaa materiaalin käytön kustannusta ja myyntiä seurataan ja yhteenveto tehdään vain projektitasolla. |
| Valitse tuote | Määritä, onko tämä arviorivi **Aiemmin luodulle** (luettelon) tuotteelle vai **Käsin lisättävälle** tuotteelle. | Tämä kenttä määrittää tuotetyypin. |
| Tuote | Tuoteluettelon tuotteen tunnus. Kun valitset tuotetunnuksen, **Valitse tuote** -kentän arvoksi päivittyy automaattisesti **Aiemmin luotu** tuote. Tunnuksen avulla haetaan kustannus- ja myyntihinta hinnastosta. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Käsin lisätyn tuotteen kuvaus | Tekstikenttä, johon kirjoitetaan tuotteen nimi. Tämä kenttä on käytössä, kun valitset **Käsin lisättävän** tuotteen **Valitse tuote** -kentässä.| Tämä kenttä ei vaikuta loppupään prosessiin. |
| Varattavissa oleva resurssi| Resurssi, joka käytti tätä materiaalia projektissa. Tämän kentän oletusarvo on kirjautuneen käyttäjän varattavissa oleva resurssi, mutta sitä voidaan muuttaa niin, että se kirjataan projektiryhmän muiden jäsenten puolesta. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikköryhmä | Tämän kentän oletusarvo tulee yksikköryhmästä, joka on määritetty luettelon tuotteen oletusarvoksi. Voit päivittää kentän ja valita toisen yksikköryhmän. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikkö | Tämän kentän oletusarvo on valitun tuotteen oletusyksikkö. Voit päivittää kentän ja valita toisen yksikön. | Jos yksikköä muutetaan, oletusyksikköhinta ja kustannus ovat erilaiset. |
| Määrä | Projektissa tai projektitehtävässä käytetyn tuotteen määrä. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikkökustannus | Valitun tuotteen ja yksikköyhdistelmän yksikkökustannukset, jotka on määritetty soveltuvassa kustannusluettelossa. | Yksikkökustannus näkyy aina projektin kustannusvaluuttana. Jos tuote- ja yksikköasetusten yhdistelmälle ei ole yksikkökustannusta hinnastossa, yksikkökustannuksen oletusarvo on 0,00. |
| Kokonaiskustannukset | Kustannussumma, joka lasketaan määrän \* yksikkökustannuksena.| Yksikkökustannuksen summa näkyy aina projektin kustannusvaluuttana. |


## <a name="submit-material-usage-for-review-and-approval"></a>Materiaalin käytön lähettäminen tarkistettavaksi ja hyväksyttäväksi 
Kun olet siepanut kaiken materiaalin käytön ja olet valmis hyväksymään sen, sinun täytyy lähettää käyttötiedot tarkistettaviksi.

1. Siirry **Materiaalin käyttölokiin** ja valitse vähintään yksi merkintä. Voit myös valita kaikki materiaalin käyttötietueet otsikon valintaruudun avulla.
2. Valitse **Lähetä**. Järjestelmä käsittelee valitut merkinnät ja luo sitten materiaalin käytön hyväksyntäpyynnöt.

## <a name="recall-a-material-usage-log"></a>Palauta materiaalin käyttöloki

Voit tarvittaessa peruuttaa lähetetyn materiaalin käytön. Materiaalin käytön merkinnän peruuttamiseen tarvittava aika määräytyy hyväksyntävaiheen mukaan.  Jos hyväksyjä ei ole vielä hyväksynyt merkintää, peruuttaminen voi tapahtua heti. Jos tapahtuma on kuitenkin jo hyväksytty, hyväksyjää pyydetään hyväksymään peruutus ja peruuttamaan tapahtumat.

1. Siirry kohteeseen **Materiaalin käyttö** ja valitse materiaalin käyttölokien luettelosta peruutettava materiaalin käyttö.
2. Valitse **Peruuta**. Jos materiaalin käyttömerkintää ei ole vielä hyväksytty, järjestelmä peruuttaa sen heti. Jos materiaalimerkintä on jo hyväksytty, ohjelma luo palautuspyynnön, joka ilmoittaa hyväksyjälle, että haluat peruuttaa materiaalin käytön. Hyväksyjä vahvistaa, että palautus voidaan tehdä, ja merkintä palautetaan.

## <a name="delete-a-material-usage-log"></a>Poista materiaalin käyttöloki

Voit poistaa materiaalien käyttölokeja, joita ei ole lähetetty. Jos haluat poistaa jo lähetetyn materiaalin käyttölokin, peruuta se ensin.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
