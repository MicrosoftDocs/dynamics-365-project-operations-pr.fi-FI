---
title: Hinnastojen määrittäminen
description: Tämä aihe tarjoaa tietoja kulu- ja myyntihintaluetteloiden määrittämisestä.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 227e9a6f0ce6fd3fa1c2b0bd9afa014a3ec4f9758ead0dfb408156535692575c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009482"
---
# <a name="set-up-price-lists"></a>Hinnastojen määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsin hinnastot edustavat hintaluetteloa. Hinnat ilmaisevat kustannus-, myynti- ja laskutushinnat. Hinnastojen konteksti on **myynti** tai **kustannus** sen mukaan, onko hinnasto ilmaissut kustannushinnat vai myynti- ja laskutushinnat.

Seuraavat laajennukset koskevat projektitoimintoja ja niitä käytetään Dynamics 365 Sales -hinnastoissa.

- **Konteksti**: Tässä kentässä on tuetut arvot, **kulut** ja **myynti**. Arvoa **Osto** ei tueta. Voit määrittää **Kulun** tehdäksesi kustannushinnaston tai määrittää kontekstin myyntihinnaston **myyntiä** varten. Kustannushinnastot ratkaisevat kustannustyypin hinnan arvio- ja toteutuneet-tietueissa. Myyntihinnastot ratkaisevat laskutettujen ja laskutettujen myyntityyppien arvioitujen ja todellisten tietueiden hinnan.
- **Aikayksikkö**: Tämä on oletusaikayksikkö, jolle hinta on määritetty tähän hinnastoon liittyvässä **roolien hinta** taulukossa.
- **Hinnastokohde**: Tämä piilotettu kenttä on Project Operationsin tehtävänä erottaa tarjous- tai sopimuskohtaiset hinnastot tavallisista ja maailmanlaajuisesti sovellettavista hinnoista.

## <a name="price-list-header"></a>Hinnaston otsikko

Seuraavassa taulukossa on esitetty niiden hinnastojen **yleiset**-välilehden kentät, jotka ovat yksilöllisiä Project Operationsille tai joilla on merkittäviä muutoksia myyntihinnastoissa.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Nimi | **Yleiset**-välilehti ja **pikaluonti**-lomakkeet | Hinnaston käyttäjätunnus. | Hinnasto näyttää tämän arvon kaikilla luettelosivuilla ja avattavan luettelon vaihtoehdoissa.|
| Konteksti | **Yleiset**-välilehti ja **pikaluonti**-lomakkeet | Tämän kentän arvoksi voidaan määrittää **kustannus** tai **myynti**. | Hinnastoa, jonka arvoksi on määritetty **kustannus**, käytetään kustannusarvioiden ja kustannusten todellisten arvojen hinnan etsimistä varten. Hinnastoa, jonka arvoksi on määritetty **Myynti**, käytetään myyntiarvioiden ja myynnin todellisten arvojen hinnan etsimistä varten. Vain hinnastot, joiden kontekstiksi on määritetty **myynti**, voidaan liittää projektin hinnastoihin asiakkaille, projektitarjouksille tai projektisopimuksille. |
| Aloituspäivämäärä | **Yleiset**-välilehti ja **pikaluonti**-lomakkeet | Sen kauden alkamispäivä, jona hinnasto on voimassa. | **Päättymispäivä**-kentän kanssa tämän kentän avulla määritetään, mitä hinnastoa käytetään tiettyyn arvioon tai todelliseen riviin. |
| Päättymispäivämäärä | **Yleiset**-välilehti ja **pikaluonti**-lomakkeet | Sen kauden loppumispäivä, jona hinnasto on voimassa. | **Alkamispäivä**-kentän kanssa tämän kentän avulla määritetään, mitä hinnastoa käytetään tiettyyn arvioon tai todelliseen riviin. |
| Valuutta | **Yleiset**-välilehti ja **pikaluonti**-lomakkeet | Tämän kentän avulla määritetään oletusvaluutta kullekin tähän hinnastoon liittyvälle roolille, luokalle tai hinnaston nimikeriville. | **Myynti**-hinnastoja, rooleja, luokkia tai hinnaston nimikerivejä ei voi luoda mihinkään muuhun valuuttaan kuin tähän valuuttaan. **Kustannus**-hinnastoissa voit luoda roolihintarivin mihin tahansa valuuttaan. Tässä määritettyä valuuttaa käytetään oletusarvona. Käyttäjäasetukset, jotka liittyvät roolien hintoihin, voivat ohittaa tämän arvon ja ottaa työvoimakustannushinnan asetukset käyttöön missä tahansa valuutassa. Luokan kustannushinnat ja hinnaston nimikekustannukset voidaan määrittää vain tässä määritetyssä valuutassa. |
| Aikayksikkö | **Yleiset**-välilehti ja **pikaluonti**-lomakkeet | Tämän kentän avulla määritetään oletusaikayksikkö kullekin tähän hinnastoon liittyvälle roolille. | Tätä kentän arvoa käytetään vain liittyvien roolien hinta-asetuksissa. **Kustannus**- ja **Myynti**-hinnastoissa voit luoda roolihintarivin mihin tahansa aikayksikköön. Tässä määritettyä aikayksikköä käytetään oletusarvona. Käyttäjäasetuksiin liittyvät roolihinnat voivat ohittaa tämän arvon, jotta työvoimakustannukset ja laskukurssi voidaan määrittää millä tahansa aikayksiköllä. |
| Kuvaus | **Yleiset**-välilehti ja **pikaluonti**-lomakkeet | Tämän tekstikentän avulla voit antaa hinnaston monirivisen kuvauksen. | Tämä kenttä näkyy hinnastossa **liittyvissä** näkymissä eri kohteissa, joissa on toisiinsa liittyviä hinnastoja. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]