---
title: Automaattisen laskun luonnin määrittäminen
description: Tässä aiheessa on tietoja proformalaskujen automaattisen luomisen määrittämisestä.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1cce457fbc04ba9d3890d73439e6e7fd3db44d84a4498d5dc68ed82d362158b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997512"
---
# <a name="set-up-automatic-invoice-creation"></a>Automaattisen laskun luonnin määrittäminen 
 
_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

Voit määrittää automaattisen laskun luonnin Dynamics 365 Project Operationsissa. Järjestelmä luo proformalaskun, joka perustuu kunkin projektisopimuksen ja sopimusrivin laskuaikatauluun. Laskuaikataulut määritetään sopimusrivin tasolla. Kullakin palvelusopimuksen rivillä voi olla erillinen laskuaikataulu, tai sama laskuaikataulu voidaan sisällyttää palvelusopimuksen jokaiseen riviin.

Kun luot laskun, järjestelmä luo aina vähintään yhden laskun projektisopimusta kohden. Joissakin tapauksissa voidaan luoda useita laskuja. Jos palvelusopimuksessa on esimerkiksi useita asiakkaita, samalla luodaan sama määrä laskuja kuin niiden asiakkaiden määrä, joilla on laskutettavia tapahtumia kyseisessä projektisopimuksessa.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Tietoja siitä, miten tapahtumat sisällytetään laskuun 

Joskus kukin projektipohjainen sopimusrivi määrittää erillisen laskun aikataulun. Esimerkiksi Adatum-palvelusopimuksen toteutuspalveluilla on seuraavat sopimusrivit:

- Kiinteähintainen prototyyppityö, jossa on kaksi manuaalisesti luotua välitavoitetta.
- Toteutustyöt, jotka sisältävät aikaa ja laskutetaan kahden viikon välein maanantaisin.
- Aiheutuneet kulut, jotka on laskutettava kuukausittain kunkin kuukauden ensimmäisenä maanantaina.

Kummallekin riville määritetyt laskuaikataulut näyttävät seuraavalta taulukolta:

| Palvelusopimuksen rivi | Laskun suorituspäivä | Tapahtuman katkaisupäivämäärä | Välitavoitteen päivämäärä | Välitavoitteen summa |
| --- | --- | --- | --- | --- |
| Prototyyppityö | 5. lokakuuta, maanantai | - | 5. lokakuuta, maanantai | 5000 USD |
| - | 3. marraskuuta, tiistai | - | 3. marraskuuta, tiistai | 12,000 USD |
| Käyttöönottotyö | 5. lokakuuta, maanantai | 4. lokakuuta, sunnuntai | - | - |
| - | 19. lokakuuta, maanantai | 18. lokakuuta, sunnuntai | - | - |
| - | 2. marraskuuta, maanantai | 1. marraskuuta, sunnuntai | - | - |
| - | 16. marraskuuta, maanantai | 15. marraskuuta, sunnuntai | - | - |
| Aiheutuneet kulut | 5. lokakuuta, maanantai | 4. lokakuuta, sunnuntai | - | - |
| - | 2. marraskuuta, maanantai | 1. marraskuuta, sunnuntai | - | - |

Tässä esimerkissä, jossa automaattinen laskutus suoritetaan:

- **4. lokakuuta tai mikä tahansa päivämäärä ennen sitä**: Tälle sopimukselle ei ole luotu laskua, koska kunkin sopimusrivin **laskuaikataulutaulukkoa** ei kutsuta pois sunnuntaina 4. lokakuuta laskun suorituspäivänä.
- **5. lokakuuta, maanantai**: Yksi lasku luodaan:

    - Välitavoitteen sisältävä prototyyppityö, jos se on merkitty **Valmiiksi laskutettavaksi**.
    - Käyttöönottotyöt, jotka sisältävät kaikki aikatapahtumat, jotka on luotu ennen tapahtuman katkaisupäivää sunnuntai lokakuun 4., joka on merkitty **valmiiksi laskutettavaksi**.
    - Aiheutuneet kulut, jotka sisältävät kaikki kulutapahtumat, jotka on luotu ennen tapahtuman katkaisupäivää sunnuntai lokakuun 4., joka on merkitty **valmiiksi laskutettavaksi**.
  
- **6. lokakuuta tai mikä tahansa päivämäärä ennen 19. lokakuuta**: Tälle sopimukselle ei ole luotu laskua, sillä kunkin sopimusrivin **laskuaikataulutaulukkoa** ei kutsuta pois sunnuntaina 6. lokakuuta tai minä tahansa päivämääränä ennen 19. lokakuuta laskun suorituspäivänä.
- **19. lokakuuta, maanantai**: Käyttöönottotöistä luodaan yksi lasku, joka sisältää ennen tapahtuman katkaisupäivää sunnuntaita lokakuun 18. luodut kaikki aikatapahtumat, jotka on merkitty **valmiiksi laskutettavaksi**.
- **2. marraskuuta, maanantai**: Yksi lasku luodaan:

    - Käyttöönottotyöt, jotka sisältävät kaikki aikatapahtumat, jotka on luotu ennen tapahtuman katkaisupäivää sunnuntai marraskuun 1., joka on merkitty **valmiiksi laskutettavaksi**.
    - Aiheutuneet kulut, jotka sisältävät kaikki kulutapahtumat, jotka on luotu ennen tapahtuman katkaisupäivää sunnuntai marraskuun 1., joka on merkitty **valmiiksi laskutettavaksi**.

- **3. marraskuuta, tiistai**: Yksi lasku luodaan prototyyppityölle, joka sisältää 12 000 USD:n välitavoitteen, jos se on merkitty **valmiiksi laskutettavaksi**.

## <a name="configure-automatic-invoicing"></a>Määritä automaattinen laskutus

Automaattinen laskujen luominen määritetään suorittamalla seuraavat vaiheet.

1. Siirry **Project Operations** -toiminnossa kohtaan **Asetukset** > **Toistuvan laskun määrittäminen**.
2. Luo erätyö ja anna sille nimeksi **Project Operationsin laskujen luominen**. Erätyön nimessä on oltava sanat "laskujen luominen".
3. Valitse **Työtyyppi**-kentässä **Ei mitään**. Kenttien **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.
4. Valitse **Suorita työnkulku**. **Valitse tietue** -valintaikkunassa näkyy kolme työnkulkua:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Valitse **ProcessRunCaller** ja sitten **Lisää**.
6. Valitse seuraavassa valintaikkunassa **OK**. **Lepo**-työnkulkua seuraa **Käsittely**-työnkulku. 

> [!NOTE]
> Vaiheessa 5 voit myös valita **ProcessRunner**. Kun tämän jälkeen valitset **OK**, **Käsittely**-työnkulkua seuraa **Lepo**-työnkulku.

Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja. Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**. **ProcessRunner** on se työnkulku, joka tosiasiassa luo laskut. Työnkulku käy läpi kaikki sopimusrivit, joille on luotava lasku, ja luo kyseiset laskut. Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja. Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä. Jos laskujen luomista edellyttäviä tapahtumia ei ole, työnkulku ohittaa laskujen luonnin.

Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller**, antaa päättymisajan ja sulkeutuu. **ProcessRunCaller** käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin. Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.

Laskujen luomisen erätyö on toistuva työ. Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä. Siksi erätyö kannatta käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.

> [!NOTE]
> Erälaskutus suoritetaan vain sellaisille Project Operations -toiminnoille, jotka on määritetty laskun aikataulun mukaan. Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet. Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
