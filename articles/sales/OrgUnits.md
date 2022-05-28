---
title: Organisaatioyksiköt
description: Tässä aiheessa kuvataan organisaatioyksiköiden käsitettä ja selostetaan organisaatioyksiköiden luontia ja ylläpitoa Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581372"
---
# <a name="organizational-units-overview"></a>Organisaatioyksiköiden yleiskatsaus

Microsoft Dynamics 365 Project Operationsissa *organisaatioyksikkö* on ammattilaispalveluja tarjoavan yrityksen erillinen ryhmä tai osasto, joka työllistää laskutettavia resursseja.

Ammattilaispalveluja tarjoaville yrityksille, jotka työllistävät teknisiä resursseja eri ammattialoilla tai liiketoiminta-alueilla, roolin täyttämisen kustannukset voivat vaihdella ammattialoittain tai liiketoiminta-alueittain. Tässä skenaariossa organisaatioyksikön käsite auttaa tarjoamalla tavan ryhmitellä joukko laskutettavia rooleja sellaiseen yritysosastoon, jolla on erillinen kustannusrakenne kyseisiä rooleja varten.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Organisaatioyksiköiden käsite Project Operationsissa

Project Operationsissa organisaatioyksiköllä on tietty valuutta ja tietyt kustannushinnastot.

Organisaatioyksikön valuutta on ensisijainen kustannusten seurannassa käytettävä valuutta.

Kuhunkin organisaatioyksikköön voidaan liittää yksi tai useampi kustannushinnasto. Project Operationsissa organisaatioyksikköön liitettäviä hinnastoja rajoitetaan seuraavasti:

- Hinnastojen on oltava organisaatioyksikön valuuttana.
- Hinnastojen on oltava kustannushinnastoja.

Lisäksi resurssientiteetissä on organisaatioyksikön määrite. Kukin resurssi voidaan kohdentaa yhdelle organisaatioyksikölle.

### <a name="roles-of-organizational-units"></a>Organisaatioyksiköiden roolit

Organisaatioyksiköllä on Project Operationsissa kaksi roolia:

- **Sopimusyksikkö** – organisaatioyksikkö, joka edustaa sitä yrityksen ryhmää tai osastoa, joka on pääasiallisesti vastuussa myynnin parantamisesta ja työn ja palvelujen asiakkaalle toimittamisen hallinnasta. Sopimusyksikkö määritetään sivujen **Mahdollisuus**, **Tarjous**, **Projektisopimus** ja **Projekti** otsikko-osion kentässä **Sopimusyksikkö**.
- **Resursointiyksikkö** – organisaatioyksikkö, johon resurssi kuuluu tai jolle se on kohdennettu. Organisaatioyksikkö voi antaa resurssejaan joihinkin rooleihin työnkuvauksissa ja projekteissa, jotka sopimusyksikkö omistaa.

![Sopimus- ja resursointiyksiköt.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Organisaatioyksikkö – UKK

Seuraavassa on vastauksia joihinkin useimmin kysyttyihin kysymyksiin organisaatioyksiköistä.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Miten Project Operationsin organisaatioyksikköentiteetti liittyy organisaatioentiteettiin, joka on jo olemassa Dynamics 365:ssä?

Dynamics 365:n organisaatioyksikkö edustaa yleisen Dynamics 365 -esiintymän nimeä. Nimi on yleensä yleisen yrityksen nimi.

Organisaatioyksikköentiteetti edustaa tyhmää tai osastoa yleisessä yrityksessä. Tällä ryhmällä tai osastolla on joukko rooleja ja kustannushinnasto kyseisille rooleille. Nämä roolit ja hinnasto eroavat muiden yrityksen ryhmien tai osastojen rooleista ja hinnastoista.

Kun Project Operations on asennettu, organisaation oletusorganisaatioyksikkö luodaan organisaation perusteella. Kaikki olemassa olevat resurssit kohdennetaan oletusorganisaatioyksikölle. Jos Dynamics 365:een tuodaan uusia Active Directoryn käyttäjiä, käyttäjien tuontiprosessi kohdentaa ne oletusorganisaatioyksikölle Project Operationsissa.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Miten organisaatioyksikköentiteetti eroaa liiketoimintayksikköentiteetistä?

Dynamics 365:ssä liiketoimintayksikkö on suojausrakenne. Käyttäjän kohdennus liiketoimintayksikköön määrittää entiteetit ja entiteettitietueet, joihin käyttäjällä on käyttöoikeus. Se määrittää myös oikeudet (luo, lue, kirjoita, poista, liitä, liitä kohteeseen, kohdenna tai jaa), jotka käyttäjällä on kyseisten entiteettitietueiden osalta.

Organisaatioyksikköentiteetti edustaa yrityksen ryhmää tai osastoa, jolla on omat kustannushinnat sille kohdennetuille työntekijöille. Resurssin kohdennus organisaatioyksikköön määrittää resurssin kustannukset projektisitoumuksille.

Kun otat Dynamics 365:n käyttöön, optimoi liiketoimintayksikköjen hierarkian suojausvaltuudet ja käyttäjien kohdennus liiketoimintayksiköille. Kohdenna kaikki ne käyttäjät samaan liiketoimintayksikköön, joiden on yleensä käytettävä samaa tietuejoukkoa. Organisaatioyksikkö ei vaikuta suojausvaltuuksiin tai käyttöoikeuksiin.

**Esimerkki, joka näyttää yhden mahdollisen eron organisaatioyksiköiden ja liiketoimintayksiköiden mallinnuksessa**

Yrityksellä Contoso, Ltd. on menestyksekäs Microsoft-teknologiakäytäntö. Jali ja Irma ovat molemmat C\#-kehittäjiä, mutta Irma on Yhdysvalloissa ja Jali on Intiassa. Useimmat projektisitoumukset tarvitsevat resursseja sekä Contoso Indialta että Contoso US:lta, ja Jali ja Irma tarvitsevat saman suojausvaltuuksien tason projekteissa tällä ammattialalla. Contoso Indian kehittäjäkustannukset kuitenkin poikkeavat merkittävästä Contoso US:n kehittäjäkustannuksista.

Tässä on optimaalinen tapa suunnitella tämä skenaario Dynamics 365:n ja Project Operationsin avulla.

1. Luo Microsoft-teknologiakäytäntö liiketoimintayksikkönä ja kohdenna Jali ja Irma sille. Tämä auttaa varmistamaan, että molemmilla työntekijöillä on samaa suojausvaltuuksien taso kaikissa kyseisen ammattialan projekteissa. Molemmat voivat seurata etenemistä ja raportoida aikaa, kuluja, materiaalin käyttöä ja tehtäväpäivityksiä.
2. Luo kaksi organisaatioyksikköä auttamaan sen varmistamisessa, että projektin kustannukset näkyvät oikein.
3. Kohdenna Irma Contoso US:lle ja kohdenna Jali Contoso Indialle.
4. Kohdenna sopivat kustannushinnastot molemmille organisaatioyksiköille. Tällä tavoin autat sen varmistamisessa, että Jalille ja Irmalle projektissa merkittävät kustannukset vastaavat kustannuseroa Contoso US:n ja Contoso Indian välillä.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Onko organisaatioyksikköjen ja myyntialueiden välillä yhteyttä Dynamics 365:ssä?

Myyntialueiden ja organisaatioyksiköiden välillä ei ole yhteyttä tai suhdetta. Myyntialue on yleensä maantieteellinen alue, jolla myynti tapahtuu. Kullekin myyntialueelle voidaan kohdentaa myyntihinnasto.

Organisaatioyksikkö on yrityksen sisäinen ryhmä tai osasto, joka seuraa muille osastoille tai ulkoisille asiakkaille myymänsä roolijoukon kustannuksia.

**Esimerkki, joka näyttää yhden mahdollisen eron organisaatioyksiköiden ja myyntialueiden mallinnuksessa**

Yrityksellä Contoso, Ltd. on kaksi kehityskeskusta: Contoso US ja Contoso India. Resurssikustannukset eroavat toisistaan merkittävästi näiden kahden kehityskeskuksen välillä. Contoso myy IT-palvelujaan monilla kansainvälisillä markkinoilla, kuten Latinalaisessa Amerikassa, Pohjois-Amerikassa, Aasian ja Tyynenmeren alueella, Länsi-Euroopassa ja Lähi-idässä. Samojen projektiroolien laskutushinnat voivat vaihdella merkittävästi markkinoiden välillä. Contoso US ja Contoso India pitäisi määrittää organisaatioyksiköiksi, ja molemmilla organisaatioyksiköillä pitäisi olla oma kustannushinnastonsa. Aasian ja Tyynenmeren alue, Latinalainen Amerikka, Pohjois-Amerikka, Länsi-Eurooppa ja Lähi-Itä pitäisi määrittää myyntialueiksi, ja kullakin myyntialueella pitäisi olla oma myyntihinnastonsa.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miksi hinnastojen organisaatioyksiköille kohdentaminen on rajoitettua?

Myyntihinnoittelu on yleensä yksilöllistä niille maantieteellisille alueille tai markkinoille, joilla palveluja myydään. Yrityksen sisäisillä osastoilla ei yleensä ole omaa myyntihinnoittelua samanlaisille palveluille. Sisäisillä osastoilla on kuitenkin erilaiset myytyjen tuotteiden kustannukset (MTKUST) riippuen työntekijöidensä osaamisalueista ja toiminta-alueensa työehdoista. Koska organisaatioyksiköt ovat malliltaan yrityksen sisäisiä osastoja, niillä voi olla vain kustannushinnastoja.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Miksi myyntihinnastoja ei voi kohdentaa organisaatioyksiköille?

Project Operationsissa myyntihinnastot voidaan kohdentaa asiakkaille ja myyntialueille. Tapahtumaentiteeteissä, kuten Mahdollisuus, Tarjous, Projektisopimus ja Projekti, käytetään projektisitoumuksen laskutushintojen ja mahdollisen tuoton määrittämiseen myyntihinnastoja, jotka on liitetty asiakastiliin tai myyntialueeseen.

Kustannushinnastot kohdennetaan organisaatioyksiköille. Tapahtumaentiteeteissä, kuten Mahdollisuus, Tarjous, Projektisopimus ja Projekti, käytetään projektisitoumuksen kustannusten määrittämiseen myyntihinnastoja, jotka on liitetty sopimusyksikköön.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Ovatko organisaatioyksiköt Project Operationsissa hierarkkisia?

Ei. Project Operationsin nykyisessä versiossa organisaatioyksiköt eivät ole hierarkkisia. Siksi et voi suorittaa seuraavia tehtäviä:

- Määrittää hierarkiassa ylöspäin kulkevaa mallia kustannushintojen oletusarvon asettamiselle.
- Raportoida tuottoa tai kustannuksia, jotka on koottu organisaatioyksikköjen hierarkian eri tasoilta.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Olemme suuri kansainvälinen yritys, jolla on monitasoinen kustannuskeskuksien, divisioonien ja laskutuskonttorien monitasoinen hierarkia. Miten voimme hyödyntää organisaatioyksikköjen konseptia parhaiten Project Operationsin nykyisessä versiossa?

Kun sinulla on monimutkainen kustannuspaikkojen, osastojen, laskutuspaikkojen jne. hierarkia, määritä kyseisen hierarkian lehtisolmut erillisiksi organisaatioyksiköiksi.

Seuraavassa esimerkissä esitetään tyypillinen hierarkia.

**Contoso India**

- SAP-käytäntö

    - Tekniset konsultit
    - Toiminnalliset konsultit

- Microsoft-teknologiakäytäntö

    - Tekniset konsultit
    - Toiminnalliset konsultit

**Contoso US**

- SAP-käytäntö

    - Tekniset konsultit
    - Toiminnalliset konsultit

- Microsoft-teknologiakäytäntö

    - Tekniset konsultit
    - Toiminnalliset konsultit

Jos hierarkiasi on samankaltainen tämän esimerkin kanssa, sinun on määritettävä se litistetyksi luetteloksi seuraavasti:

- Contoso India - SAP-käytäntö - tekniset konsultit
- Contoso India - SAP-käytäntö - toiminnalliset konsultit
- Contoso India - Microsoft-teknologiakäytäntö - toiminnalliset konsultit
- Contoso India - Microsoft-teknologiakäytäntö - toiminnalliset konsultit
- Contoso US - SAP-käytäntö - tekniset konsultit
- Contoso US - SAP-käytäntö - toiminnalliset konsultit
- Contoso US - Microsoft-teknologiakäytäntö - tekniset konsultit
- Contoso US - Microsoft-teknologiakäytäntö - toiminnalliset konsultit

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Olemme pieni asiantuntijapalveluja tarjoava yritys, joka toimii vain yhtenä osastona. Miten voimme hyödyntää organisaatioyksikköjen konseptia parhaiten Project Operationsin nykyisessä versiossa?

Jos yritys toimii yhtenä yksikkönä, jolla on yksi kustannushinnasto, sille ei tarvitse määrittää organisaatioyksikköjä. Project Operationsin asennus luo yhden oletusorganisaatioyksikön, jolla on sama nimi kuin organisaatiolla. Kaikki käyttäjät kohdennetaan oletusarvoisesti tälle organisaatioyksikölle. Kun järjestelmä edellyttää organisaatioyksikön valintaa, tämä organisaatioyksikkö valitaan oletusarvoisesti.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kun projekti luodaan tarjouksen tai projektin sopimusrivin perusteella, oletusarvoinen sopimusyksikkö perustuu tarjoukseen tai projektisopimukseen. Jos projekti luodaan ennen myyntientiteettejä, kuten tarjousta tai projektisopimusta, mikä on oletusarvoisena sopimusyksikkönä?

Kun projekti luodaan itsenäisenä, projektin oletusarvoinen sopimusyksikkö perustuu projektin luoneeseen käyttäjään. Kyseinen käyttäjä on myös oletusarvoinen projektipäällikkö. Jos projekti on yhdistetty myyntientiteettiin, kuten tarjoukseen tai projektisopimukseen, projektin sopimusyksikkö perustuu kyseiseen myyntientiteettiin. Tässä tapauksessa projektiarviot lasketaan mahdollisesti uudelleen, koska kustannushinnastoa käytetään kustannusarvion muutosten laskemiseen, jos sopimusyksikkö muuttuu. Myyntihinnastoa käytetään muutettavien myyntiarvioiden laskemiseen, jotta ne vastaavat tarjouksessa olevaa projektin hinnastoa.

Projektin kenttiä **Sopimusyksikkö** ja **Valuutta** ei voi muokata, koska niiden on vastattava sen myyntientiteetin (tarjous tai projektisopimus) arvoja, joihin projekti on yhdistetty.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Organisaatioyksiköiden luominen ja ylläpito Project Operationsissa

Luo organisaatioyksikkö Project Operationsissa seuraavien vaiheiden mukaisesti.

1. Valitse **Asetukset \> Organisaatioyksiköt**.
2. Valitse **Uusi**.
3. Anna organisaatioyksikön nimi **Yleiset**-alueen **Nimi**-kenttään. Määritä sitten muut kentät tarpeen mukaan.
4. Valitse **Tallenna** ja luo tietue, jotta voit jatkaa muokkaamista.
5. **Kustannushinnastot**-kohdassa lisää hinnasto valitsemalla plusmerkki (**+**). Voit lisätä vain hinnastoja, joilla on **Kustannus**-konteksti tässä.
6. **Nimi**-kentässä valitse **Etsi**-painike ja valitse hinnasto, jonka haluat ottaa käyttöön tässä organisaatioyksikössä. Jatka lisäämällä hinnastoja tarvittaessa.
7. Kun olet lisännyt haluamasi hinnastot, valitse sivun oikeasta alakulmasta **Tallenna**-kuvake.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
