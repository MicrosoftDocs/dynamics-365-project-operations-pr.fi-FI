---
title: ALV-palautus kulujen hallinnassa
description: Tässä aiheesa kerrotaan, miten voit saada hyvityksiä hyväksyttävistä arvonlisäverotapahtumista.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075216"
---
# <a name="vat-recovery-in-expense-management"></a>ALV-palautus kulujen hallinnassa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Saadakseen hyvityksiä hyväksyttävistä arvonlisäverotapahtumista yrityksen tai organisaation on määritettävä, kerättävä, tarkistettava ja lähetettävä tarkkoja tietoja. Tämä prosessi sisältää useita tehtäviä, ja yrityksen koosta riippuen se voi sisältää useita työntekijöitä tai rooleja.

Jos haluat palauttaa arvonlisä veron **Kulujen hallinta** moduulissa, seuraavat edellytykset on täytettävä:

- Kululuokkiin kohdistetuista maille/alueille on luotava verokoodit.
- Kullekin verokoodille on luotava arvonlisäveroryhmä.
- Kullekin ALV-ryhmälle on luotava nimikeverokoodi.

Kun edellytykset on täytetty, on suoritettava seuraavat vaiheet, jotta voit pyytää hyvitystä ALV-tapahtumille.

1. Kirjoita kuluraporttiin luottokorttitapahtumien verotiedot, jotta voit määrittää kelpoiset ALV-palautukset.
2. Tarkista, että kaikki verotiedot ovat täydelliset, ja kirjaa sitten kuluraportti.
3. Käsittele kulut, jotka kelpaavat kansainväliseen ALV-palautukseen.
4. Lähetä ALV-palautustiedot kolmannelle osapuolelle, jotta voit määrittää kansainväliset palautukset.
5. Käsittele kotimaisten kulujen ALV-palautuksia.

Seuraavissa osissa on esimerkkejä siitä, miten Contoson työntekijät suorittavat kunkin vaiheen.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Anna luottokorttitapahtumien verotiedot, jotta voit määrittää kelpoiset ALV-palautukset

Yhdysvalloissa sijaitseva Contoson myyntiedustaja Nancy on vastikään palannaut myyntimatkalta Yhdistyneeseen kuningaskuntaan. Matkan aikana Nancy aiheutti joitakin henkilökohtaisia luottokorttikuluja aterioissa. Nancyn on nyt luotava kuluraportti kulujen täsmäyttämiseksi.

Kun Nancy syöttää tiedot kuluraporttiin, hän valitsee **Yhdistynyt kuningaskunta** **Muokkaa kuluraporttia** -sivun **Maa/alue** -kentässä. Tämän jälkeen arvonlisäveroryhmien luettelo suodatetaan niin, että siinä näkyvät vain ne ryhmät, jotka koskevat Yhdistynyttä kuningaskuntaa. Nancy valitsee **Yhdistynyt kuningaskunta 001** -arvonlisäveroryhmän ja valitsee sitten **Ateriat** -nimikearvonlisäveroryhmän. Seuraavaksi Nancy lisää uuden majoitustapahtuman. Koska Yhdistyneessä kuningaskunnassa on vain yksi arvonlisäveroryhmä ja yksi nimikearvonlisäveroryhmä majoittukselle, nämä tiedot täytetään automaattisesti Nancyn kuluraporttiin.

Contoson käytännön mukaan kaikissa kuluissa on oltava täsmäävä kuitti. Tämän vuoksi, kun Nancy tallentaa kuluraportin, hän saa sanoman, jonka mukaan hänen on liitettävä kuitti jokaisesta tapahtumasta, jonka hän on luetellut kuluraportissaan. Nancy varmistaa, että hän on liittänyt jokaisen tapahtuman kuitin digitaalisen kuvan kuluraporttiin ja lähettää sitten raportin hyväksyttäväksi. Tämän jälkeen hän lähettää paperikuitit toimiston käsittelyryhmälle. Tämä ryhmä lähettää ALV-palautustiedot kolmannen osapuolen toimittajalle, joka määrittää kansainvälisen arvonlisäveron palautuksen Contosolle.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Verotietojen tarkistaminen ja kuluraportin kirjaaminen

Ennen kuin Contoson ostoreskontran koordinaattori April voi kirjata kuluraportin, hänen on annettava kaikki puuttuvat verotiedot. Hän avaa **Kuluraportin tiedot** -sivun ja näkee Nancyn hyväksytyn kuluraportin. april avaa kuluraportin tarkastellakseen tapahtumien tietoja. Hän näkee, että Nancy ei ole antanut yhden tapahtuman nimikearvonlisäveroryhmää. Koska nämä tiedot eivät ole käytettävissä, April ei voi kirjata kuluraporttia. Tämän vuoksi hän tarkastelee **Vero määritykset** -sivua kulujen hallinnassa ja etsii maalle/alueelle ja tapahtumatyypille sopivan nimikearvonlisäveroryhmän. April voi nyt kirjata kuluraportin pääkirjanpitoon.

Kun April kirjaa kuluraportin, luodaan palautettavissa oleva ALV-työnimike. Tämä työnimike delegoidaan toimiston käsittelyryhmän jäsenelle. April vastaanottaa viestin, joka vahvistaa, että kirjaus onnistui. Tässä sanomassa näkyy myös palautuksessa tunnistettujen ALV-tapahtumien määrä.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Käsittele kulut, jotka kelpaavat kansainväliseen ALV-palautukseen

Arnie, Contoson käsittelyryhmän jäsen, vastaa siitä, että kaikki tarvittavat ALV-palautuksen tiedot sisältyvät kuluraportteihin. Hän avaa **Kulun veronpalautus** -sivun ja valitsee Nancyn lähettämän kuluraportin. Tämän jälkeen Arnie tarkistaa, että kaikki pakolliset kuitit on liitetty ja että oikeat arvonlisäveroryhmän ja nimikearvonlisäveron koodit on syötetty.

Kun Arnie vastaanottaa paperikuitit Nancylta, hän tarkistaa ne digitaalisia kuitteja vastaan ja muuttaa sitten kuluraportin tilaksi **Valmis palautettavaksi**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Lähetä ALV-palautustiedot kolmannen osapuolen toimittajalle

Kun Arnie on valmis lähettämään kuluraportin tiedot kolmannelle osapuolelle, joka määrittää ALV-palautuksen, hän avaa **Kulun veronpalautus** -sivun. Hän suodattaa sivun niin, että siinä näkyvät vain ne kuluraportit, jotka on merkitty **Valmis palautettavaksi**. Arnie valitsee sitten **Tiedosto** &gt; **Vie Exceliin**. Kuluraporttien ALV-tiedot viedään Microsoft Excel -laskentataulukkoon. Arnie lähettää tämän laskentataulukon kolmannelle osapuolelle ja sisällyttää sanoman, jonka mukaan paperikuitit on lähetetty kuriiripostina.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Käsittele kotimaisten kulujen ALV-palautuksia

Arnien on tarkistettava, että kuluraportin tapahtumat ovat oikeutettuja ALV-palautukseen ja että digitaaliset kuitit on liitetty raportteihin. Aloittaakseen kotimaisen palautuksen kelpoisten kulujen käsittelemisen, Arnie Avaa **Kulun veronpalautus** -sivun ja valitsee kuluraportin, joka edellyttää vahvistusta. Hän tarkistaa, että kuitit ovat yrityksen nimissä sen sijaan että ne olisivat työntekijän nimissä. (ALV-apalautuksessa kuitit on altava yrityksen nimellä.) Tämän jälkeen Arnie tarkistaa, että kaikki pakolliset kuitit on liitetty ja että oikeat arvonlisäveroryhmän ja nimikearvonlisäveron koodit on syötetty.

Kun Arnie vastaanottaa paperikuitit, hän muuttaa kuluraportin tilaksi **Valmis palautettavaksi**. Hän voi sitten määrittää palautuksen asianmukaisen veroviranomaisen kanssa. Tässä tapauksessa asianmukainen veroviranomainen Yhdysvalloissa on Internal Revenue Service (IRS).
