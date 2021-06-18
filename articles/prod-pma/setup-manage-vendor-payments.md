---
title: Toimittajan maksu, kun maksettu -maksujen määrittäminen ja käyttäminen
description: Tässä aiheessa kerrotaan, miten luodaan maksullisten maksujen (PWP) ehtoja, jotta voit vapauttaa osittaisen toimittajan maksut asiakasmaksujen perusteella.
author: RadhikaRS
ms.date: 03/30/2020
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
ms.openlocfilehash: c6f7888f3803b2c83a72bcac4caed1a7d7bc5f65
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997552"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Toimittajan maksu, kun maksettu -maksujen määrittäminen ja käyttäminen

[!include [banner](../includes/banner.md)]

Kun hyväksyt toimittajan, joka toimii alihankkijana, haluat ehkä evätä toimittajalle maksun, kunnes asiakas maksaa projektista. Tämän skenaarion tueksi voit määrittää maksu, kun maksettu (PWP) -ehdot, kun määrität ostotilauksen toimittajalle.

Jos esimerkiksi asiakas maksaa summan projektilaskusta, voit vapauttaa toimittajan laskun määrän tai osan siitä. Määritä vain PWP-ehdot, jotka määrittävät, että toimittajalle maksetaan sen jälkeen, kun asiakkaalta on saatu maksettu prosenttiosuus liittyvästä maksusta. Jos vastaanotat osittaisen maksun asiakkaalta, voit manuaalisesti vapauttaa joitakin liittyviä toimittajan laskuja maksuun.

Seuraavassa esimerkissä kuvataan prosessia, jossa käytetään PWP-termejä.

## <a name="example"></a>Esimerkki:

Organisaatiosi suostuu tarjoamaan asiakkaalle 100 tietokonetta, joissa on asennettuna ohjelmisto, hintaan 150,00 Yhdysvaltain dollaria (USD) tietokonetta kohti. Tämän jälkeen voit palkata toimittajan toimittamaan tietokoneet, joihin on asennettu ohjelmisto. Sopimuksen mukaan asiakkaan on hyväksyttävä tietokoneiden laatu, ennen kuin se maksaa organisaatiolle. Organisaation käytäntö on evätä toimittajalle maksu, kunnes asiakas on maksanut sinulle. Tämän vuoksi projekti määritetään siten, että sen PWP-prosentti osuus on 100 prosenttia.

Toimittaja lähettää sinulle 100 tietokonetta, joihin on asennettu ohjelmisto, sekä laskun 10 000,00 USD. Koska PWP-termit määritetään projektia varten, et maksa toimittajalle, kun olet saanut tietokoneet. Sen sijaan lähetät tietokoneet asiakkaalle sekä laskun 15 000,00. Asiakas tutkii tietokoneet ja hyväksyy projektilaskun koko määrän.

Kun olet saanut täyden maksun asiakkaalta, maksat toimittajalle 10 000,00, toimittajan laskun koko summan.

## <a name="set-up-pwp-terms-for-a-project"></a>Projektin PWP-termien määrittäminen

Kun määrität projektille PWP-ehdot, sinun täytyy määrittää prosentteina vähimmäissumma, joka asiakkaan on maksettava projektista, ennen kuin maksat toimittajalle. Raja-arvo lasketaan automaattisesti projektin myyntilaskuihin. Seuraavien vaiheiden mukaisesti voit määrittää PWP-termien kynnysprosentin.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.
2. Etsi ja avaa projekti, jolle haluat määrittää PWP-ehdot.
3. Valitse **toimittajasopimukset**-pikavälilehdessä **Lisää rivi**.
3. Valitse **tilikoodi**-kentässä jokin seuraavista vaihtoehdoista:

    - **Taulukko** – PWP-ehdot koskevat yhtä toimittajaa.
    - **Ryhmä** – PWP-ehdot koskevat kaikkia toimittajaryhmän toimittajia.
    - **Kaikki** – PWP-ehdot koskevat kaikkia toimittajia.

4. Jos valitsit edellisessä vaiheessa **taulukon** tai **ryhmän**, valitse **toimittaja-/toimittajaryhmä**-kentässä toimittaja- tai toimittajaryhmä, johon PWP-termit liittyvät. Jos valitsit edellisessä vaiheessa **Kaikki**, **toimittaja-/toimittajaryhmä**-kenttää ei voi muokata.
5. Jos toimittajan pidätysehdot on määritetty toimittajalle projektissa, valitse **toimittajan säilytysehdot** -kentässä säilytysehtojen sääntötunnus.
6. Kirjoita **PWP-kynnysprosentti**-kenttään projektin kynnysprosentti. Projektille määrittämäsi prosenttiosuus määrittää vähimmäishinnan, joka asiakkaan on maksettava, ennen kuin maksat toimittajalle.

## <a name="create-a-po-that-has-pwp-terms"></a>Luo ostotilaus, jolla on PWP-termit

Kun kirjaat laskun toimittajalta, jos toimittajalle on asetettu PWP-ehtoja. Nämä termit näkyvät ostotilausriveillä. Jos haluat luoda ostotilauksen, jossa on PWP-termit, toimi seuraavasti.

1. Siirry kohtaan **ostaminen ja hankinta** \> **Ostotilaukset** \> **Kaikki ostotilaukset**.
2. Valitse toimintoruudussa **Uusi**. Kirjoita sitten **Luo ostotilaus** -valintaikkunaan tarvittavat tiedot ja valitse **OK**.

    Vaihtoehtoisesti voit avata aiemmin luodun ostotilauksen **Kaikki tilaukset** -luettelosivulla.

4. Tarkista **ostotilaus**-sivun **Ostotilauksen rivit** -pikavälilehdessä myyntitilausrivin tiedot. **Maksa, kun maksettu** -asetus valitaan automaattisesti, ja **PWP-kynnysprosentti**-kentän arvo kopioidaan automaattisesti **Projektit**-sivun **PWP-kynnysprosentti**-kentästä.
6. Jos et halua käyttää PWP-ehtoja ostotilausrivin toimittajalle, tyhjennä **maksu, kun maksettu** -vaihtoehto. Tässä tapauksessa ostotilausrivin **PWP-kynnysprosentti**-kentän arvoksi palautetaan 0 (nolla).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Asiakkaan maksun päivittäminen ja toimittajan maksaminen

Kun toimittaja suorittaa projektissa työnsä ja lähettää sinulle laskun, tarkista projektin tila ja myyntilaskut ja selvitä, onko projektin PWP-ehdot täytetty. Jos toimittajan PWP-ehdot täyttyvät, voit määrittää, mitkä toimittajan laskun rivit maksetaan projektin asiakasmaksujen perusteella. Jos päätät maksaa toimittajalle, vaikka PWP-ehdot eivät täyttyisikään, voit korvata toimittajan laskussa olevat PWP-ehdot **Toimittajan maksu kun maksettu** -sivulla.

1. Siirry kohtaan **projektinhallinta ja kirjanpito** \> **kyselyt ja raportit** \> **pidätyskyselyt** \> **toimittajan lasku maksetaan kun maksettu**.
2. Jos kyseessä on **toimittajan lasku, joka maksetaan kun on maksettu** -sivu, kirjoita hakukenttään arvot löytääksesi toimittajan laskun, jota haluat tarkastella, ja valitse sitten **Hae**.
3. Valitse **toimittajan laskun rivit** -pikavälilehden rivit, joita haluat muuttaa.
4. Jos laskun rivillä **maksetaan, kun maksu ehdot täyttyvät**, valitse **Vapauta toimittajan maksu**. **Maksu, kun maksettu** -asetus on poistettu, ja **valmis maksettavaksi** -kentän arvoksi vaihdetaan **Kyllä**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]