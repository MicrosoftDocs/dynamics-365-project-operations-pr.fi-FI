---
title: Kustannusmallien määrittäminen
description: Tässä aiheessa on tietoja kustannusmallien luomisesta ja käyttämisestä Project Operationsissa.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642719"
---
# <a name="set-up-cost-templates"></a>Kustannusmallien määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Tässä aiheessa on tietoja kustannusmallien luomisesta ja käyttämisestä Project Operationsissa. Kustannusmalli määrittää seuraavat asiat:

- Projektiluokat ennusteiden ja todellisten arvojen tapahtumille, jotka sisällytetään projektin valmistumisasteprosentin laskelmiin. Valmistumisprosentin arvoa käytetään sen jälkeen sen laskemiseen, kuinka paljon tuottoa kirjataan.
- Voidaanko valmistumisprosenttia muokata, jos se lasketaan automaattisesti.
- Lasketaanko valmistumisprosentti määrien vai yksiköiden perusteella.

## <a name="cost-template-example"></a>Kustannusmalliesimerkki

Työskentelet asiakkaalle verkkosivuston suunnitteluprojektissa, josta peritään kiinteä hinta, 10 000 USD. Ennustat, että projektin valmistuminen kestää 100 tuntia (5 000 USD). Voit myös ennustaa kaksi lentolippua ja neljä yötä hotellissa asiakkaan luo tapahtuvia matkoja varten (1 800 USD). Tuloksena on 6 800 USD suuruiset ennustetut kokonaiskustannukset.

Kun suoritat kiinteähintaisten tuottojen kirjaamisprosessin ja luot arvion kuukauden lopussa, olet työskennellyt 35 tuntia projektissa. Tämä ei vielä sisällä lentoja tai hotellikuluja. Avustaja on myös suorittanut projektissa viisi tuntia tutkimusta hintaan 100 USD, mitä et ollut suunnitellut.

Kun lasket tämän projektin valmistumisprosentin arvon, voit tehdä seuraavat valinnat:

- Haluatko sisällyttää kaikki kustannukset (tunnit ja kulut) vai ainoastaan tunnit?
- Haluatko sisällyttää kaikki tunnit vai ainoastaan suunnitellut tunnit?
- Haluatko laskea valmistumisprosentin suunniteltujen tuntien dollarimääräisiin kustannuksiin (5 000 USD) perustuen vai ainoastaan tuntien (100) perusteella?

Näihin kysymyksiin annetut vastaukset määrittävät kustannusmallin valintasi ja kustannusmallin riveillä valitsemasi luokat.

Seuraavassa taulukossa on esitetty eri menetelmien tulokset, jotka kuvaavat tämän skenaarion valmistumisprosentin arvon laskemista.

| Valmistumisperuste | Dollarikustannukset tai yksiköt | Prosenttia valmiina | Laskenta |
| --- | --- | --- | --- |
| Kaikki tunnit, ei kuluja | Dollarikustannukset | 37 % 35 x 50 USD + 100 USD = 1 850 USD 1 850 USD/5 000 USD |
| Kaikki tunnit, ei kuluja | Yksiköt | 40 % | 40 tuntia / 100 tuntia (mukaan lukien viisi suunnittelematonta tuntia) |
| Suunnitellut tunnit, ei kuluja | Dollarikustannukset tai yksikkö | 35 % | 35/100 tuntia tai 35 x 50 USD/5 000 |
| Kaikki tunnit ja kulut | Dollarikustannukset | 27,2 % | 1 850 USD / 6 800 USD |

Kustannusmallin luomiseen liittyvän lähestymistavan määrittäminen voi riippua useista seikoista:

- Suunnittelemattomien tuntien lisääminen kustannusmalliin johtaa riskiin, että 100 prosentin valmistumisprosentti saavutetaan ennen projektin päättymistä. Tämä johtuu siitä, että todelliset tunnit ovat suunniteltua tunteja suuremmat. Jos käytät jompaakumpaa taulukossa mainituista kahdesta ensimmäisestä menetelmästä, suunnitelmaa on muutettava (ennustetut yksiköt), kun poikkeamat ovat selvillä. Tässä tapauksessa voit lisätä tai vähentää tunteja sen perusteella, mitä projektin valmistumiseen tietojesi mukaan tarvitaan. Jos projektiin tarvitaan vielä 65 tuntia lisää, suunnitelmaan lisätään viisi tuntia, yhteensä 105. Jos tiedät, että avustajasi suorittaa vielä viisi tuntia tutkimusta, kokonaissummasta tulee 110 tuntia.
- Jos käytät taulukon kolmatta menetelmää, päivität suunnitellut tunnit vain omaa aikaasi varten, jotta valmistumisprosentti lasketaan tarkasti. Kannattavuus muuttuu, kun suunnittelemattomat tunnit kirjataan, mutta pysyt edelleen tunnetulla valmistumisprosenttiradalla.
- Jos käytössä on taulukossa mainittu neljäs menetelmä, vaarana on, että kulut tapahtuvat epäsäännöllisesti, eivätkä välttämättä näy valmistumisasteessa. Jos siis kulut sisällytetään, ne voivat aiheuttaa sen, että valmistumisprosentti vaihtelee enemmän kuin on toivottavaa. Jos esimerkiksi et ole vielä lentänyt, valmistumisprosentti oli 27 prosenttia eikä 35 prosenttia tai 37 prosenttia, jos laskentaperusteena käytettiin vain aikaa. Jos olet tehnyt yhden kahden yön matkan ja ennustanut lento- ja hotellikustannuksesi oikein, valmistumisprosentti olisi ollut 40,4 prosenttia (1850 USD työtä ja 900 USD kuluja = 2750 USD /6800 USD = 40,4 prosenttia). Näin ollen kustannukset vain yhdeltä lentomatkalta muuttaisivat valmistumisprosentin 27 prosentista 40 prosenttiin.

## <a name="create-cost-templates"></a>Kustannusmallien luominen
Luo kustannusmalleja suorittamalla seuraavat vaiheet:

1. Siirry kustannusmalleihin Dynamics 365 Finance -ympäristön kohdassa **Projektinhallinta ja kirjanpito** > **Asetukset** > **Arviot** > **Kustannusmalli**.
2. Valitse **Uusi** luodaksesi kustannusmallin. Syötä nimi ja kuvaus.
3. Anna kustannusrivin tunnus kullekin tapahtumatyypille.
4. Valitse oletusvalmistumistapa:

  - **Automaattinen**: Valmistumisprosentti lasketaan automaattisesti projektiin. Tuloksena olevaa arvoa ei voi muuttaa.
  - **Manuaalinen**: Valmistumisprosentti lasketaan automaattisesti projektiin. Tuloksena olevaa arvoa voi muuttaa.

  > [!NOTE]
  > Valmistumisprosentti manuaalista laskentaa varten on kohdassa **Manuaalinen laskenta** **Yleiset**-välilehdellä **Arviot**-sivulla.

5. Valitse yksi seuraavista arvoista kohdassa **Valmistumisperuste**:

  - **Summa**: Kirjanpitovaluuttana oleva summa laskee valmistumisprosentin.
  - **Yksikkö**: Määrä laskee valmistumisprosentin.
  - **Suora viiva** : Järjestelmä laskee valmistumisprosentin suhteellisesti käyttämällä projektin alkamis- ja päättymispäiviä projektin pituuden määrittämiseksi.

6. Valitsemalla **Kustannusrivit** voit tarkastella kustannusmallin kustannusrivejä. Jokaiselle tapahtumatyypille vaaditaan vähintään yksi kustannusrivi. Voit kuitenkin luoda useita kustannusrivejä samoille tapahtumatyypeille ja määrittää näille riveille halutut määritteet.
7. Valitse **Luokat**-välilehdellä projektiluokat, jotka sisällytetään kustannusmalliriville.
8. Valitse **Yleiset**-välilehdelle, sisällytetäänkö tämä rivi valmistumisprosentin laskentaan.
9. Valitse valmistumisprosentin laskennassa käytettävä valmistumiskustannusmenetelmä.
