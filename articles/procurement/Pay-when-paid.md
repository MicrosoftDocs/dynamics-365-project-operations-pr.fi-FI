---
title: Toimittajan maksa kun maksettu -maksut
description: Tässä aihe, miten maksa kun maksettu (PWP) -skenaariota käytetään.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525333"
---
# <a name="pay-when-paid-vendor-payments"></a>Toimittajan maksa kun maksettu -maksut

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aihe, miten maksa kun maksettu (PWP) -skenaariota käytetään.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Ostotilauksen luominen, jossa on PWP-termejä

Kun kirjaat laskun toimittajalta, jos toimittajalle on asetettu PWP-ehtoja, nämä termit näkyvät ostotilaus (PO) -riveillä. Jos haluat luoda ostotilauksen, jossa on PWP-termit, toimi seuraavasti.

1. Noudata yhtä näistä vaiheista Microsoft Dynamics 365 Financessa:

    - Siirry kohtaan **ostaminen ja hankinta** \> **Ostotilaukset** \> **Kaikki ostotilaukset**. Valitse toimintoruudussa **Uusi**. Valitse **Luo ostotilaus** - valintaikkunassa toimittaja, jolle projektille on määritetty PWP-ehdot, kirjoita muut pakolliset tiedot ja valitse sitten **OK**.
    - Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**. Valitse toimintoruudun **Hallitse**-välilehdessä **Nimiketehtävä**. Valitse ostotilaus. Valitse toimittaja, jolle projektille on määritetty PWP-ehdot, ja valitse sitten **OK**.

2. Valitse **Ostotilaus**-sivulla **Ostotilausrivit**-pikavälilehdellä **Lisää rivi** luodaksesi ostotilausrivin.
3. Valitse nimikenumero tai hankintaluokka ja anna muut pakolliset tiedot. Tarkista toimittajan ostotilausrivin tiedot.

    **Maksa, kun maksettu** -asetus valitaan automaattisesti, ja **PWP-kynnysprosentti**-kentän arvo kopioidaan automaattisesti **Projektit**-sivun **PWP-kynnysprosentti**-kentästä.

4. Jos et halua käyttää PWP-ehtoja ostotilausrivin toimittajalle, tyhjennä **maksu, kun maksettu** -vaihtoehto. Tässä tapauksessa ostotilausrivin **PWP-kynnysprosentti**-kentän arvoksi palautetaan **0** (nolla).
5. Valitse **Ostotilaus**-sivun toimintoruudussa **Osto**-välilehdellä **Vahvista** vahvistaaksesi ostotilauksen.
6. Luo tilauksen lasku valitsemalla toimintoruudun **Lasku**-välilehdellä **Lasku** luodaksesi ostotilaukselle laskun.

## <a name="create-a-project-invoice-proposal"></a>Projektin laskuehdotuksen luominen

Projektilaskuehdotuksia käytetään projektilaskujen luomiseen asiakkaalle. PWP-skenaariossa toimittajan maksut riippuvat asiakasmaksuista PWP-asetusten mukaisesti. Voit kuitenkin vapauttaa maksut ilman asiakkaan maksuja tarpeen mukaan. Voit luoda projektilaskun asiakkaalle seuraavasti.

1. Siirry asiakasvuorovaikutussovelluksissa kohtaan **Projekti** \> **Projektit** ja valitse projekti.
2. Valitse **Toteutuneet**-välilehdessä sen ostotilaustapahtuman luotu todellinen rivi, jonka tyyppi on **Laskuttamaton myyntitapahtuma**. Valitse sitten **Valmis laskutettavaksi**.
3. Siirry kohtaan **Myynti** \> **Myynti** \> **Projektisopimus** ja valitse projektisopimus.
4. Valitse **Lasku** toimintoruudussa luodaksesi asiakaslaskun.
5. Siirry Financessa kohtaan **projektinhallinta ja kirjanpito** \> **Jaksottainen** \> **Tuo valmistelutaulukosta** ja valitse **OK** luodaksesi Project operations -integraatiokirjauskansion.
6. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Projektin laskut** \> **Projektilaskuehdotus** ja valitse **Kirjaa** kirjataksesi laskuehdotuksen, joka luotiin projektille.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Asiakkaan maksun päivittäminen ja toimittajan maksaminen

Kun toimittaja suorittaa projektissa työnsä ja lähettää sinulle laskun, tarkista projektin tila ja myyntilaskut ja selvitä, onko projektin PWP-ehdot täytetty. Jos toimittajan PWP-ehdot täyttyvät, voit määrittää, mitkä toimittajan laskun rivit maksetaan projektin asiakasmaksujen perusteella. Jos päätät maksaa toimittajalle, vaikka PWP-ehdot eivät täyttyisikään, voit korvata toimittajan laskussa olevat PWP-ehdot **Toimittajan maksu kun maksettu** -sivulla.

1. Siirry Financessa kohtaan **Projektinhallinta ja kirjanpito** \>**Projektit** \> **Kaikki projektit** ja valitse projekti.
2. Valitse toimintoruudussa **Ohjausobjekti** ja valitse sitten **Toimittajan laskut**, kun haluat näyttää kaikki projektille luodut toimittajan laskut.
3. Jos kyseessä on **toimittajan lasku, joka maksetaan kun on maksettu** -sivu, kirjoita hakukenttään arvot löytääksesi toimittajan laskun, jota haluat tarkastella, ja valitse sitten **Hae**.
4. Valitse **Maksa, kun maksettu** -vaihtoehto, jos haluat tarkastella vain PWP-laskuja.
5. Valitse **toimittajan laskun rivit** -pikavälilehden rivit, jotka haluat vapauttaa maksettaviksi.
6. Valitse **Vapauta toimittajan maksu**. **Maksu, kun maksettu** -asetus on poistettu, ja **valmis maksettavaksi** -kentän arvoksi vaihdetaan **Kyllä**.
