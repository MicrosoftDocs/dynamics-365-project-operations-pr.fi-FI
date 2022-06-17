---
title: Oikaisukirjauskansioiden luominen ja vahvistaminen
description: Tässä artikkelissa on tietoja oikaisukirjauskansion luomisesta ja vahvistamisesta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928060"
---
# <a name="create-and-confirm-correction-journals"></a>Oikaisukirjauskansioiden luominen ja vahvistaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Aika ajoin aika- tai kulumerkintä voidaan lisätä väärin. Konsultti voi esimerkiksi valita väärän päivämäärän, kun hän luo aikamerkinnän, tai hän voi valita väärän projektin, kun hän syöttää kulun. Jos konsultti ei voi päivittää lähetettyjä merkintöjä, taustakäyttäjä voi korjata projektin toteutuneet tiedot suoraan.

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

7. Kun olet vahvistanut korjauskirjauskansion, palaa projektiin tai projekteihin, jotka päivitit, muutosten tarkastelemista varten.

8. Tarkista projektisivun **Toteutuneet**-välilehden **Toteutuneiden liitetty näkymä** -luettelo. Luettelossa näytetään alkuperäiset ja korjatut merkinnät.


## <a name="correct-approved-material-usage-logs"></a>Hyväksyttyjen materiaalien käyttölokien korjaaminen

Korjaa yksi tai useampi materiaalin käyttölokikirjaus seuraavien vaiheiden mukaisesti.

1. Valitse **Myynti**-alueen vasemmanpuoleisen siirtymisruudun **Tapahtumat**-kohdasta **Toteutuneet**.

2. Valitse **Toteutuneet**-luettelosta sarakesuodattimien avulla **Materiaali**-tapahtumaluokka niin, että vain materiaalien toteutuneet arvot näytetään. Muiden sarakesuodattimien avulla voit rajata edelleen näkyviä toteutuneita arvoja. Kun olet löytänyt haluamasi toteutuneiden arvojen joukon, valitse toteutuneet ja valitse sitten **Korjaa merkinnät**. Uusi korjauskirjauskansio luodaan automaattisesti ja sille määritetään **Materiaalikorjaus**-tyyppi.

3. Kirjoita **Uusi kirjauskansio** -sivun **Kuvaus**-kenttään korjauksen kuvaus. Valitse sitten **Materiaalikorjaus**-välilehden **Materiaalien uudet arvot** -osassa tietokentät, jotka haluat korjata valituille materiaaliriveille. Voit esimerkiksi delegoida materiaalin toiseen projektiin tai korjata tuotteen, materiaalipäivämäärän tai alihankintasopimuksen.

4. Valitse **Esikatselu**. Valitse sitten valintaikkunassa **OK**.

5. Tarkista korjaukset **Kirjauskansiorivit**-välilehdessä. Voit tarkastella luetteloa alkuperäisistä toteutuneista riveistä, jotka liittyvät palautettuihin valittuihin materiaalikirjauksiin ja luotuihin korjattuihin vastaaviin riveihin.

6. Jos korjatut arvot ovat oikein, valitse **Vahvista**. Valitse sitten valintaikkunassa **OK**. Jos arvot eivät ole odotetusti, palaa **Toteutuneet**-luetteloon valitsemalla **Peruuta**. Toista sitten vaiheet 2 –5.

7. Kun olet vahvistanut korjauskirjauskansion, palaa projektiin tai projekteihin, jotka päivitit, muutosten tarkastelemista varten.

8. Tarkista projektisivun **Toteutuneet**-välilehden **Toteutuneiden liitetty näkymä** -luettelo. Luettelossa näytetään alkuperäiset ja korjatut merkinnät.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
