---
title: Projektien ja tehtävien yhdistäminen projektipohjaiselle tarjousriville
description: Tässä aiheessa on tietoja siitä, miten projektit ja tehtävät yhdistetään projektipohjaiseen tehtäväriviin.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075240"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Projektien ja tehtävien yhdistäminen projektipohjaiselle tarjousriville

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektipohjaisilla tarjousriveillä voit yhdistää tiettyihin tehtäviin projektissa, joka on jo liitetty tarjousriviin.

Kun yhdistät tehtäviä tarjousriviin, seuraavat tarjousrivillä määritetyt kohteet koskevat vain kyseisiä tehtäviä:

- Laskutustapa
- Veloitusasetukset
- Ei-ylitettävät rajoitukset
- Asiakkaat

Sinulla voi olla esimerkiksi projekti, jossa yksi vaihe on kiinteähintainen ja kaikki muut vaiheet ovat aika- ja materiaalipohjaisia. Tässä tapauksessa voit liittää ensimmäisen vaiheen ja kaikki sen alitehtävät kyseisen vaiheen tarjousriviin kiinteähintaisella laskutusmenetelmällä. Tämän jälkeen voit liittää kaikki muut vaiheet aika- ja materiaaliperusteiseen tarjousriviin.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Tehtävien liittäminen projektipohjaisiin tarjousriveihin

Voit liittää tehtäviä tarjousriveihin seuraavista sijainneista:

- **Projekti** -sivu > **Tehtävän laskutus** -välilehti (optimaalinen)
- **Tarjousrivi** -sivu > **Veloitettavat tehtävät** -välilehti 

### <a name="from-the-project-page"></a>Projekti-sivulta

**Projekti** -sivulla on optimaalinen kokemus tehtävien liittämiseksi tarjousriveihin. Tämän sivun avulla voit valita useita tehtäviä ja liittää valittuun tarjousriviin kaikki ne sekä niiden alitehtävät.

1. Tarkista projektipohjaisen tarjous rivin **Yleiset** -välilehdestä, että **Projekti** -kenttä on täytetty.
2. Valitse **Sisällytettävät tehtävät** -kentässä **Vain valitut tehtävät**.
3. Tallenna projektipohjainen tarjousrivi. Kun lomake päivittyy, näkyviin tulee **Veloitettavat tehtävät** -välilehti.
4. Valitse **Yleiset** -välilehdessä projektin linkki **Projekti** -kentästä.
5. Valitse **Projekti** -sivulla **Tehtävän laskutus** -välilehti.
6. Valitse toisesta ruudukosta (joka koskee tehtäväkohtaisia laskutusasetuksia) vähintään yksi tehtävä ja valitse sitten **Liitä tarjousrivit**.
7. Valitse näkyviin tulevassa valintaikkunassa tarjousrivi, joka näyttää tarjouksen projektipohjaiset tarjousrivit.
8. Ilmaise **Laskutustyyppi** -kentässä, ovatko nämä tehtävät veloitettavissa vai ei-laskutettavia.
9. Valitse valintaruutu, jos haluat määrittää, sisällytetäänkö liitokseen valittujen tehtävien alitehtävät. Kun valintaruutu on valittuna, valittujen tehtävien alitehtävät yhdistetään tarjousriville.
10. Sulje valintaikkuna valitsemalla **OK**.

### <a name="from-the-quote-line-page"></a>Tarjousrivi-sivulta

Voit liittää projektitehtävät tarjousriveihin **Tarjousrivi** -sivun **Veloitettavat rivit** -välilehdestä.

>[!NOTE]
>Optimaalinen paikka liittää projektitehtävät tarjousriveihin on **Projekti** -sivun **Tehtävän laskutus** -välilehdessä. Jos liität tehtäviä **Tarjousrivi** -sivun **Veloitettavat tehtävät** -välilehdessa, kukin projekti täytyy liittää manuaalisesti.

1. Tarkista projektipohjaisen tarjous rivin **Yleiset** -välilehdestä, että **Projekti** -kentässä on valittu projekti.
2. Valitse **Sisällytettävät tehtävät** -kentässä **Vain valitut tehtävät**.
3. Tallenna projektipohjainen tarjousrivi. Kun lomake päivittyy, näkyviin tulee **Veloitettavat tehtävät** -välilehti.
4. Valitse **Veloitettavat tehtävät** -välilehdessä **Lisää tarjousrivin tehtävä**.
5. Valitse **Tarjousrivin tehtävä** - sivun **Tehtävät** -kentässä tehtävä ja valitse sitten **Laskutustyyppi** -kentässä **Tallenna**. 
6. Sulje sivu. Valittu tehtävä liitetään nyt tarjousriviin.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Tehtävien liitoksen poistaminen projektipohjaisista tarjousriveistä

### <a name="from-the-project-page"></a>Projekti-sivulta

Tämä menetelmä on optimaalinen kokemus tehtävien liitoksen poistamisesta tarjousriveistä. Tämän sivun avulla voit valita useita tehtäviä sekä niiden alitehtävät ja poistaa liitoksen valitusta tarjousrivistä.

1. Valitse projektipohjaisen tarjousrivin **Yleiset** -välilehdestä, että **Projekti** -kentässä projektin linkki.
2. Valitse **Projekti** -sivulla **Tehtävän laskutus** -välilehti.
3. Valitse toisesta ruudukosta (joka koskee tehtäväkohtaisia laskutusasetuksia) vähintään yksi tehtävä ja valitse sitten **Poista tarjousrivien liitos**.
4. Valitse näkyviin tulevassa valintaikkunassa tarjousrivi.
5. Valitse valintaruutu, jos haluat määrittää, poistetaanko liitos myös valittujen tehtävien alitehtävistä. Kun valintaruutu on valittuna, valittujen tehtävien alitehtävien liitos poistetaan tarjousrivistä.
6. Valitse **OK**. Varoitussanoma ilmoittaa, että jos poistat tämän liitoksen, tehtävään aiemmin tallennetut toteutuneet arvot voidaan palauttaa. 
7. Valitse **OK** , jos haluat jatkaa ja poistaa tehtävän ja projektipohjaisen tarjousrivin välisen liitoksen.

### <a name="from-the-quote-line-page"></a>Tarjousrivi-sivulta

Voit myös poistaa projektitehtävien liitoksen tarjousriveistä **Tarjousrivi** -sivun **Veloitettavat rivit** -välilehdestä.

1. Valitse **Veloitettavat tehtävät** -välilehdessä **Poista tarjousrivin tehtävä**.
2. Valitse **OK**. Varoitussanoma ilmoittaa, että jos poistat tämän liitoksen, tehtävään aiemmin tallennetut toteutuneet arvot voidaan palauttaa. 
3. Valitse **OK** , jos haluat jatkaa ja poistaa tehtävän ja projektipohjaisen tarjousrivin välisen liitoksen.

>[!NOTE]
> Tämä toimintosarja ei poista tehtävää projektista. Se poistaa vain tehtävän liitoksen projektipohjaisesta tarjousrivistä.
