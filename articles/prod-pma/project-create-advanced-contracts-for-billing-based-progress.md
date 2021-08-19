---
title: Etenemiseen perustuvien edistyksellisten hinnoittelusopimusten luominen
description: Tässä aiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttimäärän perusteella.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 661e8aa0be70e9c8aadcb3a3d9dd6d39d1bcb2fd55d198b3c9af19fc2d0ae9d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000977"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Etenemiseen perustuvien edistyksellisten hinnoittelusopimusten luominen
[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttimäärän perusteella. Laskun summat lasketaan automaattisesti projektille määritettyjen budjettiluokkien mukaan. Laskun ajoitus määritetään, kun neuvotellaan projektisopimuksesta asiakkaan kanssa.

Tämän aiheen ohjeiden avulla voit määrittää palvelusopimuksen, siihen liittyvän projektin ja laskutussäännöt, jotka laskevat projektin budjettiluokkien laskujen summat.

Kun olet luonut palvelusopimuksen ja projektin, voit määrittää projektin tiedot. Voit esimerkiksi määrittää aktiviteetteja ja delegoida työntekijöitä projektiin.

## <a name="example"></a>Esimerkki:

Organisaatiosi on ohjelmistokehitysyritys. Sitoudut kehittämään palkanlaskentapaketin asiakkaalle 20 000 Yhdysvaltain dollarin (USD) kokonaismaksua vastaan. Organisaatiosi sitoutuu laskuttamaan asiakasta samalla, kun se täyttää tietyt projektin prosenttiosuudet. Voit määrittää työlle seuraavat projektiluokat, jotta voit käyttää niitä laskutusprosessissa:

- Konsultointipalvelut
- Suunnittele
- Asennus

Voit myös määrittää laskutussäännöt, jotka laskevat automaattisesti kullekin luokalle valmiin projektityön prosenttimäärän laskusummat.

Budjettipäällikkö luo budjetin projektiluokille. Valmiin työn määrä lasketaan automaattisesti prosentteina todellisesta työstä budjetoitujen summien perusteella.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin luot laskutussääntöjä käyttävän projektin, sinun täytyy määrittää numerosarjat laskutussäännöille ja maksukirjauskansiolle, jota käytetään edistymiseen perustuvan laskutuksen kirjauksessa.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Projektinhallinnan ja kirjanpidon parametrit**.
2. Määritä **projektinhallinta ja kirjanpidon parametrit** -sivun **numerosarjat**-välilehdessä numerosarja, jota haluat käyttää, kun laskutussääntöjä luodaan.
3. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Kirjauskansiot** \> **Maksu**.
4. Valitse **maksukirjauskansio**-sivulla **Uusi** ja kirjoita kirjauskansion nimi.

## <a name="create-a-contract-for-progress-billings"></a>Luo sopimus edistymälaskutusta varten

Tämän menettelyn avulla voit luoda projektisopimuksen kiinteähintaiselle projektille. Projektilasku luodaan, kun projektissa valmis työ saavuttaa määritetyn prosenttiosuuden.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **projektit** \> **Projektiyhteyshenkilöt**.
2. Valitse **Projektisopimukset**-sivulla **Uusi**.
3. Määritä **Uusi projekti sopimus** -valintaikkunassa seuraavat kentät:

    - **Nimi**
    - **Rahoitustyyppi**
    - **Rahoituslähde**
    - **Myyntivaluutta** – tätä valuuttaa käytetään oletusarvon mukaan projektisopimukseen liitetyistä asiakaslaskuista. Voit kuitenkin muuttaa tietyn asiakaslaskun myyntivaluuttaa.

4. Valitse **OK**. Tiedot kopioidaan **Projektisopimukset**-sivun otsikkoon.
5. Täytä **Projektisopimukset**-sivulla loput projektin pakolliset tiedot.

## <a name="create-a-project-for-progress-billings"></a>Luo projekti edistymälaskutusta varten

Seuraavien vaiheiden mukaisesti voit luoda projektin ja kaikki projektisopimukseen liittyvät aliprojektit.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.
2. Valitse **Kaikki projektit**-sivulla **Uusi**.
3. Valitse **Uusi projekti** -valintaikkunan **Projektityyppi**-kentässä **Aika ja materiaali**.
4. Valitse projektiryhmä. Projektiryhmä määrittää ryhmälle delegoitujen projektien kirjaustiedot.
5. Valitse **Luo projekti**.
6. Kun projekti on luotu, määritä projektin vaiheeksi **tekeillä**.

## <a name="create-a-budget-for-a-project"></a>Budjetin luominen projektiin

Budjettiluokkia käytetään laskettaessa laskusummat kullekin luokalle valmistuneesta työstä. Seuraavien vaiheiden mukaisesti voit luoda arvioidut kustannusluokat.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.
2. Valitse ja avaa haluamasi projekti **kaikki projektit** -sivulla.
3. Valitse **projektit**-sivun toimintoruudun **suunnitelma**-välilehden **budjetti**-ryhmässä **Projektibudjetti**.
4. Kirjoita **projektibudjetti**-sivulle arvioidut kustannukset kullekin projektiluokalle.

## <a name="create-billing-rules-for-progress-billings"></a>Laskutussääntöjen luominen keskeneräisiä laskuja varten

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **projektit** \> **Projektiyhteyshenkilöt**.
2. Avaa projektisopimus **Projektisopimukset**-luettelosivulla.
3. Valitse projektisopimus-sivun **laskutussäännöt**-pikavälilehdessä **Lisää**.
4. Valitse **Laskutussääntö**-sivun **rivityyppi**-kentässä **edistyminen**.
5. Kirjoita **laskutussääntörivin tiedot** -pikavälilehden **sopimuksen arvo** -kenttään palvelusopimuksen kokonaisarvo.
6. Valitse **luokka**-kentässä luokka, johon maksutapahtuma kirjataan.
7. Valitse **projekti**-kentästä projekti, joka käyttää tätä laskutussääntöä.
8. Valinnainen: voit delegoida laskutussäännön lisäprojekteille. Valitse **projekti**-pikavälilehden **käytettävissä olevat projektit** -osasta ja valitse sitten oikea nuolipainike, kun haluat lisätä projektin **Valitut projektit** -osaan.
9. Valinnainen: Laske sen prosenttimäärän summa, jonka asiakas pidättää maksuista laskulla. Valitse **maksun pidätysehdot** -pikavälilehdessä rahoituslähde ja kirjoita sitten **pidätysprosentti** -kenttään pidätysprosentti.
10. Toista nämä vaiheet, kun haluat luoda projektisopimukselle lisää laskutussääntöjä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]