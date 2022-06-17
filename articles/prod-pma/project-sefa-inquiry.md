---
title: Federal Awards -tutkimuksen kulujen aikataulu
description: Tässä artikkelissa on tietoja Federal Awards -tutkimuksen kulujen aikataulusta.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 00f9e97b9a6b3e8fe5e9cf9143e670612869b84c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916652"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Federal Awards -tutkimuksen kulujen aikataulu

[!include [banner](../includes/banner.md)]

Hallinto- ja budjettitoimiston (Circular A-133) mukaan viranomaiset, jotka vastaanottavat liittovaltion varoja, kuuluvat auditoinnin vaatimuksiin, joita kutsutaan myös yksittäiseksi tarkastuksiksi. Auditointiprosessin avulla voidaan raportoida liittovaltion apurahojen tuotoista ja menoista toistuvasti. Osa yhtenäisestä auditointiraportista sisältää Federal Awards -ohjelman (SEFA) kulujen aikataulun.

Federal Awards -tutkimuksen kulujen luettelo sisältää Federal Assistance (CFDA) -osaston ja -numeron, avustusnumeron, avustuksen vuoden, liittovaltion toimiston, joka tarjoaa varat, sekä sen nimen, jossa läpimenoentiteetti on. Kysely on tiettynä ajanjaksona. Yleensä kyseinen kausi on sama kuin tilinpäätöskausi, joka on tilikausi.

Kysely sisältää apurahoja, joiden ennustepäivämäärät ovat valitulla päivämäärävälillä. **Kyselyn myöntäjä** -sarakkeessa näkyy apuraha-asiakas tai apurahan myöntäjä. Myönnettyä apurahaa varten **Myöntävä toimisto**-sarake näyttää apurahan asiakkaan. Jos apuraha ei ole myönnetty apuraha, **Myöntävä toimisto**-sarake on tyhjä.

## <a name="set-up-the-cfda-clusters"></a>Määritä CFDA-klusterit

Sinun täytyy määrittää CFDA-klusterit, jotka voidaan liittää CFDA-numeroihin Federal Awards -kyselyn kulujen aikataulussa.

1. Siirry kohtaan **projektinhallinta ja kirjanpito \> asetukset \> apurahat \> luettelo liittovaltion kotimaisista avustusklustereista**.
2. Jos haluat luoda uuden CFDA-klusterin, valitse **Uusi**.
3. Anna klusterin nimi.
4. Tallenna muutokset valitsemalla **Tallenna**.

## <a name="set-up-cfda-numbers"></a>CFDA-numeroiden määrittäminen

Sinun on määritettävä CFDA-numerot, jotka voidaan lisätä apurahoihin ja sisällyttää liittovaltion palkintojen kyselyaikatauluun.

1. Siirry kohtaan **projektinhallinta ja kirjanpito \> asetukset \> apurahat \> luettelo liittovaltion kotimaisista avustusnumeroista**.
2. Jos haluat luoda CFDA-numeron, valitse **Uusi**.
3. Kirjoita CFDA-numero **Numero**-sarakkeeseen.
4. Paina **sarkain**-näppäintä.
5. Kirjoita CFDA-ruutuun **Kuvaus**-sarakkeessa.
6. Paina **sarkain**-näppäintä.
7. Valinnainen: Lisää **Ohjelman klusteri** -kenttään sopiva CFDA-klusteri.
8. Tallenna muutokset valitsemalla **Tallenna**.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Määritä apurahat, jotka raportoivat Federal Awards -tutkimuksen kulujen aikataulusta

1. Siirry kohtaan **projektin hallinta ja kirjan pito \> avustukset \> avustukset** ja valitse olemassa oleva avustus.
2. Määritä **Asetukset**-pikavälilehden **Federal Domestic Assistance- luettelo** -kentän luettelossa CFDA-numero. Apurahan CFDA-numero määrittää CFDA-klusterin raportointia varten.
3. Kirjoita **yhteyshenkilön tiedot** -pikavälilehden myöntäjä-tiedot seuraavasti:

    1. Kirjoita **Avustusasiakas**-kenttään avustuksesta vastaava asiakas. Jos kyseessä on olemassa oleva apuraha, nämä tiedot on ehkä jo syötetty.
    2. Ilmaise, onko avustusasiakas rahoittaja. Jos avustusasiakas on rahoittaja, jätä **läpivalinta**-ruutu tyhjäksi. Jos toinen asiakas on rahoittaja ja avustusasiakas on vastuussa rahavarojen käytöstä ja seurannasta, valitse **Läpimeno**-valintaruutu.

4. Jos valitsit edellisessä vaiheessa **läpimeno**-valintaruudun, anna **myöntäjätoimisto**-kenttään avustuksen toimittanut asiakas. Myöntäjä ja avustusasiakas eivät voi olla sama asiakas.

Seuraavassa on esimerkki läpilaskuavustuksesta:

Liittohallitus rahoitti valtion infrastruktuurihanketta. Liittohallitus antoi rahat valtiolle. Tässä tapauksessa liittohallitus on myöntäjä, ja osavaltio on avustusasiakas.

> [!NOTE] 
> Kun otat ominaisuuden käyttöön ensimmäisen kerran, ensimmäiset CFDA-numerot syötetään avustuksina olevien lukujen perusteella.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Älä sisällytä avustuksia SEFA-raportointiin avustustyypin perusteella

1. Siirry kohtaan **Projektinhallinta ja kirjanpito \> Määritys \> Avustukset \> Avustustyypit**.
2. Valitse **Oletustiedot**-pikavälilehdessä **Ohita Federal Awards -ohjelman kulut** -valintaruutu.
3. Tallenna muutokset valitsemalla **Tallenna**.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Aja Federal Awards -tutkimuksen kulujen aikataulukysely

1. Siirry **projektinhallinta ja kirjanpito \> kyselyt ja raportit \> apurahakyselyt \> Federal Awards -tutkimuksen aikatauluun**.
2. Toimi **Parameterit**-osassa seuraavasti:

    1. Valitse **päivämääräväli**-kentässä päivämäärävälin koodi. Voit vaihtoehtoisesti määrittää päivämäärävälin **alkamispäivä**- ja **pvm:stä**- kenttiin.
    2. Valinnainen: Jos haluat, että kyselyyn sisällytetään vain laskutetut tapahtumat, määritä **Sisällytä vain laskutetut tulot** -asetuksen arvoksi **Kyllä**.

## <a name="columns"></a>Sarakkeet

Federal Awards -tutkimuksen kulujen aikataulu sisältää seuraavat sarakkeet:

- Federal Domestic Assistance -klusterin nimi
- Myöntäjä
- Läpivientiyritys
- Avustuksen nimi
- Avustuksen tunnus
- Avustushakemuksen tunnus
- Federal Domestic Assistance -luettelo
- Kuitit
- Menot


[!INCLUDE[footer-include](../includes/footer-banner.md)]