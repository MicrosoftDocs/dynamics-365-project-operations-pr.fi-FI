---
title: Aikamerkkinnän käyttöliittymän toiminta
description: Tässä aiheessa on tietoja käyttöliittymän toiminnasta aikamerkkinnässä.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8719e2f9ee4867f17ed75142eca2115f61e37999
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124499"
---
# <a name="time-entry-ui-behavior"></a>Aikamerkkinnän käyttöliittymän toiminta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


**Viikoittainen aikamerkintä** -ruudukko on mukautettu ohjausobjekti, jolla on kaksi pääosaa, **Dimensiot** ja **Kesto**.

## <a name="dimensions"></a>Dimensiot
**Dimensiot** -osassa näkyvät ne dimensiot, joihin aikaa voidaan lisätä. Seuraavien dimensioiden tuki on sisäänrakennettu:

  - Project
  - Projektin tehtävä
  - Rooli
  - Laji
  - Merkinnän tila

**Dimensiot** -osa ei salli tekstiin sidottua muokkausta. Tätä osaa tukee näkymä, jonka avulla mukautetut kentät voidaan lisätä viikoittaiseen ajansyöttöruudukkoon.

## <a name="duration"></a>Kesto
Kesto-osassa näkyvät viikonpäivät sarakeotsikoina. Tässä osassa voi muokata tekstiin sidotusti. Kun ajansyöttörivi on luotu ja siinä on tarvittavat dimensiot, käyttäjät voivat nopeasti syöttää sen aikamäärän, jonka he käyttivät näihin dimensioihin.

## <a name="create-a-new-time-entry"></a>Uuden aikamerkinnän luominen

1. Valitse aikamerkinnän ruudukossa **Uusi**. 
2. Valitse **Aikamerkinnän pikaluonti** -valintaikkunassa aikamerkinnän päivämäärä.
3. Kirjoita tiedot dimensioihin **Projekti**, **Projektitehtävä**, **Rooli** ja **Kesto**. Nämä tiedot on lisättävä minuutteina, tunteina tai päivinä kirjoittamalla **h**, **m** tai **d** sekä numero. 
4. Kirjoita aikamerkinnälle kuvaus ja kommentteja, jotka voidaan jakaa ulkoisesti aikamerkintään liittyen. 

Kun tallennat merkinnän, kirjoitetut arvot näkyvät **Dimensiot**-osassa. **Kesto**-kenttään syötetty tieto näkyy päivälle, jota varten aikamerkintä luotiin.

Järjestelmänäkymät tukevat valintakenttiä. Kun käyttäjä on esimerkiksi syöttänyt projektin, **Projektitehtävä**-kenttä asetetaan oletuksena **Kopioi**-näkymään. Jos haluat luoda aikamerkintöjä tehtäville, joita ei ole kohdennettu käyttäjälle, valitse **Vaihda näkymää** -valintaruudussa, ja valitse sen jälkeen **Kaikki aktiiviset projektitehtävät** -näkymä.

## <a name="edit-a-time-entry"></a>Aikamerkinnän muokkaus 
Joidenkin ajansyöttösivun kenttien, kuten **Kuvauksen** ja **Ulkoisten huomautusten**, tietoja ei näytetä viikoittaisessa ajansyöttöruudukossa. Sen sijaan näytetään pieni kolmionmuotoinen osoitin niissä **Kesto**-soluissa, joilla on näitä lisätietoja. 

1. Jos haluat muokata aikamerkintää, valitse päivitettävä solu aikamerkinnässä.
2. Päivitä tiedot **Aikamerkinnän päätiedot** -ruudussa valitsemalla **Muokkaa tietoja**. 

## <a name="copy-a-time-entry-row"></a>Aikamerkintärivin kopioiminen
Kun rivi on luotu, käyttäjät voit valita **Kopioi rivi** -toiminnon kopioidaksesi koko rivin uudelle riville. Kun rivi kopioidaan tällä tavalla, myös dimensiot ja kestot kopioidaan. Voit myös valita **Muokkaa riviä** päivittääkseesi dimension arvot ja kestot **Kesto**-osassa.

## <a name="open-a-time-entry-behavior"></a>Avaa aikamerkintä -toiminnon toiminnallisuus
Mahdollisimman optimaalisen ja nopean syötön tukemiseksi näkyvimpiin kenttiin viikoittainen ajansyöttöruudukko näyttää valittujen dimensioiden ja ajan kestojen alijoukon. Jos haluat nähdä kaikki yksittäisen aikamerkinnän tiedot, valitse **Muokkaa merkintää** -kohdassa **Avaa**,

## <a name="submit-a-time-entry"></a>Lähetä aikamerkintä
Voit lähettää yksittäisen aikamerkinnän tai aikamerkintäryhmän valitsemalla joukon soluja tai koko ajansyöttörivin ja valitsemalla sitten **Lähetä**. Lähetetyt aikamerkinnät näkyvät merkintöinä, jotka odottavat hyväksyntää hyväksyjien **Hyväksyntä**-sivulla. Kun aikamerkinnät on lähetetty onnistuneesti, niitä ei voi muokata.

## <a name="recall-a-time-entry"></a>Peruuta aikamerkintä
Voit peruuttaa lähettämiäsi aikamerkintöjä. Voit peruuttaa yksittäisen aikamerkinnän, ryhmän aikamerkintöjä tai kokonaisen aikamerkintärivin. Peruutettuja aikamerkintöjä voi muokata.

## <a name="time-entry-status"></a>Aikamerkinnän tila

- **Luonnos**: Uudet aikamerkinnät saavat automaattisesti tilan **Luonnos**. Vain aikamerkintöjä, joiden tila on **Luonnos**, voidaan poistaa.
- **Lähetetty**: Kun aikamerkintä lähetetään, tilaksi päivittyy **Lähetetty**. 
- **Hyäksytty**: Kun lähetetty aikamerkintä hyväksytään, tilaksi päivittyy **Hyväksytty**. 
- **Palautettu**: Jos aikamerkintä hylätään, sen tilaksi päivittyy **Palautettu**, ja merkintä on käytettävissä korjausta ja uudelleenlähettämistä varten. 

## <a name="view-rejection-comments"></a>Hylkäystä koskevien huomautusten tarkastelu
Kun hyväksyjä hylkää aikamerkinnän, hyväksyjä voi lisätä huomautuksia, jotka auttavat resurssia ymmärtämään hylkäyksen syyn. Jos haluat tarkastella aikamerkinnän hylkäyshuomautuksia, valitse **Avaa merkintä**. Hylkäyshuomautukset näkyvät aikajanalla. Käyttäjä voi vastata hylkäyksen kommentteihin, ennen kuin hän lähettää merkinnän uudelleen.

## <a name="copy-week"></a>Kopioi viikko
Kun olet luonut muutaman merkinnän, käyttäjät voivat luoda useita aikamerkintöjä samalla kertaa.

1. Valitse **Aikamerkinnät**-lomakkeessa **Kopioi viikko**, jotta voit luoda joukkotoimintona lisää aikamerkintöjä. 
2. Käytä **Kopioi**-valintaruudun **Lähdejakso**-osassa **Alkamispäivä**- ja **Päättymispäivä**-kenttiä sen päivämäärävälin määrittelemiseksi, jolta aikamerkinnät kopioidaan. 
3. Määritä **Kohdejakso**-osassa **Alkamispäivä**-kentässä päivämäärä, jolle luodaan aikamerkintöjä. 
4. Valitse **Kopioi**. **Kohdejaksolle** määritellylle päivämäärälle luodaan kopio aikamerkinnöistä **lähdejakson** vastaavalta viikonpäivältä. Esimerkiksi edellisen viikon maanantain aikakirjaus kopioidaan sen viikon maanantaille, joka on määritetty **kohdejaksoksi**.

## <a name="import"></a>Tuonti
Samaa perusprosessia käytetään tuotaessa varauksista, kohdennuksista ja vaihdoista. Voit määrittää varausten tuonnin lähdepäivämäärävälin ja valita sitten erikseen varaukset, jotka kopioidaan luonnosaikamerkintöinä. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]