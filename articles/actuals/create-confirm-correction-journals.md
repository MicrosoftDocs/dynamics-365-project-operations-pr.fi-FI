---
title: Oikaisukirjauskansioiden luominen ja vahvistaminen
description: Tässä aiheessa on tietoja oikaisukirjauskansion luomisesta ja vahvistamisesta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d242741b2070f086bf8d3f1d40a5380c2a0f518
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996652"
---
# <a name="create-and-confirm-correction-journals"></a>Oikaisukirjauskansioiden luominen ja vahvistaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Silloin tällöin aika- tai kulumerkintä saatetaan syöttää virheellisesti. Esimerkiksi konsultti voi valita väärän päivämäärän luodessaan aikamerkintää tai sekoittaa numerot keskenään syöttäessään kulumerkintää. Jos konsultti ei voi tehdä muutoksia lähetettyihin merkintöihin, järjestelmänvalvoja voi korjata projektin merkinnän suoraan.

Tässä aiheessa kuvattujen toimien suorittaminen edellyttää järjestelmänvalvojan oikeuksia.

## <a name="correct-approved-time-entries"></a>Hyväksyttyjen aikamerkintöjen korjaaminen     

Noudata seuraavia ohjeita korjataksesi projektin yksittäisen aikamerkinnän tai useita aikamerkintöjä.

1. Valitse **Myynti**-alueelta **Tapahtumat** ja valitse sitten **Hyväksytty aika**. 

2. Etsi ja valitse **Hyväksytty aika** -luettelosta yksi tai useampi korjattava aikamerkintä. Voit käyttää suodinta löytääksesi asiaankuuluvat merkinnät. Voit suodattaa merkinnät esimerkiksi projektin tunnuksen mukaan ja valita sitten kaikki hyväksytyt aikamerkinnät, joilla on kyseinen projektitunnus.

3. Valitse **Viennin oikaisu**. Uusi oikaisukirjauskansio luodaan automaattisesti tyypillä **Ajan korjaus**. Valitsemasi merkinnät lisätään kirjauskansioon. 

4. Syötä oikaisukirjauskansiolle kuvaus **Uusi kirjauskansio** -sivun **Kuvaus**-kenttään ja valitse sitten **Aikamerkinnän korjaukset** -välilehti.  

5. Päivitä kentät oikeilla tiedoilla tarvittaessa **Aikamerkintöjen uudet arvot** -osiossa. Voit esimerkiksi muuttaa delegoitua projektia tai varattavissa olevaa resurssia.

6. Valitse **Esikatselu**. Valitse valintaikkunasta **OK**. **Kirjauskansion rivit** -välilehdessä näet luettelon alkuperäisistä todellisista arvoista, jotka liittyvät valittuihin palautettuihin aikamerkintöihin, sekä vastaavat luodut korjatut rivit. Jos sinun tarvitsee tehdä lisää korjauksia, toista vaiheet 5 ja 6. 

> [!NOTE]
> Kaikilla korjatuilla todellisilla arvoilla on samat arvot kuin jotka valitsit **Aikamerkintöjen uudet arvot** -osiossa.

7. Jos korjaukset näkyvät odotetulla tavalla, valitse **Vahvista**. Valitse valintaikkunasta **OK**.

8. Palaa **Myynti**-alueelle, valitse **Projektit** ja avaa projekti, jonka aikamerkinnät päivitit juuri. 

9. Tarkasta tekemäsi muutokset **Projektit**-sivun **Todelliset arvot** -välilehdestä. 

> [!NOTE]
> Jos **Todelliset arvot** -välilehti ei ole näkyvissä, valitse **Liittyvät** > **Todelliset arvot**.  

10. **Todellisten arvojen liitetty näkymä** -luettelossa näet, että alkuperäiset palautetut aikamerkinnät ovat edelleen luettelossa vastaavien korjattujen aikamerkintöjen kanssa. 

Esimerkiksi seuraavassa kuva on kaksi nimikettä, joiden määrä on 8,00 ja joilla on veloituksia Summa-sarakkeessa. Lisäksi näet kaksi nimikettä, joiden summa on -8,00 ja joilla on hyvitettyjä summia Summa-sarakkeessa. Nämä korjaukset tuovat määrän nollaan.

 
## <a name="correct-approved-expense-entries"></a>Hyväksyttyjen kulumerkintöjen korjaaminen

Noudata seuraavia ohjeita korjataksesi yhden tai useamman kulumerkinnän. 

1. Valitse **Myynti**-alueen vasemmanpuoleisen siirtymisruudun **Tapahtumat**-osiosta **Hyväksytyt kulut**.

2. Valitse **Hyväksytyt kulut** -luettelosta projekti, jonka haluat korjata, ja valitse sitten **Viennin oikaisu**. Uusi oikaisukirjauskansio luodaan automaattisesti tyypillä **Kulun korjaus**. 

3. Kirjoita korjaukselle kuvaus **Uusi kirjauskansio** -sivun **Kuvaus**-kenttään ja valitse **Kulun korjaus** -välilehden **Kulujen uudet arvot** -osiosta tietokentät, jotka haluat korjata valituille kulujen riveille. Voit esimerkiksi delegoida kulun toiseen **projektiin** tai korjata **Kululuokka**-, **Kulun päivämäärä**- tai **Varattavissa oleva resurssi** -arvot.

4. Valitse **Esikatselu**. Valitse valintaikkunasta **OK**. 

5. Tarkasta korjaukset **Kirjauskansion rivit** -välilehdes. Näet luettelon alkuperäisistä todellisista arvoista, jotka liittyvät valittuihin palautettuihin kulumerkintöihin, sekä vastaavat luodut korjatut rivit.

6. Jos korjatut arvot ovat oikein, valitse **Vahvista**. Valitse valintaikkunasta **OK**. Jos arvot eivät näy odotetulla tavalla, valitse **Peruuta** palataksesi **Hyväksytyt kulut** -luetteloon. Toista vaiheet 2–5. 

> [!NOTE]
> Korjatuilla todellisilla arvoilla on samat arvot kuin jotka valitsit **Kulujen uudet arvot** -osiossa.

7. Kun olet tarkastanut oikaisukirjauskansion, siirry takaisin päivittämääsi projektiin tai projekteihin nähdäksesi muutoksesi.  

8. Tarkista **Todelliset arvot** -välilehdestä **Todellisten arvojen liitetty näkymä** . Luettelossa näytetään alkuperäiset ja korjatut merkinnät. Seuraavassa kuvassa näytetään alkuperäisten kulumerkintöjen summat ja niitä vastaavien korjattujen kulumerkintöjen summat. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]