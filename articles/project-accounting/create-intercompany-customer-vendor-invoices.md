---
title: Yritysten välisten asiakkaan ja toimittajan laskujen luominen
description: Tässä aiheessa on tietoja yritysten välisten asiakkaan ja toimittajan laskujen luomisesta.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eb9e49fee4d4a52ec53e0919c2d32c224f04df66
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010962"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Yritysten välisten asiakkaan ja toimittajan laskujen luominen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Lainaa antavan yrityksen projektin kirjanpitäjä luo yritysten välisen asiakaslaskun projektin kustannuksille, jotka siirretään lainaa ottavaan yritykseen. Kun yritysten välinen asiakaslasku on hyväksytty ja kirjattu, lainaa antava yritys lähettää yritysten välisen laskun lainaa ottavalle yritykselle.

Lainaa antavan yrityksen projektin kirjanpitäjä voi määrittää eräprosessin yritysten välisten laskujen toistuvaa luomista varten. Projektin kirjanpitäjä määrittää ehdot, kuten tietyt projektit, yritysten välisten laskujen eräluontia varten.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Yritysten välisen asiakaslaskun manuaalinen luominen projektin tapahtumille 

Toimi näin luodaksesi yritysten välisen asiakaslaskun projektin tapahtumille. Hae tunnit, jotka työntekijät kirjasivat projekteihin lainaa ottavissa yrityksissä ja kuluja, jotka tapahtuivat omassa yrityksessäsi lainaavien yritysten puolesta. Voit hakea tietoja yrityksen nimen, projektin sopimusnumeron, projektinumeron, päivämäärävälin tai minkä tahansa näiden ehtojen yhdistelmän perusteella. Valitse hakutuloksista yritysten väliseen laskuun lisättävät tapahtumat. 

Seuraavat vaiheet on suoritettava lainauksen tekevässä yrityksessä. 

1. Siirry Dynamics 365 Financessa kohtaan **Projektinhallinta ja kirjanpito** > **Proktin laskut** > **Yritysten väliset asiakaslaskut**. Valitse **Yritysten väliset asiakaslaskut** -luettelosivun toimintoruudussa **Uusi.**
2. Valitse **Luo yritysten välinen lasku** -sivun **Yritys**-kentässä lainaa ottava yritys.
3. Valinnainen: Syötä tietty projektisopimus ja projektinumero.
4. Rajaa hakua valitsemalla päivämääräväli. Syötä päivämäärät kenttiin **Alkamispäivä** ja **Päättymispäivä**. Vain kyseisellä päivämäärävälillä kirjatut yritysten väliset tapahtumat näkyvät hakutuloksissa.
5. Määritä **Projektin lisäasetuskirjauskansioriviparametrin** arvoksi **Kyllä** ja valitse **Haku**.
6. Valitse hakutuloksista yritysten väliseen laskuehdotukseen sisällytettävät tapahtumat ja valitse sitten **OK**.
7. Hakutuloksista valitsemasi yritysten väliset tapahtumat näkyvät sivulla **Yritysten välinen asiakaslasku**. Jos haluat muokata tapahtumia, ennen kuin lähetät laskun lainaa ottavalle yritykselle, toimi seuraavasti:
  
    1. Avaa **Konsernin sisäinen myyntilasku** -sivulla laskun tiedot ja valitse sitten **Lisää rivi**.
    2. Voit poistaa rivin valitsemalla sen ja valitsemalla sen jälkeen **Poista**.
    3. Tarkastele kommentteja, syitä, taloushallinnon dimensioita ja muita tietoja valitusta rivistä laskurivin tiedoissa.
    
8. Voit kirjata yritysten välisen asiakaslaskun valitsemalla toimintoruudussa **Kirjaa**.

> [!NOTE]
> Jos organisaatiosi edellyttää yritysten välisten laskujen tarkistamista ennen niiden kirjaamista, järjestelmän järjestelmänvalvoja voi määrittää yritysten välisille laskuille työnkulun. Jos yritysten välisille laskuille ei ole määritetty työnkulkua, voit kirjata yritysten välisen laskun.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Erätyön luominen yritysten välisiä laskuja varten

Voit luoda useita yritysten välisiä laskuja samalla kertaa kaikkien kaikille lainaa ottaville yrityksille. Hakutoiminnon avulla voit esimerkiksi hakea kaikkia lainaa ottaneiden työntekijöiden kirjaamia tapahtumia, jotka liittyvät projekteihin, joita hallinnoivat toiset yritykset. Voit tämän jälkeen luoda yritysten välisen laskun jokaiselle lainaa ottavalle yritykselle hakutulosten antamia tapahtumia varten.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Projektin laskut** > **Luo yritysten välisiä asiakaslaskuja**.
2. Valitse **Luo yritysten välisiä laskuja** -sivun **Yritys**-kentässä laskutettava yritys. Jos et valitse yritystä, kaikki hakuehtoja vastaavat tapahtumat näytetään kaikille lainaa ottaville yrityksille.
3. Valitse kohdassa **Luo yksi lasku per**, tulisiko yritysten välinen lasku luoda projektin perusteella vai lainaa ottavan yrityksen perusteella.
4. Valinnainen: Jos haluat valita tietyn projektin ja projektisopimuksen yritysten välisten laskujen luomista varten, napauta **Valitse**. Valitse **Tiedustelu**-sivun **Ehdot**-kentässä projektisopimus, projektinumero tai molemmat ja valitse sitten **OK**.
5. Määritä **Erä**-sivulla eräprosetti luomaan yritysten välisiä laskuja toistuvasti. Lisätietoja on aiheessa [Eräkäsittelytyön lähettäminen lomakkeesta](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Voit kirjata yritysten välisiä laskuja valitsemalla toimintoruudussa **Kirjaa**.

> [!NOTE]
> Jos organisaatiosi edellyttää yritysten välisten laskujen tarkistamista ennen niiden kirjaamista, järjestelmän järjestelmänvalvoja voi määrittää yritysten välisille laskuille työnkulun. Jos yritysten välisille laskuille ei ole määritetty työnkulkua, voit kirjata yritysten välisiä laskuja.

## <a name="post-the-intercompany-vendor-invoice"></a>Kirjaa yritysten välinen toimittajalasku

Lainaa ottavan yrityksen projektin kirjanpitäjä voi tarkistaa odottavia yritysten välisiä laskuja, kun vastaava yritysten välinen asiakaslasku on kirjattu. Siirry Rahoituksessa lainaa ottavassa yrityksessä kohtaan **Ostoreskontra** > **Laskut** > **Odottavat toimittajan laskut**. Odottava laskun numero vastaa yritysten välisen asiakaslaskun numeroa. Tarkista, että lasku on oikein, ja kirjaa sitten lasku. Yritysten välisen toimittajan laskun kirjaaminen luo projektin alikirjanpidon ja pääkirjanpidon tapahtuman, joka vastaa tapahtuman kustannuksia lainaa ottavassa yrityksessä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
