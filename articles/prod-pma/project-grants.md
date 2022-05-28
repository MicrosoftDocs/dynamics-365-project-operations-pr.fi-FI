---
title: Projektimäärärahat
description: Tässä aiheessa kerrotaan, miten avustus luodaan tai miten sitä muokataan.
author: RadhikaRS
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bc8240c2193bd2c27d54c04b55e14725ab208ac
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683994"
---
# <a name="project-grants"></a>Projektimäärärahat

[!include [banner](../includes/banner.md)]

Avustus on lahjaraha tiettyyn tarkoitukseen tai hankkeeseen. Yleensä avustuksen käyttämiselle on rajoituksia. Projektinhallinnassa ja kirjanpidossa voit lisätä ja seurata avustuksia sekä määrittää niiden suhteet projekteihin ja projektisopimuksiin. Esimerkiksi kaikille kentille voi tehdä alla mainitut toimet:

- Liitä apurahoja projekteihin ja rahoituslähteisiin **projektien** ja **Projektisopimuksen tieto** -sivujen linkkien kautta.
- Anna ja seuraa avustukseen tehtyjä muutoksia, kun se siirtyy tilasta toiseen.
- Määritä ja seuraa kustannuksia, pyydettyjä summia ja myönnettyjä summia.
- Luo pääapurahoja ja liitä niihin aliapurahoja.

Voit luoda avustuksen syöttämällä kaikki tiedot uuteen tietueeseen tai voit kopioida tiedot aiemmin luodusta tuesta ja päivittää ne sitten.

## <a name="create-a-new-grant"></a>Luo uusi avustus

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Avustukset** \> **Avustukset**.
2. Valitse **Uusi** \> **Apuraha**.
3. Kirjoita avustuksen tiedot -sivun **Yleinen**-pikavälilehden **avustuksen tunnus** -kenttään avustuksen aakkosnumeerinen tunnus.
4. Kirjoita avustuksen nimi **Avustuksen nimi** -kenttään.
5. Lisää **Kuvaus**-kenttään uuden avustuksen tiedot.

    Useimmat sivun kentistä ovat valinnaisia, ja voit kirjoittaa haluamasi määrän tietoja.

    Seuraavassa luettelossa on kuvattu kunkin avustuksen tiedot -sivun pikavälilehdessä määritetyt tiedot:

    - **Yleinen** – Anna avustuksen nimi, tila, kuvaus, tarkoitus ja summa.
    - **Yhteystiedot** – Anna tiedot henkilöstön jäsenistä, avustuksen hallinnoijasta ja avustuksen asiakas- tai organisaatiolähteestä. Voit myös määrittää, onko organisaatiosi läpikulkukohde, joka vastaanottaa avustuksen, ja välittää sen sitten toiselle vastaanottajalle. Valitse **Lisää**, jos haluat lisätä yhteyshenkilön tietoja, kuten puhelinnumeroita ja sähköpostiosoitteita.
    - **Päivämäärät ja määräajat** – Anna avustukseen ja avustussovellukseen liittyvät päivämäärät. Esimerkkejä ovat sovelluksen määräpäivä, lähetyspäivä sekä päivämäärä, jona avustus on hyväksytty tai hylätty.
    - **Liitetyt projektit ja projektisopimukset** – tähän pikavälilehteen voi syöttää tietoja vain, jos **Yleinen**-pikavälilehden **avustuksen tila** -kentän arvoksi on määritetty **aktiivinen** tai **myönnetty**. Viimeistele liittyvä tehtävä valitsemalla jokin seuraavista vaihtoehdoista:

        - **Lisää rahoituslähde** – Lisää avustukseen uusi rahoituslähde. Voit kirjoittaa kaikki tiedot nyt tai voit käyttää oletustietoja ja päivittää ne myöhemmin.
        - **Lisää projektisopimus** – Lisää tai päivitä projektisopimuksen tietoja.
        - **Lisää projekti** – Lisää tai päivitä projektin tietoja.

    - **Asetukset** – Anna tiedot toisiaan vastaavista varoista, jos nämä tiedot ovat pakollisia. Monet organisaatiot, jotka myöntävät apurahoja, edellyttävät, että vastaanottajat käyttävät tiettyä määrää omia rahojaan tai resursseja, jotta ne vastaisivat avustukseen myönnettyjä summia. Voit kirjoittaa **Paikallinen projekti- tai seurantatunnus** -kenttään tunnuksen, joka eroaa projektitunnuksesta.

        > [!NOTE]
        > Jos osa tuesta myönnetään jollekin toiselle organisaatiolle, määritä **alimyöntäjä**-asetukseksi **Kyllä**. Jos kyseessä on Yhdysvalloissa myönnetty avustus, voit määrittää, myönnetäänkö apuraha osavaltion toimeksiannon vai liittovaltion mandaatin perusteella.

    - **Nostotiedot** – voit lisätä tai päivittää tietoja siitä, miten usein avustusvaroja voidaan peruuttaa, laskuttaa tai käyttää.

## <a name="create-a-new-grant-from-a-copy"></a>Uuden avustuksen luominen kopiosta

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Avustukset** \> **Avustukset**.
2. Valitse **Uusi** \> **Kopio tuesta**.
3. Kirjoita uuden avustuksen aakkosnumeerinen tunnus ja nimi ja valitse sitten **OK**.
4. Tarkista tuen tiedot -sivulla kopioidun avustuksen tiedot ja tee tarvittavat muutokset. Useimmat sivun kentistä ovat valinnaisia.

## <a name="view-or-modify-grant-details"></a>Avustuksen tietojen tarkasteleminen tai muokkaaminen

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Avustukset** \> **Avustukset**.
2. Valitse muokattava avustus.
3. Valitse toimintoruudun **Avustus**-välilehden **Ylläpidä**-ryhmässä **Muokkaa**.
4. Tarkista avustuksen tiedot ja tee tarvittavat muutokset.


[!INCLUDE[footer-include](../includes/footer-banner.md)]