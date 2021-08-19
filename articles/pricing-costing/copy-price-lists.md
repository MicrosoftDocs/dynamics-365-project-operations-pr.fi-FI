---
title: Hinnastojen kopioiminen
description: Tämä aihe tarjoaa tietojen kopioinnista Project Operationsin tuotehinnastoista.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003722"
---
# <a name="copy-price-lists"></a>Hinnastojen kopioiminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Voit luoda kopioita hinnastoista Dynamics 365 Project Operationsissa. Voit esimerkiksi luoda hinnastoja tulevalle vuodelle käyttämällä kuluvan vuoden hinnastoa.  Voit myös kopioida hinnastoista hintaluettelon laskuhinnoista ja myyntihinnoista. 

Jos haluat tehdä kopion hinnastosta, tee seuraavat toimet.

1. Avaa hinnasto, josta haluat tehdä kopion, ja valitse sitten **Kopioi**.
2. Kirjoita kaikki tarvittavat tiedot hinnaston kopioimista varten. Seuraavassa taulukossa on esitetty seikat, jotka kannattaa pitää mielessä tietoja syöttäessäsi.

| Field | Kuvaus | Loppupään vaikutus |
| --- | --- | --- |
| Nimi | Lähdehinnaston nimi, johon on lisätty **kopio**. | Hinnasto sisältää tämän arvon kaikilla luettelosivuilla ja avattavan luettelon vaihtoehdoissa. |
| Konteksti | Kirjoita kohdehinnastoon haluamasi konteksti. | Hinnastoa, jonka kontekstiksi on määritetty **kustannus**, käytetään kustannusarvioiden ja kustannusten todellisten arvojen hinnan etsimistä varten. Hinnastoa, jonka kontekstiksi on määritetty **myynti**, käytetään myyntiarvioiden ja myynnin todellisten arvojen hinnan etsimistä varten. Vain hinnastot, joiden kontekstiksi on määritetty **myynti**, voidaan liittää projektin hinnastoon asiakkaalle, tarjouksille tai sopimukselle. |
| Aloituspäivämäärä | Sen kauden alkamispäivä, jona hinnasto on voimassa. | Yhdessä **päättymispäivän** kanssa tämän kentän avulla määritetään, mitä hinnastoa käytetään tiettyyn arvioon tai todelliseen riviin. |
| Päättymispäivämäärä | Sen kauden loppumispäivä, jona hinnasto on voimassa. | Yhdessä **alkamispäivän** kanssa tämän kentän avulla määritetään, mitä hinnastoa käytetään tiettyyn arvioon tai todelliseen riviin. |
| Valuutta | Lähdehinnaston valuutta. Tämä voidaan kuitenkin muuttaa. | Kun tätä muutetaan, kaikki työn, kulun ja tuoteluettelon nimikkeiden hintarivit muunnetaan kohdehinnaston valuutaksi kopioinnin aikana. |
| Aikayksikkö | Lähdehinnaston valuutta. Tämä voidaan kuitenkin muuttaa. | Kun tätä muutetaan, kaikki tuloksena olevat työnimikkeiden hintarivit muunnetaan kohdehintayksiköksi kopioinnin aikana. Lähteen hinnaston aikayksikön ja kohdehintaluettelon aikayksikön muunnosta käytetään yksikköasetuksista. |
| Kuvaus | Lähdehinnaston kuvaus, johon on lisätty **kopio**. Tämä on tekstikenttä, jonka avulla voit määrittää hinnastosta monirivistä kuvausta. | Tämä kenttä näkyy hinnastossa **liittyvissä** näkymissä eri kohteissa, joissa on toisiinsa liittyviä hinnastoja. |

3. Tallenna hinnasto. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Hinnaston päivittäminen käyttämällä kaikkien hintojen merkintää

1. Hinnankorotuksen voi käyttöön kaikissa aliruudukon hinnoissa valitsemalla hinnaston **Rooli**-, **Luokka**- ja **Hinnaston nimike** -välilehdissä **Päivitä hinnat**. 
2. Kirjoita avautuvaan valintaikkunaan korotus. Voit myös määrittää negatiivisen korotusprosentin, jolloin hinnat laskevat tietyllä prosenttiosuudella. 
3. Valitse valintaruudussa **OK** ja varmista sitten, että aliruudukon hinnat vastaavat tehtyjä muutoksia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]