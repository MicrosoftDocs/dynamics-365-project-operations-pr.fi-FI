---
title: Ulkoinen aikataulutus
description: Tässä artikkelissa on tietoja ulkoisesta aikataulutuksesta.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736960"
---
# <a name="external-scheduling"></a>Ulkoinen aikataulutus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ulkoisen aikataulutustilan avulla voit natiivisti luoda, päivittää ja poistaa entiteettejä, jotka liittyvät työrakenteisiin (WBS), mutta ilman Microsoft Project for the Webin pakottamia nykyisiä rajoituksia. Lisäksi se tarjoaa rajoitetun vahvistuksen. Vain seuraavat asiakkaat voivat käyttää tätä tilaa:

- Asiakkaat, joilla on työkalut, joita tarvitaan Project Operationsin toimittaman aikataulutuslogiikan ulkopuolisen WBS-logiikan määrittämiseen
- Asiakkaat, joiden on hallittava aikatauluhierarkiaa, riippuvuuksia tai tehtävän kestoa

> [!IMPORTANT]
> Tietoja, joita ei ole syötetty oikein WBS:iin liittyviin entiteetteihin, ei ehkä hahmonneta resurssin täsmäytysruudukossa, arvioruudukossa, seurantaruudukossa tai resurssin määritysruudukossa.

## <a name="configuration"></a>Configuration

Tämä ominaisuus on oletusarvoisesti käytössä. Projektien käyttövalmiissa pääsivussa liittyvä kenttä ei ole kuitenkaan oletusarvoisesti näkyvissä. Jos haluat ottaa kentän käyttöön, avaa Maker Portal -portaalissa projektientiteetin pääsivu, valitse **Aikataulutusmoduuli**-kenttä ja muuta kentän arvoksi **Oletusarvoisesti näkyvissä**. Jos et käytä käyttövalmista projektin pääsivua, muokkaa aiemmin luotua sivua ja lisää siihen **Aikataulutusmoduuli**-kenttä.

## <a name="settings"></a>Asetukset

Jos haluat käyttää ulkoista aikataulutustilaa, luo ensin uusi projekti ja valitse **Ulkoisesti ajoitettu** aikataulutusmoduuli projektin pääsivun avattavasta luettelosta. Kun tämä tila on määritetty projektia varten, sitä ei voi muuttaa.

## <a name="viewing-the-wbs"></a>WBS:n tarkasteleminen

Jos projekti on ajoitettu ulkoisesti, käyttöoikeus Project for the Webiin on rajoitettu kyseiseen projektiin. Jotta voit tarkastella WBS:ää, siirry seurantaruudukkoon, jossa koko WBS näytetään.

## <a name="creating-and-editing-the-wbs"></a>WBS:n luominen ja muokkaaminen

Jos projektissa on otettu käyttöön ulkoinen aikataulutus, kaikkien WBS-entiteettien, kuten tehtävien, ryhmän jäsenten, resurssin määritysten ja riippuvuuksien, tiedot on määritettävä.

Seuraavassa kuvassa on projektin suunnittelun tietomalli.

![Projektin suunnittelun tietomalli.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Toiminnalliset rajoitukset

Seuraavat toiminnot eivät ole sallittuja ulkoisesti aikataulutetuissa projekteissa.

### <a name="project-planning"></a>Projektin suunnittelu

- **Kopioi projekti** – tätä toimintoa ei tueta ulkoisesti ajoitettujen projektien yhteydessä.
- **Siirrä projekti** – muutokset projektin aloituspäivään eivät siirrä tehtävien tai resurssivarausten alkamista työrakenteessa.
- **Projektipäällikön päivittäminen** – projektipäällikön muutokset projektin pääsivulla eivät luo uutta projektiryhmän jäsentä automaattisesti, ennen kuin projekti on muunnettu.
- **Projektin työtuntimallin päivittäminen** – projektin työtuntimalliin tehdyt muutokset eivät laske projektin aikataulua uudelleen.
- **Resurssien määrityksen jaksotus** – resurssimääritysten luominen ei päivitä **mdyn\_PlannedWork** -kenttää automaattisesti. Tähän kenttään voidaan tallentaa resurssin määrityksen työmäärän jaksotukset. Jos resurssien määritysruudukossa tai resurssin täsmäytysruudukossa näkyy aikajaksotettu työmäärä, määritä kelvolliset resurssien määrityksen jaksotukset. Nämä jaksotukset on muotoiltava oikein niin, että ne käynnistävät sekä kustannusjaksotukset että myyntihinnan jaksotukset. On suositeltavaa luoda testiprojekti, jonka Project for the Web ajoittaa, ja tarkistaa sitten liittyvät tiedot ja vahvistaa edellytykset ja muotoilun.

### <a name="resource-management"></a>Resurssien hallinta

- **Yleinen resurssien täyttäminen** – yleistä resurssien täyttämistä ei tueta ulkoisesti ajoitettujen projektien osalta. Yritys täyttää aktiiviset avoimet tarpeet luo uusia projektiryhmän jäseniä, mutta se ei poista yleistä ryhmän jäsentä eikä korvaa yleistä ryhmän jäsentä aiemmin luoduissa resurssimäärityksissä.
- **Poista ryhmän jäsen** – Ryhmän jäsenen poistaminen ei poista automaattisesti resurssimäärityksiä.

### <a name="quoting-and-contracting"></a>Tarjouksen ja sopimuksen tekeminen

- **Tarjousrivin ja sopimusrivin tietojen tuominen** – Kun tarjous- tai sopimusrivin tiedot tuodaan projektista, sovellus on testattu tukemaan enintään 500 tehtävää WBA:ssa tehtäväkohtaisen 20 määrityksen raja-arvon perusteella.

### <a name="actuals-and-invoicing"></a>Toteutuneet ja laskutus

- Vaikka WBS:n ja taloushallinnon tapahtumien välillä ei ole muutoksia nykyisiin tarkistuksiin, on tärkeää, että noudatat käyttövalmista tietomallia, jotta kaikki loppuvaiheen tapahtumat suoritetaan odotetulla tavalla.
