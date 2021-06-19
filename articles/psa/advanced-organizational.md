---
title: Organisaatioyksiköt
description: Tässä aiheessa on tietoja Dynamics 365 Project Service Automationin organisaatioyksiköistä.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 3be18adfa1d346bdabae7e89375ca2c5a2dbda95
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009612"
---
# <a name="organizational-units"></a>Organisaatioyksiköt 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automationissa organisaatioyksikkö on ammattilaispalveluja tarjoavan yrityksen erillinen ryhmä tai osasto, joka työllistää laskutettavia resursseja.

Ammattilaispalveluja tarjoaville yrityksille, jotka työllistävät teknisiä resursseja eri ammattialoilla tai liiketoiminta-alueilla, roolin täyttämisen kustannukset voivat vaihdella ammattialoittain tai liiketoiminta-alueittain. Organisaatioyksikön käsite auttaa tässä tilanteessa tarjoamalla tavan ryhmitellä joukko laskutettavia rooleja sellaiseen yritysosastoon, jolla on erillinen kustannusrakenne kyseisiä rooleja varten.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Organisaatioyksiköiden keskeiset määritteet ja yhteydet

PSA:ssa organisaatioyksiköllä on tietty valuutta ja tietyt kustannushinnastot.

Organisaatioyksikön valuutta on ensisijainen kustannusten seurannassa käytettävä valuutta.

Kuhunkin organisaatioyksikköön voidaan liittää yksi tai useampi kustannushinnasto. PSA:ssa organisaatioyksikköön liitettäviä hinnastoja rajoitetaan seuraavasti:

- Hinnastojen on oltava organisaatioyksikön valuutassa
- Hinnastojen on oltava peräisin kustannushinnastoista

Lisäksi resurssientiteetissä on organisaatioyksikön määrite. Kukin resurssi voidaan kohdentaa yhdelle organisaatioyksikölle.

## <a name="roles-of-organizational-units"></a>Organisaatioyksiköiden roolit

Organisaatioyksiköllä on PSA:ssa kaksi roolia:

- **Sopimusyksikkö** – organisaatioyksikkö, joka edustaa sitä yrityksen ryhmää tai osastoa, joka on pääasiallisesti vastuussa myynnin parantamisesta ja työn ja palvelujen asiakkaalle toimittamisen hallinnasta. Sopimusyksikkö määritetään sivujen **Mahdollisuus**, **Tarjous**, **Projektisopimus** ja **Projekti** otsikko-osion kentässä **Sopimusyksikkö**.
- **Resursointiyksikkö** – organisaatioyksikkö, johon resurssi kuuluu tai jolle se on kohdennettu. Organisaatioyksikkö voi antaa resurssejaan joihinkin rooleihin työnkuvauksissa ja projekteissa, jotka sopimusyksikkö omistaa.

> ![Sopimus- ja resursointiyksiköt](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Organisaatioyksikön usein kysytyt kysymykset

Seuraavassa on vastauksia joihinkin useimmin kysyttyihin kysymyksiin organisaatioyksiköistä.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Miten PSA:n organisaatioyksikköentiteetti liittyy organisaatioentiteettiin, joka on jo olemassa Dynamics 365:ssä?

Microsoft Dynamics 365:n organisaatioyksikkö edustaa yleisen Dynamics 365 -esiintymän nimeä. Nimi on yleensä yleisen yrityksen nimi.

Organisaatioyksikköentiteetti edustaa tyhmää tai osastoa yleisessä yrityksessä. Tällä ryhmällä tai osastolla on joukko rooleja ja kustannushinnasto kyseisille rooleille. Nämä roolit ja hinnasto eroavat muiden yrityksen ryhmien tai osastojen rooleista ja hinnastoista.

Kun PSA on asennettu, organisaation oletusorganisaatioyksikkö luodaan organisaation perusteella. Kaikki olemassa olevat resurssit kohdennetaan oletusorganisaatioyksikölle. Jos Dynamics 365:een tuodaan uusia Active Directoryn käyttäjiä, käyttäjien tuontiprosessi kohdentaa ne oletusorganisaatioyksikölle PSA:ssa.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Miten organisaatioyksikköentiteetti eroaa liiketoimintayksikköentiteetistä?

Dynamics 365:ssä liiketoimintayksikkö on suojausrakenne. Käyttäjän kohdennus liiketoimintayksikköön määrittää entiteetit ja entiteettitietueet, joihin käyttäjällä on käyttöoikeus. Se määrittää myös oikeudet (luo, lue, kirjoita, poista, liitä, liitä kohteeseen, kohdenna tai jaa), jotka käyttäjällä on kyseisten entiteettitietueiden osalta.

Organisaatioyksikköentiteetti edustaa yrityksen ryhmää tai osastoa, jolla on omat kustannushinnat sille kohdennetuille työntekijöille. Resurssin kohdennus organisaatioyksikköön määrittää resurssin kustannukset projektisitoumuksille.

Kun otat Dynamics 365:n käyttöön, optimoi liiketoimintayksikköjen hierarkian suojausvaltuudet ja käyttäjien kohdennus liiketoimintayksiköille. Kohdenna kaikki ne käyttäjät samaan liiketoimintayksikköön, joiden on yleensä käytettävä samaa tietuejoukkoa. Organisaatioyksikkö ei vaikuta suojausvaltuuksiin tai käyttöoikeuksiin.

#### <a name="example-of-organizational-units-and-business-units"></a>Esimerkki organisaatioyksiköistä ja liiketoimintayksiköistä

Yrityksellä Contoso, Ltd. on menestyksekäs Microsoft-teknologiakäytäntö. Jali ja Irma ovat molemmat C\#-kehittäjiä, mutta Irma on Yhdysvalloissa ja Jali on Intiassa. Useimmat projektisitoumukset tarvitsevat resursseja Contoso Indialta ja Contoso US:lta, ja Jali ja Irma tarvitsevat saman suojausvaltuuksien tason projekteissa tällä ammattialalla. Contoso Indian kehittäjäkustannukset kuitenkin poikkeavat merkittävästä Contoso US:n kehittäjäkustannuksista.

Tässä on optimaalinen tapa suunnitella tämä skenaario Dynamics 365:n ja PSA:n avulla.

1. Luo Microsoft-teknologiakäytäntö liiketoimintayksikkönä ja kohdenna Jali ja Irma sille. Tämä auttaa takaamaan, että molemmilla työntekijöillä on samaa suojausvaltuuksien taso kaikissa kyseisen ammattialan projekteissa. Molemmat voivat seurata etenemistä ja raportoida aikaa, kustannuksia ja tehtäväpäivityksiä. 
2. Luo kaksi organisaatioyksikköä auttamaan sen takaamisessa, että projektin kustannukset näkyvät oikein. 
3. Kohdenna Irma Contoso US:lle ja kohdenna Jali Contoso Indialle.
4. Kohdenna sopivat kustannushinnastot molemmille organisaatioyksiköille. Tällä tavoin autat sen takaamisessa, että Jalille ja Irmalle projektissa merkittävät kustannukset vastaavat kustannuseroa Contoso US:n ja Contoso Indian välillä.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Onko organisaatioyksikköjen ja myyntialueiden välillä yhteyttä Dynamics 365:ssä?

Myyntialueiden ja organisaatioyksiköiden välillä ei ole yhteyttä tai suhdetta. Myyntialue on yleensä maantieteellinen alue, jolla myynti tapahtuu. Kullekin myyntialueelle voidaan kohdentaa myyntihinnasto.

Organisaatioyksikkö on yrityksen sisäinen ryhmä tai osasto, joka seuraa muille osastoille tai ulkoisille asiakkaille myymänsä roolijoukon kustannuksia.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Esimerkki organisaatioyksiköistä ja myyntialueista

Yrityksellä Contoso, Ltd. on kaksi kehityskeskusta: Contoso US ja Contoso India. Resurssikustannukset eroavat toisistaan merkittävästi näiden kahden kehityskeskuksen välillä.

Contoso myy IT-palvelujaan monilla kansainvälisillä markkinoilla, kuten Latinalaisessa Amerikassa, Pohjois-Amerikassa, Aasian ja Tyynenmeren alueella, Länsi-Euroopassa ja Lähi-idässä. Samojen projektiroolien laskutushinnat voivat vaihdella merkittävästi markkinoiden välillä.

Contoso US ja Contoso India pitäisi määrittää organisaatioyksiköiksi, ja molemmilla organisaatioyksiköillä pitäisi olla oma kustannushinnastonsa. Aasian ja Tyynenmeren alue, Latinalainen Amerikka, Pohjois-Amerikka, Länsi-Eurooppa ja Lähi-Itä pitäisi määrittää myyntialueiksi, ja kullakin myyntialueella pitäisi olla oma myyntihinnastonsa.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miksi hinnastojen organisaatioyksiköille kohdentaminen on rajoitettua? 

Myyntihinnoittelu on yleensä yksilöllistä niille maantieteellisille alueille tai markkinoille, joilla palveluja myydään. Yrityksen sisäisillä osastoilla ei yleensä ole omaa myyntihinnoittelua samanlaisille palveluille. Sisäisillä osastoilla on kuitenkin erilaiset myytyjen tuotteiden kustannukset (MTKUST) riippuen työntekijöidensä osaamisalueista ja toiminta-alueensa työehdoista. Koska organisaatioyksiköt ovat malliltaan yrityksen sisäisiä osastoja, niillä voi olla vain kustannushinnastoja.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Miksi myyntihinnastoja ei voi kohdentaa organisaatioyksiköille?

PSA:ssa myyntihinnastot voidaan kohdentaa asiakkaille ja myyntialueille. Tapahtumaentiteeteissä, kuten Mahdollisuus, Tarjous, Projektisopimus ja Projekti, käytetään projektisitoumuksen laskutushintojen ja mahdollisen tuoton määrittämiseen myyntihinnastoja, jotka on liitetty asiakastiliin tai myyntialueeseen.

Kustannushinnastot kohdennetaan organisaatioyksiköille. Tapahtumaentiteeteissä, kuten Mahdollisuus, Tarjous, Projektisopimus ja Projekti, käytetään projektisitoumuksen kustannusten määrittämiseen myyntihinnastoja, jotka on liitetty sopimusyksikköön.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Ovatko organisaatioyksiköt PSA:ssa hierarkkisia?

Ei. PSA:n nykyisessä versiossa organisaatioyksiköt eivät ole hierarkkisia. Tämä tarkoittaa, että et voi:

- Määrittää hierarkiassa ylöspäin kulkevaa mallia kustannushintojen oletusarvon asettamiselle. 
- Raportoida tuottoa tai kustannuksia, jotka on koottu organisaatioyksikköjen hierarkian eri tasoilta.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Olemme suuri monikansallinen yritys, jolla on monimutkainen ja monitasoinen kustannuspaikkojen, osastojen ja laskutuspaikkojen hierarkia. Miten voimme hyödyntää organisaatioyksikköjen konseptia parhaiten tässä Project Service -sovelluksen versiossa?

Kun sinulla on monimutkainen kustannuspaikkojen, osastojen, laskutuspaikkojen jne. hierarkia, määritä kyseisen hierarkian lehtisolmut erillisiksi organisaatioyksiköiksi.
Seuraavassa esimerkissä esitetään tyypillinen hierarkia:

**ContosoIntia**

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
 
Jos hierarkiasi on samankaltainen, sinun on määritettävä se litistetyksi luetteloksi seuraavasti:
- Contoso India - SAP-käytäntö - tekniset konsultit 
- Contoso India - SAP-käytäntö - toiminnalliset konsultit       
- Contoso India - Microsoft-teknologiakäytäntö - toiminnalliset konsultit 
- Contoso India - Microsoft-teknologiakäytäntö - toiminnalliset konsultit 
- Contoso US - SAP-käytäntö - tekniset konsultit  
- Contoso US - SAP-käytäntö - toiminnalliset konsultit  
- Contoso US - Microsoft-teknologiakäytäntö - tekniset konsultit 
- Contoso US - Microsoft-teknologiakäytäntö - toiminnalliset konsultit

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Olemme pieni asiantuntijapalveluja tarjoava yritys, joka toimii vain yhtenä osastona. Miten voimme hyödyntää organisaatioyksikköjen konseptia parhaiten tässä PSA:n versiossa?

Jos yritys toimii yhtenä yksikkönä, jolla on yksi kustannushinnasto, sille ei tarvitse määrittää organisaatioyksikköjä. Dynamics 365 luo PSA:n asentamisen aikana yhden oletusorganisaatioyksikön, jolla on sama nimi kuin yrityksellä. Kaikki käyttäjät kohdennetaan oletusarvoisesti tälle organisaatioyksikölle. Kun järjestelmä edellyttää organisaatioyksikön valintaa, tämä organisaatioyksikkö valitaan oletusarvoisesti.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Kun projekti luodaan tarjouksen tai projektin sopimusrivin perusteella, oletusarvoinen sopimusyksikkö perustuu tarjoukseen tai projektisopimukseen. Jos projekti luodaan ennen myyntientiteettejä, kuten tarjousta tai projektisopimusta, mikä on oletusarvoisena sopimusyksikkönä?

Kun projekti luodaan itsenäisenä, projektin oletusarvoinen sopimusyksikkö perustuu projektin luoneeseen käyttäjään. Kyseinen käyttäjä on myös oletusarvoinen projektipäällikkö. Jos projekti on yhdistetty myyntientiteettiin, kuten tarjoukseen tai projektisopimukseen, projektin sopimusyksikkö perustuu kyseiseen myyntientiteettiin. Tässä tapauksessa projektiarviot lasketaan mahdollisesti uudelleen, koska kustannushinnastoa käytetään kustannusarvion muutosten laskemiseen, jos sopimusyksikkö muuttuu. Myyntihinnastoa käytetään muutettavien myyntiarvioiden laskemiseen, jotta ne vastaavat tarjouksessa olevaa projektin hinnastoa.

Projektin kenttiä **Sopimusyksikkö** ja **Valuutta** ei voi muokata, koska niiden on vastattava sen myyntientiteetin (tarjous tai projektisopimus) arvoja, joihin projekti on yhdistetty.


[!INCLUDE[footer-include](../includes/footer-banner.md)]