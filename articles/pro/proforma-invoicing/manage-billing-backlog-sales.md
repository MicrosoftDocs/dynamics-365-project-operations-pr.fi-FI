---
title: Keskeneräisen projektilaskutuksen hallinta
description: Tässä aiheessa on tietoja erilaisista näkymistä, jotka ovat käytettävissä projektien laskutuksen jonon hallinnassa.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 27ef2ae90778394d15b979a13215c8f5af483cda0312682e9fc7256b8282b999
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988287"
---
# <a name="manage-project-billing-backlog"></a>Keskeneräisen projektilaskutuksen hallinta 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa on näkymiä, jotka on tarkoitettu nimenomaan keskeneräisen laskutuksen hallintaan. Keskeneräistä laskutusta voi hallita valitsemalla linkkejä **Myynti**-alueen **Laskutus**-kohdassa. 

Seuraavat näkymät ovat käytettävissä:

- Ennakkomaksut ja ennakot
- Käytettävissä olevat ennakkomaksut ja ennakot
- Kiinteän hinnan välitavoitteet
- Tuotteiden keskeneräiset laskutukset
- Keskeneräiset ajan ja materiaalin laskutukset

## <a name="retainers-and-advances"></a>Ennakkomaksut ja ennakot

**Ennakkomaksut ja ennakot** -näkymässä on luettelo kaikkien järjestelmässä olevien projektisopimusten kaikista ennakkomaksuista ja ennakoista. Kun ennakkomaksu tai ennakko on laskutettu, ennakon summa vapautuu käytettäväksi.

## <a name="available-retainers-and-advances"></a>Käytettävissä olevat ennakkomaksut ja ennakot

**Käytettävissä olevat ennakkomaksut ja ennakot** -näkymässä on luettelo kaikkien järjestelmässä olevien projektisopimusten kaikista käytettävissä olevista ennakkomaksuista ja ennakoista. Kun ennakkomaksu tai ennakko on laskutettu, ennakon summa vapautuu käytettäväksi ja se lisätään luetteloon. Kun ennakkomaksun tai ennakon summan on käytetty kokonaan, se poistetaan luettelosta.

## <a name="fixed-price-milestones"></a>Kiinteän hinnan välitavoitteet

**Kiinteän hinnan välitavoitteet** -näkymässä on luettelo kaikkien järjestelmässä olevien projektien kaikista kiinteähintaisista välitavoitteista. Tässä näkymässä yhteen tai useaan välitavoitteeseen voi valita merkinnäksi **Valmis laskutettaviksi** tai **Ei valmis laskutettavaksi**. Kun välitavoitteen merkintänä on **Valmis laskutettavaksi**, se voidaan sijoittaa luonnoslaskuun.

Jos usean asiakkaan sopimusrivien laskutapana on kiinteä hinta, kullekin sopimusrivin asiakkaalle luodaan välitavoite. Välitavoite voidaan luoda ja sitten jakaa yksittäisiin asiakaskohtaisiin välitavoitetietueisiin. Tämä jako on sisäinen ja se noudattaa kullekin asiakkaalle sopimusrivillä määritettyä laskutuksen jakoprosenttia. Yksittäiset asiakaskohtaiset välitavoitetietueet ovat näkyvissä **Kiinteän hinnan välitavoitteet** -näkymässä. Kukin näistä välitavoitetietueista voidaan merkitä **valmiiksi laskutettavaksi** erillään tästä näkymästä. Jos vähintään yhden liittyvän välitavoitejaon merkintä on **Valmis laskutettavaksi**, otsikon tila **Ei aloitettu** päivittyy tilaan **Kesken**. Kun kaikki välitavoitejaot on laskutettu, otsikon välitavoitteen tilaksi päivitetään **Valmis**.

Tässä näkymässä näkyy luonnoslaskun välitavoite, joka sisältää **luodun asiakaslaskun** laskutuksen tilan. Kun luonnoslasku vahvistetaan, tietueen laskutuksen tilaksi päivitetään **Asiakaslasku kirjattu**. Älä päivitä tätä tila-arvoa mukautetulla koodilla. Project Operations ei toimi oikein, jos nämä tila-arvot päivitetään mukautetulla koodilla.

## <a name="product-billing-backlog"></a>Tuotteiden keskeneräiset laskutukset

**Tuotteiden keskeneräiset laskutukset** -näkymässä on luettelo kaikkien järjestelmässä olevien projektisopimusten kaikista tuotepohjaisista sopimusriveistä. Tässä näkymässä yhden tai usean tuotepohjaisen sopimusrivin merkinnäksi voi valita **Valmis laskutettaviksi** tai **Ei valmis laskutettavaksi**. Kun tuotepohjaisen sopimusrivin merkintänä on **Valmis laskutettavaksi**, se voidaan sijoittaa luonnoslaskuun.

Luonnoslaskussa olevan tuotepohjaisen sopimusrivin laskutuksen tilana näytetään tässä näkymässä **Asiakaslasku luotu**. Kun luonnoslasku on vahvistettu, tämän tietueen laskutuksen tilaksi päivittyy **Asiakaslasku kirjattu**. Älä päivitä tätä tila-arvoa mukautetulla koodilla. Project Operations ei toimi oikein, jos nämä tila-arvot päivitetään mukautetulla koodilla.

## <a name="time-and-material-billing-backlog"></a>Keskeneräiset ajan ja materiaalin laskutukset

**Keskeneräiset ajan ja materiaalin laskutukset** -näkymässä on luettelo sellaisista järjestelmässä olevista kaikkien projektien laskuttamattomista myynnin todellisista arvoista, joita ei ole laskutettu. Yhden tai usean laskuttamattoman toteutuneen myynnin voi merkitä **valmiiksi laskutettaviksi** tai **ei valmis laskutettavaksi** tästä näkymästä. Laskuttamattomien myynti todellisten tietojen merkitseminen **valmiiksi laskutettavaksi** mahdollistaa sen, että se voidaan siirtää luonnoslaskuun.

Sellaisiin laskuttamattomiin myynnin todellisiin arvoihin, joiden **Ei-ylitettävän rajoitus** -tila on **Epäonnistui**, ei voi käyttää merkintää **Valmis laskutettavaksi**. Jos todellisten arvojen merkinnän on oltava **Valmis laskutettavaksi**, nollaa muiden sopimusrivillä vahvistettujen todellisten arvojen tila ja arvioi **Ei-ylitettävän rajoitus** -tila uudelleen.

Jos monen asiakkaan sopimusrivien laskutustapana on aika ja materiaali, aikaa ja kuluja hyväksyttäessä yksi laskuttamaton myynnin todellinen arvo luodaan kullekin sopimusrivin asiakkaalle kullekin asiakkaalle määritetyn laskutuksen jakoprosentin mukaisesti. Nämä yksittäiset asiakaskohtaiset laskuttamattomat myynnin todelliset arvot näkyvät **Keskeneräiset ajan ja materiaalin laskutukset** -näkymässä. Kukin näistä laskuttamattomista toteutuneista myynneistä voidaan merkitä **valmiiksi laskutettavaksi** erillään tästä näkymästä.

Luonnoslaskussa olevan laskuttamattoman myynnin todellisen arvon laskutuksen tilana näytetään tässä näkymässä **Asiakaslasku luotu**. Kun luonnoslasku on vahvistettu, tämän tietueen laskutuksen tilaksi päivittyy **Asiakaslasku kirjattu**. Älä päivitä tätä tila-arvoa mukautetulla koodilla. Project Operations ei toimi oikein, jos nämä tila-arvot päivitetään mukautetulla koodilla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
