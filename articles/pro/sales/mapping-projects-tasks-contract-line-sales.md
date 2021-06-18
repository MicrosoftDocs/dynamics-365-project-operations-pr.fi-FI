---
title: Projektien ja tehtävien yhdistäminen projektipohjaiselle sopimusriville – lite
description: Tässä aiheessa on tietoja projektien ja tehtävien lisäämisestä sopimusriville ja niiden poistamisesta sopimusriviltä.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b86e03192625b0dabb89080f2ade1ed9e3567cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994628"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Projektien ja tehtävien yhdistäminen projektipohjaiselle sopimusriville 

_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

Projektipohjaisilla sopimusriveillä tietyt projektin tehtävät yhdistetään projektin sopimusriville.

Kun tietyt tehtävät yhdistetään sopimusriville, laskutustapa, veloitettavuusvaihtoehdot, ei-ylitettävät rajoitukset ja sopimusriville määritetyt asiakkaat koskevat vain kyseisiä tehtäviä.

Jos käytössä on skenaario, jossa projektin yhdessä vaiheessa, esimerkiksi prototyyppivaiheessa, on kiinteä hinta ja kaikissa muissa vaiheessa laskutustapana on aika ja materiaali, prototyyppivaihe ja kaikki liitetyt alitehtävät voivat liittää kyseisen vaiheen sopimusriville käyttämällä laskutustapana kiinteää hintaa.

Kaikki muut projektin työrakenteen vaiheet voidaan liittää aika- ja materiaalipohjaiselle sopimusriville.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Tehtävien liittäminen projektipohjaisille sopimusriveille

Tehtäviä voidaan liittää sopimusriveille **Sopimusrivi**-sivun **Veloitettavat tehtävät** -välilehdestä tai **Projekti**-sivun **Tehtävän laskutus** -välilehdestä.

### <a name="from-the-contract-line-page"></a>Sopimusrivi-sivulta

Projektitehtävät voi liittää sopimusriville **Sopimusrivi**-sivun **Veloitettavat tehtävät** -välilehdessä seuraavien ohjeiden mukaisesti.

1. Tarkista projektipohjaisen sopimusrivin **Yleiset**-välilehdessä, että **Projekti**-kenttä on täytetty.
2. Valitse **Sisällytettävät tehtävät** -kentässä **Vain valitut tehtävät**.
3. Tallenna tekemäsi muutokset. Lomake päivittyy ja **Veloitettavat tehtävät** -välilehti on näkyvissä.
4. Valitse ensin **Veloitettavat tehtävät** -välilehti ja sitten aliruudukossa **Lisää sopimusrivin tehtävä**.
5. Valitse **Sopimusrivin tehtävät** -sivun avattavassa **Tehtävät**-luettelossa tehtävä. 
6. Anna tiedot **Laskutustyyppi**-kentän tiedot ja valitse **Tallenna ja sulje**. Valittu tehtävä liitetään sopimusriviin.

> [!NOTE]
> Tämä ei ole optimaalinen tapa liittää projektitehtäviä sopimusriveihin. Jokainen projekti on liitettävä manuaalisesti tällä tavoin toimittaessa. Ensisijainen toimintatapa on käyttää **Projekti**-sivun **Tehtävän laskutus** -välilehdessä.

### <a name="from-the-project-page"></a>Projekti-sivulta

Tämä on optimaalinen tapa liittää tehtäviä sopimusriveihin. Voit valita useita tehtäviä ja liittää ne kaikki alitehtävineen valittuun sopimusriviin. Tehtäviä voi liittää sopimusriviin **Projekti**-sivulla seuraavien ohjeiden mukaisesti.

1. Tarkista projektipohjaisen sopimusrivin **Yleiset**-välilehdessä, että **Projekti**-kenttä on täytetty.
2. Valitse **Sisällytettävät tehtävät** -kentässä **Vain valitut tehtävät**.
3. Tallenna projektipohjainen sopimusrivi. Lomake päivittyy ja **Veloitettavat tehtävät** -välilehti on näkyvissä. Tätä tarvitaan vahvistamista varten.
4. Valitse projektipohjaisen sopimusrivin **Yleiset**-välilehden **Projekti**-kentässä projektin linkki.
5. Valitse **Projekti**-sivulla **Tehtävän laskutuksen asetukset** -välilehti.
6. Ruudukkoja on kaksi. Toinen ruudukko on varattu koko projektissa käytettäville sopimusriveille. Toinen ruudukko on puolestaan varattu tehtäväkohtaisen laskutuksen määrittämistä varten. Valitse toisessa ruudukossa vähintään yksi tehtävä ja valitse sitten **Liitä sopimusrivit**.
7. Valitse sopimusrivi avautuvan valintaikkunan avattavasta luettelosta.
8. Merkitse avattavan **Laskutustyyppi**-luettelon avulla tehtävät veloitettaviksi tai ei-veloitettaviksi.
9. Valitse valintaruutu ilmaisemaan, liitetäänkö myös valittujen tehtävien alitehtävät. Valintaruudun valitseminen liittää valittujen tehtävien alitehtävät sopimusriviin.
10. Sulje valintaikkuna valitsemalla **OK**.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Tehtävien liitoksen poistaminen projektipohjaisia sopimusriveiltä

### <a name="from-the-contract-line-page"></a>Sopimusrivi-sivulta

Projektitehtävien liitokset sopimusriveihin voidaan poistaa **Sopimusrivi**-sivun **Veloitettavat tehtävät** -välilehdessä seuraavien ohjeiden mukaisesti.

1. Valitse **Veloitettavat tehtävät** -välilehdessä **Poista sopimusrivin tehtävä**.
2. Varoitussanoma ilmaisee, että tämän liitoksen poistaminen aiheuttaa tehtävään aiemmin kirjattujen todellisten arvojen palautuksen. Poista tehtävän ja projektipohjaisen sopimusrivin välinen liitos valitsemalla valintaikkunassa **OK**. 

> [!NOTE]
> Tämän tekeminen ei poista tehtävää projektista. Sen sijaan poistetaan tehtävän liitos projektipohjaiseen sopimusriviin.

### <a name="from-the-project-page"></a>Projekti-sivulta

Tämä ei ole optimaalinen tapa poistaa tehtävien liitoksia sopimusriveistä. Voit valita useita tehtäviä sekä poistaa kaikkien tehtävien ja niiden alitehtävien liitokset valittuun sopimusriviin. Tehtävien liitoksen sopimusriviin voi poistaa seuraavien ohjeiden mukaisesti.

1. Valitse projektipohjaisen sopimusrivin **Yleiset**-välilehden **Projekti**-kentässä projektin linkki.
2. Valitse **Projekti**-sivulla **Tehtävän laskutuksen asetukset** -välilehti.
3. Sivulla on kaksi ruudukkoa. Toinen ruudukko on varattu koko projektissa käytettäville sopimusriveille ja toinen tehtäväkohtaisen laskutuksen määrittämistä varten. Valitse toisessa ruudukossa vähintään yksi tehtävä ja valitse sitten **Poista sopimusrivien liitos**.
4. Valitse sopimusrivi avautuvan valintaikkunan avattavasta luettelosta.
5. Valitse valintaruutu ilmaisemaan, poistetaanko liitos myös valittujen tehtävien alitehtävistä. Valintaruudun valitseminen poistaa valittujen tehtävien alitehtävien liitokset sopimusriviltä.
6. Valitse **OK**. Varoitussanoma ilmaisee, että tämän liitoksen poistaminen aiheuttaa tehtävään aiemmin kirjattujen todellisten arvojen palautuksen. Poista tehtävän ja projektipohjaisen sopimusrivin välinen liitos valitsemalla varoitussanomassa **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
