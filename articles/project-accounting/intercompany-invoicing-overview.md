---
title: Yritysten välisen laskutuksen yleiskatsaus
description: Tässä aiheessa on tietoja ja esimerkkejä yritysten välisistä laskuista projekteissa.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002637"
---
# <a name="intercompany-invoicing-overview"></a>Yritysten välisen laskutuksen yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Organisaatiolla voi olla useita osastoja, tytäryhtiöitä ja muita juridisia kohteita, jotka siirtävät tuotteita ja palveluja toisiinsa projekteissa. Palvelua tai tuotetta tarjoava yritys on nimeltään *lainaa antava yritys*. Palvelun tai tuotteen vastaanottava yritys on nimeltään *lainaa ottava yritys*.

Seuraavassa kuvassa on esitetty tyypillinen skenaario, jossa kaksi yritystä, Contoso Robotics USA (lainaa ottava yritys) ja Contoso Robotics UK (lainaa antava yritys) jakavat resursseja keskenään toimittaakseen projektin asiakkaalle, eli Adventure Worksille. Tässä skenaariossa Contoso Robotics USA on palkattu toimittamaan työ Adventure Worksille.

![Konsernin sisäinen laskutus](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations käyttää seuraavaa työnkulkua yritysten välisten tapahtumien käsittelyyn:

1. Resurssit lainaa antavasta yrityksestä kirjaavat yritysten väliset aika- tai kulutapahtumat merkitsemällä aikaa tai kuluja lainaa ottavan yrityksen projekteihin.
2. Ajan ja kulujen kustannukset kirjataan lainaa antavaan yritykseen käyttämällä lainaa ottavan yrityksen yksikkökustannushinnastoa.
3. Yritysten väliset laskuttamattomat myyntitapahtumat kirjataan lainaa antavaan yritykseen käyttämällä lainaa ottavan yrityksen yksikkökustannushinnastoa.
4. Laskuttamaton tuotto kirjataan lainaa ottavaan yritykseen käyttäen projektisopimuksen myyntihinnastoa. Asiakasta voidaan laskuttaa, kun laskuttamaton tuotto kirjataan. Asiakkaan ei tarvitse odottaa, kunnes yritysten välisen laskun käsittely on valmis.
5. Yritysten väliset asiakaslaskut luodaan säännöllisin väliajoin lainaa antavassa yrityksessä. Laskut luodaan manuaalisesti tai käyttämällä kausittaista automatisoitua prosessia. Kullekin lainaa ottavalle yritykselle voidaan luoda yksittäinen lasku, tai voidaan luoda erilliset, projektikohtaiset laskut.
6. Kun yritysten välinen asiakaslasku kirjataan lainaa antavassa yrityksessä, sitä vastaava, odottava toimittajan lasku luodaan lainaa ottavassa yrityksessä. Odottavan toimittajan laskun kustannukset tallennetaan projektin alikirjauksiin, kun lasku kirjataan.

Seuraavassa kaaviossa on kuvattu yritysten välinen laskutus siltä osin, kun se liittyy kirjanpitotapahtumiin ja odotettuihin yleisen tapahtumarekisterin kirjauksiin.

![Yritysten välinen työnkulku](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Yritysten välisen laskutuksen määrittäminen](configure-intercompany-invoicing.md)
- [Yritysten välisten tapahtumien tallentaminen](create-intercompany-transactions.md)
- [Yritysten välisten asiakas- ja toimittajalaskujen luominen](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]