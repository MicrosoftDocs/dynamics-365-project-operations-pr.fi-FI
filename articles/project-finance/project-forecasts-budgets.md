---
title: Projektiennusteet ja -budjetit
description: Microsoft Dynamics 365 Finance tarjoaa projektiennusteita ja projektibudjetteja projektien hallintaa ja valvontaa varten.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85a5577968024bf42449c50d72a11414f9207eec
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751200"
---
# <a name="project-forecasts-and-budgets"></a>Projektiennusteet ja -budjetit

[!include [banner](../includes/banner.md)]

Projektinhallintaan on kaksi tapaa: projektiennusteet ja projektibudjetit. 

Voit käyttää projektiennusteita, jos organisaatiollasi on operatiivinen perspektiivi ja jos se keskittyy tuottoihin ja kustannuksiin, jotka johdetaan tietyistä tapahtumista. Käytä projektibudjetointia, jos organisaatiosi keskittyy enemmän rahamääriin. 

Sekä projektiennusteet että projektibudjetit käyttävät ennustemalleja suunniteltujen tapahtumasummien määrittämiseen. 

Kullakin tavalla on etunsa. Ota huomioon seuraavat seikat, ennen kuin valitset menetelmän organisaatiollesi.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Projektin ennustaminen**                  | **Projektin budjetointi**                              |
| **Jaksokohdistus**     | Tapahtumia ei voi kohdistaa eksplisiittisesti kirjanpitokauden ajalle. Sen sijaan ennuste ja ennusteen valvonta perustuvat projektin elinkaareen. Koska ennusteet perustuvat tiettyyn päivämäärään, sinun täytyy päätellä ajanjakso päivämäärän perusteella. | Voit kohdistaa tapahtumia koko projektin tai kirjanpitokauden ajalle. Jos kohdistat jakson ajalle, voit siirtää käyttämättömiä summia seuraavalle kirjanpitokaudelle. |
| **Tapahtumien tarkasteleminen**  | Voit tarkastella tapahtumia ennustelomakkeissa, joissa näet koko yrityksen ja kaikkien projektien ennusteet hierarkiasta riippumatta. Jos haluat keskittyä tiettyyn projektiin, sinun on suodatettava tiedot.                                       | Voit tarkastella yhden projektihierarkian budjetoituja tapahtumia. Siten voit tarkastella pääprojektin tai sen aliprojektien tapahtumatietoja.                 |
| **Tapahtumamuuttujat** | Kun lisäät ennustetapahtumia, voit käyttää kaikkia toteutuneeseen tapahtumaan liittyviä määritteitä. Tämä lisää ennusteen mahdollista yksityiskohtaisuutta. Voit esimerkiksi syöttää tietoja määristä, työntekijöistä, nimikkeistä tai riviominaisuuksista.         | Kun syötät budjettitietoja, voit käyttää vain summia, luokkia ja aktiviteetteja.                    |
| **Suojaus**              | Ennusteet perustuvat tapahtumiin, jotka lisätään ennustelomakkeisiin, eikä niihin liity prosessinvalvonnan mekanismia. Kaikki työntekijät, joilla on käyttöoikeudet ennustelomakkeeseen, voivat tarkistaa tietoja ilman hyväksyntää.                                        | Budjetointi käyttää työnkulkujärjestelmää, mikä mahdollistaa muutoksenhallinnan sekä tarkistushistorian ylläpitämisen.         |
| **Kirjaustyypit**           | Ennustetapahtumien kirjaukset perustuvat yksikköjen määrään sekä kustannuksiin ja myyntiyksikköhintoihin.  | Budjetintiedot perustuvat summiin, jotka jaetaan kustannusten ja tuottojen kesken.                                          |
| **Ennustemallit**       | Koska jokainen ennuste on liitettävä malliin, voit luoda useita ennustemalleja ja määrittää myös alimalleja.           | Projektin budjetointi rajoittaa budjetoinnissa käytettäviä ennustemalleja. Pienempi määrä ennustemalleja voi parantaa ennusteiden yhdenmukaisuutta.                           |
| **Kustannusten ylittyminen**         | Voit vain sallia tai estää sellaisten tapahtumien kirjauksen, joka aiheuttaisi kustannusten ylittymisen.   | Projektin budjetointi tarjoaa käyttäjille lisää ohjausmahdollisuuksia. Voit sallia varoitukset ja ylitykset.                    |
| **Ohjausobjekti**               | Ennustevalvontaa suoritetaan käyttämällä ennusteiden vähentämistä. Todelliset summat vähennetään ennustetapahtumien saldoista ilman kirjausketjua. Tämä voi vaikeuttaa sen jäljittämistä, missä todelliset tapahtumat ovat tapahtuneet.                   | Projektin budjetinvalvonnassa todelliset summat vähennetään jäljellä olevan budjetin summista. Tämä mahdollistaa selkeämmän kirjausketjun.                                   |

## <a name="project-forecasts"></a>Projektiennusteet
Kun käytät projektiennusteita, voit lisätä kullekin tapahtumatyypille ennustetapahtumia ennustelomakkeisiin. Jokaista todellista tapahtumaa varten käytettävissä olevaa määritettä voidaan käyttää ennustetapahtumassa. Esimerkkejä näistä määritteistä ovat rivin kannattavuus, rivimääritteet, työntekijät ja kuvaukset. Voit myös ennustaa, kuinka kauan kulun ilmaantumisesta kestää asiakkaan laskuttamiseen. 

Projektiennusteen tapahtumat perustuvat yksikköihin ja määriin. 

Sinun on yhdistettävä jokainen projektiennuste ennustemalliin. Kun lisäät ennustetapahtuman, järjestelmä ehdottaa automaattisesti ennustemallia. Ennustemalli toimii ennustetapahtumien säilönä. 

Voit määrittää ennustemalleja mallien alimalleiksi. Tämän avulla voit ennustaa alueen, ajanjakson tai osaston mukaan. Voit kopioida ennustetapahtumat malliin, jos haluat luoda uuden mallin, ja voit myös siirtää tapahtumat pääkirjaan. Koska ennusteen ja mallin välillä on yksi-yhteen-suhde, kukin ennustemalli muodostaa projektille erillisen budjetin. 

Ennustemalleissa voi käyttää ennusteen vähentämistä projektien ohjausmekanismina. Ennusteen vähentämisessä toteutuneet tapahtumat vähentävät ennusteen tapahtumasaldoja. Koska ennusteen vähennystä kuitenkin käytetään hierarkian korkeimmassa projektissa, se tarjoaa rajallisen näkymän ennusteen muutoksista. Jos työntekijä on esimerkiksi liitetty aliprojektiin, työntekijän toteutuneet tapahtumat kirjataan pääprojektiin. Tämä voi vaikeuttaa muutosten seuraamista, koska et voi helposti selvittää, mikä tapahtuma missä aliprojektissa aiheutti ennustesumman vähennyksen. Siksi on hyvä luoda ennustemallin kopio käytettäväksi ennusteen vähentämisessä. Raporttien avulla voit tarkastella alun perin ennustettuja tietoja. 

Voit tarkistaa, kopioida, poistaa tai siirtää projektiennusteita pääkirjan budjettiin. Prosessinvalvontaa ei kuitenkaan ole. Kaikki työntekijät, joilla on käyttöoikeus ennustelomakkeeseen, tehdä tarkistuksia ilman arviointia.

-   **Tarkista** – Voit tarkistaa ennustetapahtuma samoissa lomakkeissa, joihin alkuperäiset kirjaukset tehtiin.
-   **Kopioi tai poista** – Kun kopioit ennustetapahtumia, kopioit yhden ennustemallin rivit toiseen ennustemalliin. Kun poistat ennusteen, poistat ennustetapahtumat ennustemallista. Jos haluat rajoittaa kopioitavia tai poistettavia ennustetapahtumia, valitse tietyt tapahtumatyypit ja -päivämäärät. Siten voit kopioida tai poistaa vain tiettyjä ennusteen osia.
-   **Siirto** – Kun siirrät projektiennusteen pääkirjan budjettiin, siirrät ennustemallin ennustetapahtumat pääkirjan budjettiin. Voit korvata kaikki siihen pääkirjaan aiemmin siirretyt tapahtumat, johon siirrät projektiennusteesi.

## <a name="project-budgets"></a>Projektibudjetit
Projektien budjetointi on ennustamista yksinkertaisempaa, vaikka se integroituukin ennustemalleihin. Siinä käytetään yksittäistä kirjauslomaketta alkuperäisiä budjettitietoja ja -tarkistuksia varten ja mahdollistaa ennusteet, jotka perustuvat ainoastaan määrään, luokkaan tai aktiviteettiin. 

Projektin budjetoinnissa kaikki alkuperäiset budjetit ja tarkistukset on lähetettävä hyväksyttäväksi projektityönkulkuun. Työnkulkujen avulla voit hallita prosessia entistä laajemmin ja luoda muutoksia historiatietueeseen. 

Projektin budjetointi muistuttaa pääkirjan budjetointia, mutta sen määrittäminen on nopeampaa ja helpompaa. Monia pääkirjan budjetoinnin asetuksia, kuten numerosarjoja tai valuuttaa, ei tarvitse määrittää erikseen projekteille.

Projektibudjetit liitetään automaattisesti kahteen ennustemalliin, joista toinen on alkuperäiselle budjetille ja toinen jäljellä olevalle budjetille. Siten ennustemalleihin perustuvissa raporteissa voi käyttää budjettitietoja. Kun projektibudjetti on vahvistettu, järjestelmä luo ennustesiirtoja niiden määritettyjen mallien perusteella, joita käytetään raportointi- ja hallintatarkoituksiin.

## <a name="forecast-models"></a>Ennustemallit
Ennustemalleilla on yksikerroksinen hierarkia. Tämä tarkoittaa sitä, että yksi projektiennuste on liitettävä yhteen ennustemalliin.

Jos käytät projektiennustusta, voit määrittää malleja alimalleiksi. Sitten voit luoda malleja osastoittain, aikajaksoittain tai alueittain. Voit esimerkiksi luoda ennustemallin vuodeksi ja luoda sitten alimallit koillisen, kaakon, lounaan ja luoteen alue-ennusteille, jotka aluepäälliköt lähettävät. Valitsemalla eri vaihto ehtoja käytettävissä olevissa raporteissa voit tarkastella tietoja kokonaisennusteen tai alimallin mukaan.



