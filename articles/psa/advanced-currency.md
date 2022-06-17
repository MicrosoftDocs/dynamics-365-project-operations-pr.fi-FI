---
title: Monivaluuttaskenaariot (versio 3.x)
description: Tässä artikkelissa on tietoja monivaluuttaskenaarioista.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 0c302526991f8887395c11fb6c07dd29f5e6f65d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925484"
---
# <a name="multiple-currency-scenarios"></a>Monivaluuttaskenaariot

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365:ssä on kaksi valuuttakonseptia:

- **Tapahtumavaluutta** – Valuutta, jota tapahtumassa käytetään. 
- **Perusvaluutta** – Dynamics 365 -esiintymän valuutta. Tämä valuutta määritetään, kun Dynamics 365 -esiintymä provisioidaan. Sitä ei voi muuttaa.

Esimerkiksi Contoso US on myynyt 100 T-paitaa asiakkaalle Yhdistyneessä kuningaskunnassa 15 punnan (GBP) kappalehintaan. Seuraavassa taulukossa näkyy, miten tämä tapahtuma tallennetaan Tilaustuote-entiteettiin.

| Tuote | Määrä | Yksikköhinta | Valuutta | Summa | Vaihtokurssi | Yksikköhinta (perus)| Summa (perusvaluutta)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-paita | 100      | 15             | GBP      | 1500   | 0.94          | 17.25 $               | 1,725 $       |

**Valuutta** -sarakkeessa näkyy tapahtumavaluutta eli valuutta, jota myynnissä on käytetty. **Vaihtokurssi**-sarake on tapahtumavaluutan ja perusvaluutan välinen vaihtokurssi. Perusvaluutta on Yhdysvaltojen dollari (USD). Tämä perusvaluutta määritettiin Dynamics 365 -esiintymän provisioinnin yhteydessä.
Kuten taulukossa näkyy, kaikki tapahtumat tallennetaan sekä tapahtumavaluutassa että perusvaluutassa. Dynamics 365 käyttää vaihtokurssia perusvaluuttamäärien laskemiseen.

## <a name="project-service-automation-extensions"></a>Asenna Project Service Automation -laajennukset

Dynamics 365 Project Service Automation vaikuttaa tapahtumavaluuttaan, koska liiketoimintatapahtumilla on yleensä kaksi osaa: kustannus ja myynti.

Liiketoimintatapahtumiksi katsotaan seuraavat entiteetit:

- Tarjousrivin tiedot
- Projektin sopimusrivin tiedot
- Arviorivi
- Kirjauskansion rivi
- Laskurivin tiedot
- Todellinen

Jokaisessa näistä entiteeteistä on tietue, joka edustaa kustannussummaa tai myyntisummaa. Kuten kaikissa Dynamics 365-entiteetissä, joilla on **Summa**, kussakin tietueessa on summat sekä tapahtumavaluutassa että perusvaluutassa. 

PSA laajentaa kustannuksen ja myynnin tapahtumavaluutan konseptia seuraavasti:

- Aikatapahtumien kustannustapahtumavaluutta perustuu aina sen organisaatioyksikön valuuttaan, joka omistaa projektin tai hallitsee sitä. Tätä organisaatioyksikköä kutsutaan sopimusyksiköksi.
- Aika- ja kulutapahtumien myyntitapahtumavaluutta perustuu aina projektisopimuksen valuuttaan.
- Kulujen kustannustapahtuma perustuu valuuttaan, jota käytettiin kulumerkinnän luomisen yhteydessä.

## <a name="multiple-currency-scenario"></a>Monivaluuttaskenaario

Tässä osassa annetaan esimerkki projektista, jonka Contoso UK toimittaa japanilaiselle Fabrikam-asiakkaalleen. Skenaario on seuraava:

1. GBP ja Japanin jeni (JPY) määritetään kohdassa **Asetukset** \> **Yrityksen hallinta** \> **Valuutat**. 
2. Asiakastili nimeltään **Fabrikam – Japani** määritetään ja tilin valuutaksi valitaan JPY.
3. **Contoso UK** - niminen organisaatioyksikkö määritetään, ja GBP valitaan sen valuutaksi.
4. Luodaan projektisopimus, jossa **Contoso UK** määritetään sopimusyksiköksi **Fabrikam – Japani** asiakkaaksi.
5. Projektin eri tapahtumaluokkien laskutusjärjestelyjen, kuten ajasta laskuttamisen ja kuluista laskuttamisen, perusteella luodaan projektisopimuksen rivejä.
6. Luodaan projekti, jossa **Contoso UK** määritetään sopimusyksiköksi. Tämä projekti luodaan ja yhdistetään projektin sopimusriveihin.


Tarjousrivin tietoja, projektin sopimusrivin tietoja tai aikataulun arvioriviä käyttävän arvioinnin aikana entiteetissä luodaan aina kaksi tietuetta. Yksi tietue on kustannusta ja toinen myyntiä varten.

- Kustannustietueen tapahtumavaluuttana käytetään oletusarvoisesti projektin sopimusyksikön valuuttaa. Tässä esimerkissä valuuttana on GBP.
- Myyntitietueen tapahtumavaluuttana käytetään oletusarvoisesti projektisopimuksen valuuttaa. Tässä esimerkissä valuuttana on JPY.

Kun ajalle luodaan todellisia arvoja aikamerkinnän tai kustannusrivin perusteella, tapahtuu seuraavaa:

- Kustannustietueen tapahtumavaluuttana käytetään oletusarvoisesti projektin sopimusyksikön valuuttaa.
- Myyntitietueen tapahtumavaluuttana käytetään oletusarvoisesti projektisopimuksen valuuttaa.

Kun kululle luodaan todellisia arvoja kulumerkinnän tai kustannusrivin perusteella, tapahtuu seuraavaa:

- Kulusumma voidaan tallentaa missä tahansa valuutassa. Valitse valuutta käyttämällä **Kulumerkintä**-sivun tai **Kirjauskansion rivi** -sivun valuutanvalitsinta. Kulutietueen tapahtumavaluuttana käytetään oletusarvoisesti kulumerkinnän valuuttaa. 
- Myyntitietueen tapahtumavaluuttana käytetään oletusarvoisesti projektisopimuksen valuuttaa. Tämän valuutan määrittämistä varten järjestelmä muuntaa ensin tapahtuman summan käyttäjän antamasta valuutasta perusvaluutaksi. Tämän se muuntaa summan projektisopimuksen valuutaksi. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Koontien laskeminen, kun projektin todelliset arvot tallennetaan useissa tapahtumavaluutoissa

Dynamics 365 käsittelee eri valuutoissa olevien summien koonnit automaattisesti. Esimerkki:

| Tapahtumaluokka | Tapahtumatyyppi| Date   | Resurssi | Tapahtumaluokka | Määrä | Yksikköhinta | Summa      | Vaihtokurssi | Summa perusvaluutassa |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Laskuttamaton myynti   | 14. kesä | Jali  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Time              | Laskuttamaton myynti   | 15. kesä | Jali  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Kulut           | Laskuttamaton myynti   | 16. kesä | Jali  | Hotelli                | 1 kpl     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Kulut           | Laskuttamaton myynti   | 17. kesä | Jali  | Auton vuokraus           | 1 kpl     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Projektin laskuttamattoman myynnin kokonaissumman laskemista varten voidaan luoda **Summa**-kentän koontikenttä kaikille asiaan liittyville laskuttamattomille myynnin todellisille arvoille. Koontikenttä on Dynamics 365:n rakenne, jonka avulla voidaan luoda pikakaavioita toisiinsa liittyville tietueille.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
