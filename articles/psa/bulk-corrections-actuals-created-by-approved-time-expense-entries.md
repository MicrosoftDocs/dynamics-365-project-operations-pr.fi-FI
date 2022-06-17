---
title: Hyväksyttyjen aika- ja kulumerkintöjen luomien todellisten arvojen joukkokorjaukset
description: Tässä artikkelissa käsitellään sitä, miten järjestelmänvalvoja voi tehdä yksittäisiä korjauksia tai joukkokorjauksia aiemmin hyväksyttyihin aika- tai kulumerkintöihin, jos laskutus ei ole valmis.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 82c9b38e4c79511fe3b6abfcb973fff8b56f1522
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916285"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Hyväksyttyjen aika- ja kulumerkintöjen luomien todellisten arvojen joukkokorjaukset

[!include [banner](../includes/psa-now-project-operations.md)]

Silloin tällöin aika- tai kulumerkintä saatetaan syöttää virheellisesti. Esimerkiksi konsultti voi valita väärän päivämäärän luodessaan aikamerkintää tai sekoittaa numerot keskenään syöttäessään kulumerkintää. Jos konsultti ei voi tehdä muutoksia lähetettyihin merkintöihin, järjestelmänvalvoja voi korjata projektin merkinnän suoraan.

Tässä artikkelissa kuvattujen toimien suorittaminen edellyttää järjestelmänvalvojan oikeuksia.

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
