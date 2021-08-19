---
title: Yritysten välisten tapahtumien luominen
description: Tässä aiheessa on tietoja yritysten välisten asiakkaan ja toimittajan tapahtumien luomisesta.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4ce3a45e5a09b7ac5b5663cf9983e3bed7bf7e0d3fedede2e4524c51069a800b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005477"
---
# <a name="create-intercompany-transactions"></a>Yritysten välisten tapahtumien luominen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Yritysten väliset tapahtuman ovat projektisopimuksen aika- ja kulutapahtumia, jotka kuuluvat yhteen yritykseen tai organisaatioyksikköön, kun projektisopimuksen resurssit ovat osa toista yritystä tai organisaatioyksikköä.

Kun yritysten välinen tapahtuma hyväksytään, luodaan seuraavat todelliset tapahtumat

| **Tapahtumatyyppi** | **Sovellettava hinnasto** | **Tapahtumavaluutta** |
| --- | --- | --- |
| Kustannus | Hankintayksikön kustannushinnasto | Hintarivillä oleva valuutta |
| Laskuttamaton myynti. Nämä luodaan vain sellaisia toteutuneita arvoja varten, jotka liittyvät laskutustyypin, ajan ja materiaalin sopimusriviin. | Sopimusprojektin myyntihinnasto | Sopimusvaluutta |
| Resursointiyksikön kustannus | Resursointiyksikön kustannushinnasto | Hintarivillä oleva valuutta |
| Organisaatioyksiköiden välinen myynti | Hankintayksikön kustannushinnasto | Hintarivillä oleva valuutta |

Kustannukset, resursointiyksikön kustannukset ja organisaatioyksikön myyntitapahtumien hinnoittelu ja valuutta määritetään **organisaatioyksikössä**. Tämä on tärkeää muistaa päätettäessä, miten yritysten ja organisaatioyksiköiden rakenne toteutetaan.

Kun luot mahdollisuus-, tarjous-, projektisopimus- ja projektitietueita, järjestelmä tarkistaa, että hankintayksikön valuutta vastaa hankintayrityksen kirjanpitovaluuttaa. Näitä tietueita ei voi luoda, jos ne eivät ole samat. Organisaatioyksikön valuutta määritetään Dynamics 365 Project Operationsissa siirtymällä kohtaan **Dataverse** > **Asetukset** > **Organisaatioyksiköt**. Yrityksen kirjanpitovaluutta määritetään Dynamics 365 Financessa siirtymällä kohtaan **Pääkirjankirjanpito** > **Tapahtumarekisterin määritys** > **Tapahtumarekisteri**. Valuutta synkronoidaan Dataverse-ympäristöön Ledgers Dual Write Map -toiminnolla.

Järjestelmä luo resursointiyksikön kustannukset ja organisaatioksiköiden väliset toteutuneet myynnit seuraavissa tilanteissa:

  - Kun resursointiyksikkö eroaa hankintayksiköstä
  - Kun resursointiyritys eroaa hankintayrityksestä

Kuitenkin vain sellaiset tapahtumat, joilla on eri resursointiyritys, siirretään Dynamics 365 Finance -ympäristöön lisäkirjanpitoa varten.

Projektin toteutuneiden arvojen kirjanpito kirjataan Project Operationsissa Financen integrointikirjauskansioon. Järjestelmä luo seuraavat kirjauskansion rivit.

| **Tapahtumatyyppi** | **Oikeushenkilö** | **Luo projektitapahtuman kirjattaessa** | **Taloushallinnon dimension oletusarvot tulevat kohteesta** | **Arvonlisäveron laskutuksen oletusryhmä ja laskutusnimikkeen oletusarvonlisäveroryhmä** |
| --- | --- | --- | --- | --- |
| Kustannus | Ei lisätä integrointikirjauskansioon | – | – | – |
| Laskuttamaton myynti | Lainaa ottavan yrityksen integrointikirjauskansio | Kyllä | Project | **Laskutuksen arvonlisäveroryhmä**: **Palvelusopimuksen asiakkaan perusteella** <br/> **Laskutusnimikkeen arvonlisäveroryhmä**: Nykyisestä yrityksen projektiluokasta kirjauskansion rivillä |
| Resursointiyksikön kustannus | Lainaa antavan yrityksen integrointikirjauskansio | No | Yritysten välinen asiakas | **Laskutuksen arvonlisäveroryhmä**: **Yritysten välisen asiakkaan perusteella** <br/> **Laskutusnimikkeen arvonlisäveroryhmä**: Nykyisestä yrityksen projektiluokasta kirjauskansion rivillä |
| Organisaatioiden välinen myynti | Lainaa antavan yrityksen integrointikirjauskansio | No | Yritysten välinen asiakas | **Laskutuksen arvonlisäveroryhmä**: **Yritysten välisen asiakkaan perusteella** <br/> **Laskutusnimikkeen arvonlisäveroryhmä**: Nykyisestä yrityksen projektiluokasta kirjauskansion rivillä |

### <a name="example-intercompany-transactions"></a>Esimerkki: Yritysten väliset tapahtumat

Molly Clark, , GBPM:llä työskentelevä kehittäjä, kirjaa 10 tuntia työtä USPM Adventure Works -projektiin, minkä projektipäällikkö hyväksyy. Kehittäjän hinta GBPM:llä on 88 GBP tunnissa. GBPM laskuttaa USPM:ltä 120 USD kehitystuntia kohti. USPM laskuttaa asiakkaalta Adventure Works 200 USD GBPM-resurssin tekemästä työstä. Lisätietoja on kohdassa [Yritysten välisen laskutuksen määrittäminen](configure-intercompany-invoicing.md).

1. Siirry Project Operationsissa kohtaan **Resurssit** ja valitse luettelosta **Molly Clark**. Valitse **Aikataulutus**-välilehden **Yritys**-kentässä **GBPM**.
2. Siirry kohtaan **Myynti** > **Asiakkaat** ja valitse **Uusi** luodaksesi asiakastietueen Adventure Worksille.
    1. Määritä yritykseksi **USPM**.
    2. Määritä **Suhdetyypiksi** **Asiakas**.
    3. Valitse **Asiakasryhmä 10 – kotimaa**.
    4. Määritä valuutaksi **USD**.
    5. Tallenna tietue.
3. Siirry kohtaan **Myynti** > **Projektisopimukset** ja luo uusi projektisopimus Adventure Worksille.
    1. Määritä omistava yritys **USPM**-yksiköiksi ja sopimusyksiköksi **Contoso Robotics US**.
    2. Valitse asiakkaaksi Adventure Works.
    3. Valitse tuotehinnasto ja tallenna tietue.
    4. Luo uusi sopimusripi **Sopimusrivit**-välilehdellä. Määritä mikä tahansa nimi ja valitse laskutustavaksi **Aika ja materiaalit**.
    5. Luo uusi projekti ja liitä se tähän sopimusriviin.
4. Kirjaudu sisään resurssina **Molly Clark**. Siirry kohtaan **Projektit** > **Aikamerkinnät** ja luo aikamerkintä Adventure Works -projektille.
5. Kirjaudu sisään projektipäällikkönä. Siirry kohtaan **Projektit** > **Hyväksynnät** ja hyväksy Molly Clarkin luoma aikamerkintätapahtuma.
6. Siirry Adventure Works -projektiin ja valitse **Liittyvät** > **Todelliset arvot**. Seuraavat toteutuneet tapahtumat luodaan.

| **Tapahtumatyyppi** | **Hinta** | **Tapahtumavaluutta** | **Summa** |
| --- | --- | --- | --- |
| Kustannus | 120 | USD | 1200 |
| Laskuttamaton myynti | 200 | USD | 2000 |
| Resursointiyksikön kustannus | 88 | GBP | 880 |
| Organisaatioyksiköiden välinen myynti | 120 | USD | 1200 |

7. Kirjaudu sisään USPM-kirjanpitäjänä. Avaa Finance-esiintymä, joka liittyy Project Operationsiin, ja valitse **USPM**. 
8. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Project Operations ja Customer Engagement** > **Tuo valmistelusta** ja valitse kausittainen prosessi suoritettavaksi. Tämä kausittainen prosessi täyttää Project Operationsin integrointikirjauskansion.
9. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kirjauskansiot** > **Project Operationsin integrointikirjauskansio** ja tarkista kirjauskansion rivit. Järjestelmä luo seuraavan rivin.

    | **Tapahtumatyyppi** | **Hinta** | **Tapahtumavaluutta** | **Summa** |
    | --- | --- | --- | --- |
    | Laskuttamaton myynti | 200 | USD | 2000 |

    Jos järjestelmä on määritetty kerryttämään tämän projektin tuoton, seuraava on kirjattu:

    - Debit: Projekti – Käynnissä oleva myynnin arvo 200 USD
    - Credit: Projekti – Kerrytetty tuotto 200 USD

    Tämä laskuttamaton myynti on nyt valmis laskutettavaksi. Adventure Worksin lasku voidaan kirjata rahoituksellisesti tarvittaessa.

10. Kirjaudu sisään **GBPM**-kirjanpitäjänä. Avaa Finance-esiintymä, joka liittyy Project Operationsiin, ja avaa yritys **GBPM**. 
11. Siirry kohtaan **projektinhallinta ja kirjanpito** > **Jaksottainen** > **projektitoimintojen integrointi** > **Tuo valmistelutaulukosta** ja suorita jaksottainen prosessi täyttääksesi Project Operations Integroinnin kirjauskansion.
12. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kirjauskansiot** > **Project Operationsin integrointikirjauskansio** ja tarkista rivit. Järjestelmä luo seuraavat rivit.

    | **Tapahtumatyyppi** | **Hinta** | **Tapahtumavaluutta** | **Summa** |
    | --- | --- | --- | --- |
    | Resursointiyksikön kustannus | 88 | GBP | 880 |
    | Organisaatioyksiköiden välinen myynti | 120 | USD | 1200 |

    Näiden tietueiden kirjaaminen aiheuttaa seuraavat tositetapahtumat:

    - Debit: Projektikustannus 88 GBP
    - Credit: Palkanlaskennan kohdistus 88 GBP

    Jos järjestelmä on määritetty kerryttämään yritysten välisen tuoton, seuraava on kirjattu:

    - Debit: Projekti – Käynnissä oleva myynnin arvo 120 USD
    - Credit: Projekti – Kerrytetty tuotto 120 USD

    Järjestelmä on nyt valmis luomaan yritysten välisen asiakaslaskun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
