---
title: Yritysten välisen laskutuksen yleiskatsaus
description: Tässä aiheessa on tietoja ja esimerkkejä yritysten välisistä laskuista projekteissa.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595459"
---
# <a name="intercompany-invoicing-overview"></a>Yritysten välisen laskutuksen yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Organisaatiolla voi olla useita osastoja, tytäryhtiöitä ja muita juridisia kohteita, jotka siirtävät tuotteita ja palveluja toisiinsa projekteissa. Palvelua tai tuotetta tarjoava yritys on nimeltään *lainaa antava yritys*. Palvelun tai tuotteen vastaanottava yritys on nimeltään *lainaa ottava yritys*.

Seuraavassa kuvassa on tyypillinen skenaario, jossa kaksi yritystä, Contoso Robotics USA (lainaa ottava yritys) ja Contoso Robotics UK (lainaa antava yritys) jakavat resursseja toimittaakseen projektin asiakkaalle nimeltä Adventure works. Tässä skenaariossa contoso Robotics USA on tehnyt sopimuksen työn toimittamisesta Adventure Worksille.

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