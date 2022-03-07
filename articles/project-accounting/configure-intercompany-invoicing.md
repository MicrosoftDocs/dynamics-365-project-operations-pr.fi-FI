---
title: Yritysten välisen laskutuksen määrittäminen
description: Tässä aiheessa on tietoja ja esimerkkejä yritysten välisten laskujen määrittämisestä projekteille.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2dec6669a41161a23f74ea962df6d8708b905315
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287549"
---
# <a name="configure-intercompany-invoicing"></a>Yritysten välisen laskutuksen määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Suorita seuraavat vaiheet, kun haluat määrittää yritysten välisen projektien laskutuksen Dynamics 365 Project Operationsissa. Yritysten väliset tapahtuman ovat projektisopimuksen aika- ja kulutapahtumia, jotka kuuluvat yhteen yritykseen tai organisaatioyksikköön, kun projektisopimuksen resurssit ovat osa toista yritystä tai organisaatioyksikköä.

## <a name="example-configure-intercompany-invoicing"></a>Esimerkki: Yritysten välisen laskutuksen määrittäminen

Seuraavassa esimerkissä Contoso Robotics USA (USPM) on lainaa ottava yritys, ja Contoso Robotics UK (GBPM) on lainaa antava yritys. 

1. **Määritä yritysten välinen kirjanpito yritysten välillä**. Kukin lainaa ottava ja antava yritys on määritettävä Pääkirjanpidon [Yritysten välinen kirjanpito](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup)-sivulla.
    
    1. Siirry Dynamics 365 Financessa kohtaan **Pääkirjanpito** > **Kirjausasetukset** > **Yritysten välinen kirjanpito**. Luo tietue, jossa on seuraavat tiedot:

        - **Alkuperäyritys** = **GBPM**
        - **KOhdeyritys** = **USPM**

2. **Määritä yritysten välinen kauppasuhde**. Lainaa ottavaa yritystä kuvaava asiakastietue on luotava lainaa antavaan yritykseen. Lainaa antavaa yritystä kuvaava asiakastietue on luotava lainaa ottavaan yritykseen.

     1. Valitse Rahoituksessa yritys **GBPM**.
     2. Valitse **Myyntireskontra** > **Asiakas** > **Kaikki asiakkaat**. Luo yritykselle uusi tietue, **USPM**.
     3. Laajenna **Nimi**, suodata tietueet **Tyypin** mukaan ja valitse **Yritykset**. 
     4. Etsi ja valitse asiakastietue yritykselle **Contoso Robotics USA (USPM)**.
     5. Valitse **Käytä vastaavuutta**. 
     6. Valitse asiakasryhmä ja tallenna sitten tietue.
     7. Valitse yritys **USPM**.
     8. Siirry kohtaan **Ostoreskontra** > **Toimittajat** > **Kaikki toimittajat**. Luo yritykselle uusi tietue, **GBPM**.
     9. Laajenna **Nimi**, suodata tietueet **Tyypin** mukaan ja valitse **Yritykset**. 
     10. Etsi ja valitse asiakastietue yritykselle **Contoso Robotics UK (USPM)**.
     11. Valitse **Käytä vastaavuutta**, valitse toimittajaryhmä ja tallenna sitten tietue.
     12. Valitse toimittajatietueessa **Yleiset** > **Määritä** > **Yritysten välinen**.
     13. Määritä **Kauppasuhde**-välilehdessä **Aktiivisen** arvoksi **Kyllä**.
     14. Valitse toimittajayritys **GBPM** ja valitse kohdassa **Oma tilitietue** asiakastietue, jonka loit aiemmin.

3. **Määritä yritysten väliset asetukset kohdassa Projektinhallinta- ja kirjanpitoparametrit**. 

    1. Valitse yritys **USPM** ja siirry kohtaan **Projektinhallinta ja kirjanpito** > **Asetukset** > **Projektinhallinta- ja kirjanpitoparametrit**.
    2. Valitse **Yritysten välinen** -välilehdessä toimittajan automaattisesti luotavia laskuja vastaava hankintaluokka.
    3. Valitse kohdassa **Oletusluokka** **Yritysten väliset resurssit**.
    4. Valitse yritys **GBPM** ja siirry kohtaan **Projektinhallinta ja kirjanpito** > **Asetukset** > **Projektinhallinta- ja kirjanpitoparametrit**.
    5. Valitse **Yritysten välinen** -välilehdellä projektin oletusluokka kullekin tapahtumatyypille. Projektiluokkia käytetään veromäärityksessä, kun konserniyritysten välisissä tapahtumissa laskutettu luokka on vain lainaavassa yrityksessä. Voit määrittää, että konserniyritysten väliset tapahtumat jaksotetaan. Kertymä tapahtuu, kun tapahtumat kirjataan Project Operationsin integraatiokirjauskansion kautta lainaa antavassa yrityksessä. Kirjauskansio peruutetaan, kun yritysten välinen lasku kirjataan.
    6. Valitse **Kun resursseja lainataan** -ryhmässä **...** > **Uusi**. 
    7. Valitse ruudukossa seuraavat tiedot:

          - **Lainaa ottava yritys** = **GBPM**
          - **Kerrytä tuottoa** = **Kyllä**
          - **Työaikaraportin oletusluokka** = **Oletus – Tunti**
          - **Kulujen oletusluokka** = **Oletus – kulu**

4. **Määritä yritysten väliset kulu- ja tuottotilit Kirjanpidon kirjauksen asetuksissa**. Yritysten väliselle tuottotilille suoritetaan pano, kun yritysten välinen asiakaslasku kirjataan lainaa antavassa yrityksessä. Yritysten väliseltä kustannustililtä suoritetaan nosto, kun vastaava odottava toimittajan lasku kirjataan lainaa ottavassa yrityksessä. Nämä tilit määritetään vastaavissa yrityksissä. 
      
     1. Valitse Rahoituksessa lainaa ottava yritys **USPM**. 
     2. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Asetukset** > **Kirjaus** > **Kirjanpidon kirjausasetukset**. 
     3. Valitse **Kustannustilit**-välilehdellä **Kirjanpidon tilityyppi** -kohdassa **Yritysten välinen kustannus**. Luo uusi tietue, jossa on seuraavat tiedot:
      
        - **Lainaa antava yritys** = **GBPM**
        - **Päätili** = Valitse yritysten välisten kustannusten päätili
        
     4. Valitse lainaa antava yritys **GBPM**. 
     5. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Asetukset** > **Kirjaus** > **Kirjanpidon kirjausasetukset**. 
     6. Valitse **Tuottotilit**-välilehdellä **Kirjanpidon tilityyppi** -kohdassa **Yritysten välinen tuotto**. Luo uusi tietue, jossa on seuraavat tiedot:

        - **Lainaa ottava yritys** = **USPM**
        - **Päätili** = Valitse yritysten välisten tuottojen päätili 

5. **Määritä työn siirtohinnoittelu**. Yritysten välinen siirtohinnoittelu määritetään Project Operationsissa Dataversessa. Määritä [työn siirtohinnoittelu](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) ja [työn laskutushinnoittelu](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) yritysten välistä laskutusta varten. Siirtohinnoittelua ei tueta yritysten välisille kulutapahtumille. Organisaatioiden välinen yksikkömyyntihinta asetetaan aina samaksi arvoksi kuin resursoivan yksikön yksikkökustannushinta.

      Kehitysresurssin kustannukset Contoso Robotics UK:lle ovat 88 GBP tunnissa. Contoso Robotics UK laskuttaa Contoso Robotics USA:lta 120 USD:a jokaista tuntia kohden, jotka tämä resurssi työskenteli Yhdysvaltain projekteissa. Contoso Robotics USA laskuttaa asiakkaalta Adventure Works 200 USD:a Contoso Robotics UK:n kehittäjäresurssin tekemästä työstä.

      1. Siirry Project Operationsissa Dataversessa kohtaan **Myynti** > **Hinnastot**. Luo uusi kustannushinnasto, jonka nimi on **Contoso Robotics UK kustannushinnat.** 
      2. Luo kustannushinnastossa tietue, jossa on seuraavat tiedot:
         - **Rooli** = **Kehittäjä**
         - **Kustannus** = **88 GBP**
      3. Siirry kohtaan **Asetukset** > **Organisaatioyksiköt** ja liitä tämä kustannushinnasto **Contoso Robotics UK** -organisaatioyksikköön.
      4. Siirry kohtaan **Myynti** > **Hinnastot**. Luo uusi kustannushinnasto, jonka nimi on **Contoso Robotics USA kustannushinnat**. 
      5. Luo kustannushinnastossa tietue, jossa on seuraavat tiedot:
          - **Rooli** = **Kehittäjä**
          - **Resurssointiyritys** = **Contoso Robotics UK**
          - **Kustannus** = **120 USD**
      6. Siirry kohtaan **Asetukset** > **Organisaatioyksiköt** ja liitä **Contoso Robotics USA kustannushinnat** -kustannushinnasto **Contoso Robotics USA** -organisaatioyksikköön.
      7. Siirry kohtaan **Myynti** > **Hinnastot**. Luo myyntihinnasto, jonka nimi on **Adventure Works laskutushinnasto**. 
      8. Luo myyntihinnastossa tietue, jossa on seuraavat tiedot:
          - **Rooli** = **Kehittäjä**
          - **Resurssointiyritys** = **Contoso Robotics UK**
          - **Laskutushinta** = **200 USD**
      9. Siirry kohtaan **Myynti** > **Projektisopimukset** ja liitä **Adventure Works laskutushinnasto** -hinnasto Adventure Works -projektin hinnastoon projektisopimuksessa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]