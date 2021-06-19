---
title: Keskeneräisen laskutuksen hallinta
description: Tässä aiheessa on tietoja siitä, miten laskutusruuhkaa voidaan tarkastella ja käsitellä Project Operationsissa.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7c242937cd9dd277f8d92b7a29333c1fa272e5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011907"
---
# <a name="manage-billing-backlog"></a>Keskeneräisen laskutuksen hallinta

**Käytetään**: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

Dynamics 365 Project Operationsissa on näkymiä, jotka on tarkoitettu nimenomaan keskeneräisen laskutuksen hallintaan. Keskeneräistä laskutusta voi hallita valitsemalla linkkejä **Myynti**-alueen **Laskutus**-kohdassa. 

Seuraavat näkymät ovat käytettävissä:

- Ennakkomaksut ja ennakot
- Käytettävissä olevat ennakkomaksut ja ennakot
- Kiinteän hinnan välitavoitteet
- Keskeneräiset ajan ja materiaalin laskutukset

## <a name="retainers-and-advances"></a>Ennakkomaksut ja ennakot

**Ennakkomaksut ja ennakot** -näkymässä luetellaan ennakkomaksut ja ennakot kaikista projektisopimuksista. Kun ennakkomaksu tai ennakko on laskutettu, ennakon summa vapautuu käytettäväksi.

## <a name="available-retainers-and-advances"></a>Käytettävissä olevat ennakkomaksut ja ennakot

**Käytettävissä olevat ennakkomaksut ja ennakot** -näkymässä luetellaan kaikki käytettävissä olevat ennakkomaksut ja ennakot kaikista projektisopimuksista. Kun ennakkomaksu tai ennakko on laskutettu, ennakon summa vapautuu käytettäväksi ja se lisätään luetteloon. Kun ennakkomaksu on käytetty kokonaan, se poistuu luettelosta.

## <a name="fixed-price-milestones"></a>Kiinteän hinnan välitavoitteet

**Kiinteän hinnan välitavoitteet** -näkymässä luetellaan kaikki kaikkien projektisopimusrivien kiinteän hinnan välitavoitteet. Tässä näkymässä yhden tai usean välitavoitteen voi merkitä **Valmiina laskutettavaksi** tai **Ei valmis laskutettavaksi**. Kun välitavoitteen merkintänä on **Valmis laskutettavaksi**, se voidaan sijoittaa luonnoslaskuun.

Jos usean asiakkaan sopimusrivien laskutapana on kiinteä hinta, kullekin sopimusrivin asiakkaalle luodaan välitavoite. Välitavoite voidaan luoda ja sitten jakaa yksittäisiin asiakaskohtaisiin välitavoitetietueisiin. Tämä jako on sisäinen ja se noudattaa kullekin asiakkaalle sopimusrivillä määritettyä laskutuksen jakoprosenttia. Yksittäiset asiakaskohtaiset välitavoitetietueet ovat näkyvissä **Kiinteän hinnan välitavoitteet** -näkymässä. Kukin näistä välitavoitetietueista voidaan merkitä **valmiiksi laskutettavaksi** erillään tästä näkymästä. Kun yksi tai useampi liittyvistä välitavoitteista merkitään **Valmis laskutettavaksi**, otsikon tila päivittyy arvoksi **Käynnissä** tilasta **Ei aloitettu**. Kun kaikki välitavoitteet on laskutettu, otsikon välitavoitteen tilaksi päivittyy **Valmis**.

Tässä näkymässä näkyy luonnoslaskun välitavoite, joka sisältää **luodun asiakaslaskun** laskutuksen tilan. Kun luonnoslasku vahvistetaan, tietueen laskutuksen tilaksi päivitetään **Asiakaslasku kirjattu**. 

> [!NOTE] 
> Älä päivitä tätä tila-arvoa käyttämällä mukautettua koodia. Project Operations ei toimi oikein, jos nämä tila-arvot päivitetään mukautetulla koodilla.

## <a name="time-and-material-billing-backlog"></a>Keskeneräiset ajan ja materiaalin laskutukset

**Keskeneräiset ajan ja materiaalin laskutukset** -näkymässä on luettelo sellaisista järjestelmässä olevista kaikkien projektien laskuttamattomista myynnin todellisista arvoista, joita ei ole laskutettu. Yhden tai usean laskuttamattoman toteutuneen myynnin voi merkitä **valmiiksi laskutettaviksi** tai **ei valmis laskutettavaksi** tästä näkymästä. Laskuttamattomien myynti todellisten tietojen merkitseminen **valmiiksi laskutettavaksi** mahdollistaa sen, että se voidaan siirtää luonnoslaskuun.

Sellaisiin laskuttamattomiin myynnin todellisiin arvoihin, joiden **Ei-ylitettävän rajoitus** -tila on **Epäonnistui**, ei voi käyttää merkintää **Valmis laskutettavaksi**. Jos todelliset arvot on merkittävä **Valmis laskutettavaksi**, nollaa muiden vahvistettujen todellisten arvojen tila sopimusrivillä ja arvioi sitten uudelleen **Älä ylitä** -tila.

Jos monen asiakkaan sopimusrivien laskutustapana on aika ja materiaali, aikaa ja kuluja hyväksyttäessä yksi laskuttamaton myynnin todellinen arvo luodaan kullekin sopimusrivin asiakkaalle kullekin asiakkaalle määritetyn laskutuksen jakoprosentin mukaisesti. Nämä yksittäiset asiakaskohtaiset laskuttamattomat myynnin todelliset arvot näkyvät **Keskeneräiset ajan ja materiaalin laskutukset** -näkymässä. Kukin näistä laskuttamattomista toteutuneista myynneistä voidaan merkitä **valmiiksi laskutettavaksi** erillään tästä näkymästä.

Laskuluonnokseen merkitty laskuttamaton myynti näkyy tässä näkymässä laskutustilassa **Luotu asiakaslasku**. Kun luonnoslasku on vahvistettu, tämän tietueen laskutuksen tilaksi päivittyy **Asiakaslasku kirjattu**. 

> [!NOTE] 
> Älä päivitä tätä tila-arvoa käyttämällä mukautettua koodia. Project Operations ei toimi oikein, jos nämä tila-arvot päivitetään mukautetulla koodilla.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
