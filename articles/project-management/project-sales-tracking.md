---
title: Projektin myynnin seuranta
description: Tässä aiheessa tietoja siitä, miten Project Operations seuraa työn tuoton edistymistä projektissa.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711041"
---
# <a name="project-sales-tracking"></a>Projektin myynnin seuranta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations seuraa työvoima-arvioita ja tuottoa pienimmällä tarvittavalla rakeisuuden tasolla projektisuunnitelmassa. Työvoiman tuoton arvio perustuu suunniteltuun työmäärään ja yleisiin tai nimetyihin resursseihin, jotka on delegoitu kuhunkin projektisuunnitelman lehtisolmutehtävään. Kun projekti alkaa ja ihmiset alkavat raportoida eri projektitehtävien ajasta, työn toteutuneesta tuotosta tehdään yhteenveto, joka alkaa ennusteiden laskutoimitusten suorittamisesta.

## <a name="labor-revenue-tracking-view"></a>Työvoima tuoton seurannan näkymä

Voit valita **Projektit**-sivun **Seuranta**-välilehdessä **Seuranta** > **Kustannuksett** avataksesi **Kustannusten seuranta** -näkymän. Voit myös valita **Käytä** > **Laskutusprosentti** avataksesi **Tuoton seuranta** -näkymän, joka näyttää työn tuoton jokaiselle tehtävälle projektisuunnitelmassa. Tässä näkymässä myös verrataan tehtävään käytettyä todellista työvoiman tuottoa tehtävän suunniteltuun työvoiman tuottoon. Project Operations käyttää seuraavia kaavoja työvoiman tuoton mittaustietojen laskennassa:

- **Suunniteltu tuotto**: Kaikkien resurssivarausten myynnin arvot kussakin lehtisolmutehtävässä
- **Toteutunut tuotto**: Tehtävään kirjatun ajan kaikkien laskuttamattomien myyntien summa
- **Laskutettava tuotto %**: Toteutunut tuotto ÷ Tuottoarvio valmistumishetkellä
- **Jäljellä oleva tuotto**: Tuottoarvio valmistumishetkellä - Toteutunut tuotto
- **Tuottoarvio valmistumishetkellä**: Jäljellä oleva tuotto + Toteutunut tuotto
- **Tuoton varianssi**: Suunniteltu tuotto - Tuottoarvio valmistumishetkellä


> [!NOTE]
> Project Operations näyttää työvoiman tuoton vain **Projekti**-sivulla **Seuranta**-välilehdessä. Materiaaleja ja kuluja voidaan arvioida ja seurata niiden kulutusta, mutta näitä tuottoja ei sisällytetä **Seuranta**-välilehdellä näkyviin tuottoihin. Tämä välilehti on suunniteltu toimimaan vain työvoiman tuoton uudelleen ennustamisessa työmääräennusteita päivitettäessä.  
> Kaikki näytetut tuottosummat muunnetaan projektin kustannusvaluuttaan. Projektin kustannusvaluutta on projektin sopimusyksikön valuutta. Kiinteähintaisten projektien tuottoluvut **Työvoiman tuoton seuranta** -näkymässä eivät ole merkityksellisiä, koska laskuttamattoman myynnin todellisia arvoja ei tallenneta ajan hyväksynnän yhteydessä.
> Arvioidut ajan myyntiarvot, jotka näkyvät projektin **Arviot**-välitehdessä eivät välttämättä summaudu suunnitellun tuoton arvoksi **Seuranta**-välilehdellä. Tämä ero voi johtua kahdesta mahdollisesta syystä:
><ol>
   ><li> <b>Arviot</b>-välilehdessä näkyy arvioitu tuotto myyntivaluutassa, kun taas <b>Seuranta</b>-välilehdessä näkyy suunniteltu tuotto muunnettuna kustannusvaluuttaan. </li>
   ><li> Kun arvioitu myynti muunnetaan sopimusvaluutaksi <b>Arviot</b>-välilehden mukaan, projektivaluuttaan muunto sisältää vaiheita, jotka voivat aiheuttaa jonkin verran tarkkuuden heikkenemistä: </li>
><ol>
><li> Sopimusvaluutan arvioitu myyntisumma muunnetaan perusvaluutaksi (muunto 1).</li>
><li> Perusvaluutan arvioitu myyntisumma muunnetaan projektikustannusten valuutaksi (muunto 2). </li>
></ol>
></ol>
> Valuutan tarkkuutta käytetään molemmissa vaiheissa, mikä johtaa projektivaluutan arvioidun myyntituottoprosentin poikkeamaan sopimusvaluutan suunnitellusta myynnistä.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Tuoton uudelleen ennustaminen lehtisolmujen tehtävissä

Lehtisolmun tehtävän työvoiman tuottoa ei voi muuntaa suoraan **Seuranta**-välilehdellä **Projekti**-sivulla. **Työmäärän seuranta** -näkymässä voit kuitenkin ennustaa tehtävän jäljellä olevan työmäärän uudelleen. Tämä aiheuttaa tehtävän jäljellä olevan tuoton uudelleenlaskennan. Seuraavassa on kuvaus tämän toiminnasta.

1. Projektipäällikkö voi ennustaa yhteenvetotehtävien työmäärän uudelleen päivittämällä **Läljellä oleva työmäärä** -kentän oletusarvon uudella arviolla tehtävän jäljellä olevasta työmäärästä. Uudelleen arviointi aiheuttaa tehtävän työmäärän arvion (EAC), valmistumisprosentin ja ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien arvio valmistumiseksi (ETC) ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.
2. Järjestelmä laskee jäljellä olevan työtehtävän uuden arvon perusteella jäljellä olevan tuoton **Tuoton seuranta** -näkymään. Jos haluat laskea jäljellä olevan tuoton jäljellä olevan työmäärän perusteella, järjestelmä laskee ensin tehtävän yhden tunnin keskimääräisen työn tuoton yhteenvetotehtävässä suunniteltuna tuottona tai suunniteltuna työmääränä. Suunniteltu tuotto on kaikkien tehtävän resurssivarausten tuottojen summa. Keskimääräisellä tuntituotolla lasketaan tehtävän jäljellä olevan työmäärän jäljellä oleva tuotto.
3. Valmistumishetken tuotto ja tuoton käyttöprosentti lehtisolmun tehtävässä lasketaan uudelleen.
4. Yhteenvetotehtävien valmistumishetken tuoton arvo lasketaan uudelleen aina juurisolmuun asti.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Tuottojen uudelleen ennustaminen yhteenvetotehtävissä

Voit ennustaa yhteenvedon tehtävien tai säilötehtävien työvoiman tuottoa uudelleen. Projektin yhteenvetotehtävän työvoiman tuottoa ei voi kuitenkaan ennustaa uudelleen suoraan **Seuranta**-välilehdellä **Projekti**-sivulla. Samoin kuin solmun solmutehtävät, yhteenveto- ja säilötehtäväien tuoton uudelleen ennustaminen voidaan tehdä **Työmäärän seuranta** -näkymässä. Tässä näkymässä voit ennustaa yhteenvetotehtävän jäljellä olevan työmäärän uudelleen, jolloin yhteenvetotehtävälle jäljellä oleva tuotto lasketaan uudelleen. Seuraavassa on kuvaus tämän toiminnasta.

1. Projektipäällikkö voi ennustaa yhteenvetotehtävien työmäärän uudelleen päivittämällä **Jäljellä oleva työmäärä** -kentän oletusarvon uudella arviolla tehtävän **Jäljellä olevasta** työmäärästä. Uudelleen arviointi aiheuttaa tehtävän työmäärän arvion valmistumishetkellä (EAC), valmistumisprosentin ja ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien EAC, ETC ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.
2. Järjestelmä laskee tehtävän **Jäljellä oleva työmäärä** -kentän uuden arvon perusteella jäljellä olevan tuoton **Tuoton seuranta** -näkymään. Jos haluat laskea jäljellä olevan tuoton jäljellä olevan työmäärän perusteella, järjestelmä laskee ensin tehtävän yhden tunnin keskimääräisen työn tuoton yhteenvetotehtävässä suunniteltuna tuottona tai suunniteltuna työmääränä. Suunniteltu tuotto on kaikkien tehtävän resurssivarausten tuottojen summa. Tällä keskimääräisellä tuntituotolla lasketaan sitten tehtävän jäljellä olevan työmäärän jäljellä oleva tuotto.
3. Valmistumishetken tuoton arvio ja tuoton käyttöprosentit yhteenvetotehtävässä lasketaan uudelleen.
4. Uusi arvioidun tuoton arvo jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen suunniteltu tuotto oli tehtävässä.
5. Jokaisen yksittäisen tehtävän arvioitu valmistumishetken tuotto aina lehtisolmutehtäviin asti lasketaan. Tämän arvon perusteella alitehtävien, lehtisolmuihin asti, jäljellä oleva tuotto ja tuoton käyttöprosentti lasketaan uudelleen valmistumishetken tuoton arvon perusteella. Tuloksena on uusi projektio tehtävän tuoton varianssista. 
6. Yhteenvetotehtävien valmistumishetken tuoton arvo lasketaan uudelleen aina juurisolmuun asti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

