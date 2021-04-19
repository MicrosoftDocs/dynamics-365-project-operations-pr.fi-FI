---
title: Projektin kustannusten seuranta
description: Tässä aiheessa tietoja siitä, miten Project Operations seuraa edistymistä suhteessa työvoimakustannuksiin ja kuluihin projektissa.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711040"
---
# <a name="labor-cost-tracking-on-projects"></a>Projektien työvoimakustannusten seuranta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations seuraa työvoima-arvioita ja käyttää projektisuunnitelmaan pienintä tarvittavaa rakeisuutta. Työvoimakustannusten taloudellinen arvio perustuu suunniteltuun työmäärään ja yleisiin tai nimetyihin resursseihin, jotka on delegoitu kuhunkin projektisuunnitelman lehtisolmutehtävään. Kun projekti alkaa ja ihmiset alkavat raportoida eri projektitehtävien ajasta, työn todellisesta kulusta tehdään yhteenveto, joka alkaa ennusteiden laskutoimitusten suorittamisesta.

## <a name="labor-cost-tracking-view"></a>Työvoimakustannusten seurannan näkymä

**Projektit**-sivun **Seuranta**-välilehdessä voit valita **Seuranta** > **Kustannukset**, kun haluat avata **Kustannusten seuranta** -näkymän ja tarkastella työvoimakustannusten edistymistä kussakin projektisuunnitelman tehtävässä. Tässä näkymässä myös verrataan tehtävään käytettyä todellista työvoimakustannusta tehtävän suunniteltuun työvoimakustannukseen. Project Operations käyttää seuraavia kaavoja työvoimakustannusten mittaustietojen laskennassa:

- **Suunniteltu kustannus**: Kaikkien resurssivarausten arvioidut kustannukset kussakin solmutehtävässä
- **Toteutunut kustannus**: Tehtävään kirjatun ajan kaikkien toteutuneiden kustannusten summa
- **Kustannuksen käyttöprosentti**: Toteutuneet kustannukset ÷ Kustannusarvio valmistumishetkellä
- **Jäljellä olevat kustannukset**: Kustannusarvio valmistumishetkellä – Toteutuneet kustannukset
- **Kustannukset valmistumishetkellä**: Jäljellä olevat kustannukset + Toteutuneet kustannukset
- **Kustannusten varianssi**: Suunnitellut kustannukset – Kustannusarvio toteutumishetkellä

Kussakin tehtävässä näytetään ennuste tehtävän kustannusten varianssista. Jos kustannusarvio valmistumishetkellä on suurempi kuin suunnitellut kustannukset, tehtävän ennustetaan ylittävän budjetin. Jos kustannusarvio valmistumishetkellä on pienempi kuin suunnitellut kustannukset, tehtävän ennustetaan alittavan budjetin.

>[!NOTE]
> Project Operations näyttää työvoimakustannukset vain **Projekti**-sivulla **Seuranta**-välilehdessä. Materiaaleja ja kuluja voidaan arvioida ja seurata niiden kulutusta, mutta näitä kustannuksia ei sisällytetä **Seuranta**-välilehdellä näkyviin kustannuksiin. Tämä välilehti on suunniteltu toimimaan vain työvoimakustannusten uudelleen ennustamisessa työmääräennusteita päivitettäessä.
Kaikki näytetut kustannussummat muunnetaan projektin kustannusvaluutaksi projektin kustannushinnan valuutasta, jota käytetään kustannushinnan määrittämiseen. Projektin kustannusvaluutta on projektin sopimusyksikön valuutta. Arvioidut kustannusten arvot ajalle, jotka näytetään **Arviot**-välilehdessä **Projekti**-sivulla eivät välttämättä summaudu suunnitelluiksi kustannuksiksi **Seuranta**-välilehdellä. Syy tälle erolle on ero arvioitujen kustannusten yhteenvetotavassa **Arviot** ruudukossa verrattuna suunniteltujen kustannusten laskentaan **Seuranta**-ruudukossa. 
>
> - **Arviot**-välilehti laskee arvioidun kustannuksen käyttämällä hinnastossa samaa kustannusten valuuttaa. Tämän jälkeen hinnastovaluutan arvioitu kustannus muunnetaan projektin kustannusvaluutan arvioiduiksi kustannuksiksi. Projektivaluutan arvioitu kustannus pyöristetään kahteen desimaaliin. Valuutan desimaalien määrä ei ole käytössä tämän muunnoksen aikana. 
> - Suunniteltujen kustannusten laskenta noudattaa **Seuranta**-välilehdessä hieman erilaista laskentajärjestystä, jossa valuutan desimaalien määrä otetaan käyttöön kahdessa vaiheessa: 
   ><ol>
   ><li>Hinnastovaluutan arvioitu kustannussumma muunnetaan perusvaluutaksi (muunto 1).</li>
   ><li>Perusvaluutan arvioitu kustannussumma muunnetaan projektikustannusten valuutaksi (muunto 2). </li>
   ></ol>
   >Valuutan tarkkuutta käytetään molemmissa vaiheissa suunniteltujen kustannusten saamiseksi (**Seuranta**-välilehdessä), mikä poikkeaa hieman arvioiduista kustannuksista (**Aika** - vaiheittain  -näkymässä **Arviot**-välilehdessä). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Kustannusten uudelleen ennustaminen lehtisolmujen tehtävissä

Lehtisolmun tehtävän työvoimakustannuksia ei voi muuntaa suoraan **Seuranta**-välilehdellä **Projekti-sivulla**. **Työmäärän seuranta** -näkymässä voit kuitenkin ennustaa tehtävän jäljellä olevan työmäärän uudelleen. Tämä aiheuttaa tehtävän jäljellä olevan kustannuksen uudelleenlaskennan. Seuraavassa on kuvaus tämän toiminnasta.

1. Projektipäällikkö voi ennustaa yhteenvetotehtävien työmäärän uudelleen päivittämällä **Läljellä oleva työmäärä** -kentän oletusarvon uudella arviolla tehtävän jäljellä olevasta työmäärästä. Uudelleen arviointi aiheuttaa tehtävän työmäärän arvion (EAC), valmistumisprosentin ja ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien arvio valmistumiseksi (ETC) ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.
2. Järjestelmä laskee jäljellä olevan työtehtävän uuden arvon perusteella jäljellä olevan kustannuksen **Kustannusten seuranta** -näkymään. Jos haluat laskea jäljellä olevan kustannuksen jäljellä olevan työmäärän perusteella, järjestelmä laskee ensin tehtävän yhden tunnin keskimääräisen työkustannuksen suunniteltuna kustannuksena tai suunniteltuna työmääränä. Suunniteltu kustannus on kaikkien tehtävän resurssivarausten kustannusten summa. Keskimääräisellä tuntikustannuksella lasketaan tehtävän jäljellä olevan työmäärän jäljellä oleva kustannus.
3. Valmistumishetken kustannukset ja kustannusten käyttöprosentti lehtisolmun tehtävässä lasketaan uudelleen.
4. Yhteenvetotehtävien valmistumishetken kustannusten arvo lasketaan uudelleen aina juurisolmuun asti.

## <a name="reprojecting-costs-on-summary-tasks"></a>Kustannusten uudelleen ennustaminen yhteenvetotehtävissä

Voit ennustaa yhteenvedon tehtävien tai säilötehtävien työvoimakustannuksia uudelleen. Projektin yhteenvetotehtävän työvoimakustannuksia ei voi kuitenkaan ennustaa uudelleen suoraan **Seuranta**-välilehdellä **Projekti**-sivulla. Samoin kuin solmun solmutehtävät, yhteenveto- ja säilötehtäväien tuoton uudelleen ennustaminen voidaan tehdä **Työmäärän seuranta** -näkymässä. Tässä näkymässä voit ennustaa yhteenvetotehtävän jäljellä olevan työmäärän uudelleen, jolloin yhteenvetotehtävälle jäljellä oleva kustannus lasketaan uudelleen. Seuraavassa on kuvaus tämän toiminnasta.

1. Projektipäällikkö voi ennustaa yhteenvetotehtävien työmäärän uudelleen päivittämällä jäljellä olevan työmäärän oletusarvon uudella arviolla tehtävässä. Tämä päivitys aiheuttaa yhteenvetotehtävän valmistumisen ajankohdan arvion (EAC) valmistumisprosentin ja ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien EAC, ETC ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.
2. Järjestelmä laskee jäljellä olevan yhteenvetotehtävän työmäärän uuden arvon perusteella jäljellä olevan kustannuksen **Kustannusten seuranta** -näkymään. Jos haluat laskea jäljellä olevan kustannuksen jäljellä olevan työmäärän perusteella, järjestelmä laskee ensin tehtävän yhden tunnin keskimääräisen työkustannuksen yhteenvetotehtävässä suunniteltuna kustannuksena tai suunniteltuna työmääränä. Keskimääräisellä tuntikustannuksella lasketaan yhteenvetotehtävän jäljellä olevan työmäärän jäljellä oleva kustannus.
3. Valmistumishetken kustannukset ja kustannusten käyttöprosentti yhteenvetotehtävässä lasketaan uudelleen.
4. Uusi valmistumishetken kustannus jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen suunniteltu kustannus oli tehtävässä.
5. Jokaisen yksittäisen tehtävän valmistumishetken kustannus aina lehtisolmutehtäviin asti lasketaan. Tämän arvon perusteella alitehtävien, lehtisolmuihin asti, jäljellä olevat kustannukset ja kustannusten käyttöprosentti lasketaan uudelleen valmistumishetken kustannusten arvon perusteella. Tämän arvon tuloksena on uusi projektio tehtävän kustannusten varianssista. 


**Kustannustehokkuus**-kenttä voidaan määrittää seurantatietojen perusteella. Kun kustannusvarianssi juurisolmulle **Kustannusten seuranta**-näkymässä on negatiivinen, voit asettaa kentän arvoksi **Alle budjetin**. Kun pääsolmun kustannuseron arvo on positiivinen, voit määrittää arvoksi **Yli budjetin**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
