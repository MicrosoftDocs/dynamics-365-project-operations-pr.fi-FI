---
title: ALV:n palautus
description: Tässä aiheessa kerrotaan, miten voit saada hyvityksiä arvonlisäverotapahtumista.
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20e29a47d73d28c0bf8dbb3495ad301481c529cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993592"
---
# <a name="vat-recovery"></a>ALV:n palautus 

Saadakseen hyvityksiä hyväksyttävistä arvonlisäverotapahtumista yrityksen tai organisaation on määritettävä, kerättävä, tarkistettava ja lähetettävä tarkkoja tietoja. Tämä prosessi sisältää useita tehtäviä, ja yrityksen koosta riippuen se voi sisältää useita työntekijöitä tai rooleja.

Jos haluat palauttaa arvonlisäveron kulujenhallintamoduulissa, seuraavat edellytykset on täytettävä:

- Kululuokkiin kohdistetuista maille/alueille on luotava verokoodit.
- Kullekin verokoodille on luotava arvonlisäveroryhmä.
- Kullekin ALV-ryhmälle on luotava nimikeverokoodi.

Kun edellytykset on täytetty, työntekijöiden on suoritettava seuraavat vaiheet, jotta voit pyytää hyvitystä ALV-tapahtumille.

1. Kirjoita kuluraporttiin luottokorttitapahtumien verotiedot, jotta voit määrittää kelpoiset ALV-palautukset.
2. Varmista, että kaikki verotiedot ovat täydelliset, ja kirjaa sitten kuluraportti.
3. Käsittele kulut, jotka kelpaavat kansainväliseen ALV-palautukseen.
4. Lähetä ALV-palautustiedot kolmannelle osapuolelle, jotta voit määrittää kansainväliset palautukset.
5. Käsittele kotimaisten kulujen ALV-palautuksia.

Seuraavissa osissa on esimerkkejä siitä, miten Contoso-yrityksen työntekijät suorittavat kunkin vaiheen.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Kirjoita kuluraporttiin luottokorttitapahtumien verotiedot, jotta voit määrittää kelpoiset ALV-palautukset

Nancy on Yhdysvalloissa sijaitseva Contoso-yrityksen myyntiedustaja, joka palasi äskettäin myyntimatkalta Yhdistyneestä kuningaskunnasta. Matkan aikana hän aiheutti joitakin henkilökohtaisia luottokorttikuluja aterioissa. Nancyn on nyt luotava kuluraportti kulujen täsmäyttämiseksi.

Kun Nancy syöttää tiedot kuluraporttiin, hän valitsee **Yhdistynyt kuningaskunta** **Muokkaa kuluraporttia** -sivun **Maa/alue**-kentässä. Tämän jälkeen arvonlisäveroryhmien luettelo suodatetaan niin, että siinä näkyvät vain ne ryhmät, jotka koskevat Yhdistynyttä kuningaskuntaa. Nancy valitsee **Yhdistynyt kuningaskunta 001** -arvonlisäveroryhmän ja valitsee sitten **Ateriat**-nimikearvonlisäveroryhmän. Seuraavaksi hän lisää uuden majoitustapahtuman. Koska Yhdistyneessä kuningaskunnassa on vain yksi arvonlisäveroryhmä ja yksi nimikearvonlisäveroryhmä majoittukselle, nämä tiedot täytetään automaattisesti Nancyn kuluraporttiin.

Kaikilla kuluilla on oltava vastaava vastaanottaja Contoso-yrityksen käytännön mukaisesti. Tämän vuoksi, kun Nancy tallentaa kuluraporttinsa, hän saa sanoman, jonka mukaan hänen on liitettävä kuitti jokaisesta tapahtumasta, jonka hän on luetellut kuluraportissaan. Nancy varmistaa, että hän on liittänyt jokaisen tapahtuman kuitin digitaalisen kuvan kuluraporttiin ja lähettää sitten raportin hyväksyttäväksi. Tämän jälkeen hän lähettää paperikuitit toimiston käsittelyryhmälle. Tämä ryhmä lähettää ALV-palautustiedot ulkopuoliselle toimittajalle, joka tallentaa kansainväliset ALV-palautustiedot Contoso-yrityksen puolesta.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Varmista, että kaikki verotiedot ovat täydelliset, ja kirjaa sitten kuluraportti

April on Contoso-yrityksen ostoreskontrakoordinaattori, jonka on syötettävä kaikki kuluraportista puuttuvat verotiedot ennen kuin raportti voidaan kirjata. Hän avaa **Kuluraportin tiedot** -sivun ja näkee Nancyn hyväksytyn kuluraportin. april avaa kuluraportin tarkastellakseen tapahtumien tietoja. Hän näkee, että Nancy ei ole antanut yhden tapahtuman nimikearvonlisäveroryhmää. Koska nämä tiedot eivät ole käytettävissä, April ei voi kirjata kuluraporttia. Tämän vuoksi April tarkastelee **Veromääritykset**-sivua kulujen hallinnassa ja etsii maalle/alueelle ja tapahtumatyypille sopivan nimikearvonlisäveroryhmän. April voi nyt kirjata kuluraportin pääkirjanpitoon.

Kun April kirjaa kuluraportin, luodaan palautettavissa oleva ALV-työnimike. Tämä työnimike delegoidaan toimiston käsittelyryhmän jäsenelle. April vastaanottaa viestin, joka vahvistaa, että kirjaus onnistui. Tässä sanomassa näkyy myös palautuksessa tunnistettujen ALV-tapahtumien määrä.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Käsittele kulut, jotka kelpaavat kansainväliseen ALV-palautukseen

Arnie on Contoso-yrityksen taustakäsittelyryhmän jäsen, jonka vastuulla on vahvistaa, että kuluraportit sisältävät kaikki pakolliset ALV-palautustiedot. Hän avaa **Kulun veronpalautus** -sivun ja valitsee Nancyn lähettämän kuluraportin. Arnie tarkistaa, että kaikki pakolliset kuitit on liitetty ja että oikeat arvonlisäveroryhmän ja nimikearvonlisäveron koodit on syötetty.

Kun Arnie vastaanottaa paperikuitit Nancylta, hän tarkistaa paperikuitit digitaalisia kuitteja vastaan ja muuttaa sitten kuluraportin tilaksi **Valmis palautettavaksi**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Lähetä ALV-palautustiedot kolmannelle osapuolelle, jotta voit määrittää kansainväliset palautukset

Kun Arnie on valmis lähettämään kuluraportin tiedot kolmannelle osapuolelle, joka määrittää ALV-palautuksen, hän avaa **Kulun veronpalautus** -sivun. Hän suodattaa sivun niin, että siinä näkyvät vain ne kuluraportit, jotka on merkitty **Valmis palautettavaksi**. Arnie valitsee sitten **Tiedosto** &gt; **Vie Exceliin**. Kuluraporttien ALV-tiedot viedään Microsoft Excel -laskentataulukkoon. Arnie lähettää tämän laskentataulukon kolmannelle osapuolelle ja sisällyttää sanoman, jonka mukaan paperikuitit on lähetetty kuriiripostina.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Käsittele kotimaisten kulujen ALV-palautuksia

Arnien on tarkistettava, että kuluraportin tapahtumat ovat oikeutettuja ALV-palautukseen ja että digitaaliset kuitit on liitetty raportteihin. Aloittaakseen kotimaisen palautuksen kelpoisten kulujen käsittelemisen, Arnie Avaa **Kulun veronpalautus** -sivun ja valitsee kuluraportin, joka edellyttää vahvistusta. Hän tarkistaa, että kuitit ovat yrityksen nimissä sen sijaan että ne olisivat työntekijän nimissä. Jos kyseessä on ALV-palautus, kuittien on oltava yrityksen nimissä. Tämän jälkeen Arnie vahvistaa, että oikeat arvonlisäveroryhmän ja nimikkeen arvonlisäverokoodit on otettu käyttöön.

Kun Arnie vastaanottaa paperikuitit, hän muuttaa kuluraportin tilaksi **Valmis palautettavaksi**. Hän voi sitten määrittää palautuksen asianmukaisen veroviranomaisen kanssa. Tässä tapauksessa asianmukainen veroviranomainen Yhdysvalloissa on Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]