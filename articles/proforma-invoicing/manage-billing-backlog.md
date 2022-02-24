---
title: Keskeneräisen laskutuksen hallinta
description: Tässä aiheessa on tietoja siitä, miten laskutusruuhkaa voidaan tarkastella ja käsitellä Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122339"
---
# <a name="manage-the-billing-backlog"></a>Keskeneräisen laskutuksen hallinta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsilla on kaksi erillistä näkymää, joiden avulla voit käsitellä ja hallita laskutuksen ruuhkaa. Ne ovat **kiinteähintaisia välitavoitteita** sekä **aika- ja materiaalilaskutuksen tilauskanta**, jos haluat valita näkymän, valitse projektitoimintojen **myynti**-alueessa vasemmalla siirtymissivulla **laskutus**. Laskutuksen ruuhkan linkit tallennetaan tähän.

## <a name="fixed-price-milestones"></a>Kiinteän hinnan välitavoitteet

Tässä näkymässä näkyvät kaikki järjestelmän projektisopimusrivien kiinteät hinnan välitavoitteet. Yhden tai usean välitavoitteen voi merkitä **valmiiksi laskutettaviksi** tai **ei valmis laskutettavaksi** tästä näkymästä. Kun merkitset välitavoitteen **valmiiksi laskutettavaksi**, välitavoite on käytettävissä laskuluonnoksena.

Kun usean asiakkaan sopimusriveillä on kiinteämääräinen laskutusmenetelmä, jokaiselle sopimusrivin asiakkaalle luodaan yksi välitavoite. Käyttäjä luo välitavoitteen ja välitavoite on jaettu asiakkaaseen = tietyt välitavoitetietueet sisäisesti kunkin sopimusrivin asiakkaan kullekin asiakkaalle määrittämän laskutusprosentin mukaan. **Kiinteähintaiset välitavoitteet** -näkymässä näkyvät yksittäiset asiakaskohtaiset välitavoitetietueet. Kukin näistä välitavoitetietueista voidaan merkitä **valmiiksi laskutettavaksi** erillään tästä näkymästä. Kun vähintään yksi toisiinsa liittyvä välitavoitteen jako on merkitty **valmiiksi laskutettavaksi**, otsikko siirtää sen tilaan, jossa se on **keskeneräinen** tilasta **ei aloitettu**. Kun kaikki välitavoitteen jaot on laskutettu, otsikon välitavoitteen tila on **valmis**.

Tässä näkymässä näkyy luonnoslaskun välitavoite, joka sisältää **luodun asiakaslaskun** laskutuksen tilan. Kun luonnoslasku on vahvistettu, tämän tietueen laskutuksen tila päivittyy laskuun, joka on **kirjattu**. Tämän tilan arvon päivittämistä mukautettua koodia käyttämällä ei suositella. Project Operations ei toimi oikein, jos näihin tila-arvoihin päivitetään mukautettua koodia.

## <a name="time-and-material-billing-backlog"></a>Keskeneräiset ajan ja materiaalin laskutukset

Tässä näkymässä luetellaan kaikki laskuttamattomat myynnin todelliset arvot, joita ei ole laskutettu kaikissa järjestelmässä olevissa projektisopimuksissa. Yhden tai usean laskuttamattoman toteutuneen myynnin voi merkitä **valmiiksi laskutettaviksi** tai **ei valmis laskutettavaksi** tästä näkymästä. Laskuttamattomien myynti todellisten tietojen merkitseminen **valmiiksi laskutettavaksi** mahdollistaa sen, että se voidaan siirtää luonnoslaskuun.

Laskuttamattomia toteutuneita myyntejä, joiden **ei saa ylittää** -tila on **epäonnistunut** voi merkitä **valmiiksi laskutettavaksi**. Jos nämä toteutuneet arvot on merkittävä sellaisenaan, palauta niiden sopimusrivin muiden todellisten arvojen tila, jotka on vahvistettu, ja arvioi sitten **ei saa ylittää** -tila.

Jos kyseessä on usean asiakkaan sopimusrivi, jolla on ajan ja materiaalin laskutustapa, kun ajan ja kulujen hyväksyminen on tehty, jokaiselle sopimusrivillä olevalle asiakkaalle luodaan laskuttamaton todellisen myynnin sopimusrivi kullekin asiakkaalle määritetyn laskutusprosentin mukaan. **Aika- ja materiaalilaskutuksen ruuhkan** näkymässä näkyvät yksittäiset asiakaskohtaiset laskuttamattomat toteutuneet myynnit. Kukin näistä laskuttamattomista toteutuneista myynneistä voidaan merkitä **valmiiksi laskutettavaksi** erillään tästä näkymästä.

Tässä näkymässä näkyy luonnoslaskun välitavoite, joka sisältää **luodun asiakaslaskun** **laskutuksen tilan**. Kun luonnoslasku on vahvistettu, tämän tietueen laskutuksen tilaksi päivittyy **Asiakaslasku kirjattu**. Tämän tilan arvon päivittämistä, kun se on tässä tilassa, mukautettua koodia käyttämällä ei suositella. Project Operations ei toimi oikein, kun näihin tila-arvoihin päivitetään mukautettua koodia.
