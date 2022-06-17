---
title: Yritysten välisen laskutuksen yleiskatsaus
description: Tässä artikkelissa on tietoja ja esimerkkejä projektien laskutuksesta konsernin sisällä.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913570"
---
# <a name="intercompany-invoicing-overview"></a>Yritysten välisen laskutuksen yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Organisaatiolla voi olla useita osastoja, tytäryhtiöitä ja muita juridisia kohteita, jotka siirtävät tuotteita ja palveluja toisiinsa projekteissa. Palvelua tai tuotetta tarjoava yritys on nimeltään *lainaa antava yritys*. Palvelun tai tuotteen vastaanottava yritys on nimeltään *lainaa ottava yritys*.

Seuraavassa kuvassa on tyypillinen skenaario, jossa kaksi yritystä, Contoso Robotics USA (lainaa ottava yritys) ja Contoso Robotics UK (lainaa antava yritys) jakavat resursseja toimittaakseen projektin asiakkaalle nimeltä Adventure works. Tässä skenaariossa contoso Robotics USA on tehnyt sopimuksen työn toimittamisesta Adventure Worksille.

![Yritysten välinen laskutus.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations käyttää seuraavaa työnkulkua yritysten välisten tapahtumien käsittelyyn:

1. Resurssit lainaa antavasta yrityksestä kirjaavat yritysten väliset aika- tai kulutapahtumat merkitsemällä aikaa tai kuluja lainaa ottavan yrityksen projekteihin.
2. Ajan ja kulujen kustannukset kirjataan lainaa antavaan yritykseen käyttämällä lainaa ottavan yrityksen yksikkökustannushinnastoa.
3. Yritysten väliset laskuttamattomat myyntitapahtumat kirjataan lainaa antavaan yritykseen käyttämällä lainaa ottavan yrityksen yksikkökustannushinnastoa.
4. Laskuttamaton tuotto kirjataan lainaa ottavaan yritykseen käyttäen projektisopimuksen myyntihinnastoa. Asiakasta voidaan laskuttaa, kun laskuttamaton tuotto kirjataan. Asiakkaan ei tarvitse odottaa, kunnes yritysten välisen laskun käsittely on valmis.
5. Yritysten väliset asiakaslaskut luodaan säännöllisin väliajoin lainaa antavassa yrityksessä. Laskut luodaan manuaalisesti tai käyttämällä kausittaista automatisoitua prosessia. Kullekin lainaa ottavalle yritykselle voidaan luoda yksittäinen lasku, tai voidaan luoda erilliset, projektikohtaiset laskut.
6. Kun yritysten välinen asiakaslasku kirjataan lainaa antavassa yrityksessä, sitä vastaava, odottava toimittajan lasku luodaan lainaa ottavassa yrityksessä. Odottavan toimittajan laskun kustannukset tallennetaan projektin alikirjauksiin, kun lasku kirjataan.

Seuraavassa kaaviossa on kuvattu yritysten välinen laskutus siltä osin, kun se liittyy kirjanpitotapahtumiin ja odotettuihin yleisen tapahtumarekisterin kirjauksiin.

![Yritysten välinen työnkulku.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Konsernin sisäisen laskutuksen määrittäminen](configure-intercompany-invoicing.md)
- [Yritysten välisten tapahtumien tallentaminen](create-intercompany-transactions.md)
- [Yritysten välisten asiakas- ja toimittajalaskujen luominen](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]