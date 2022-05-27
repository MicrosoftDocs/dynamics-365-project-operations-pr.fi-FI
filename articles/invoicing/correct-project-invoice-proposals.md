---
title: Projektilaskuehdotusten luonnoksen kirjanpidon oikaisu
description: Tässä aiheessa selostetaan, miten laskuluonnokseen liittyviä kirjanpitoon liittyviä tietoja oikaistaan.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575070"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Projektilaskuehdotusten luonnoksen kirjanpidon oikaisu

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektipäällikkö ylläpitää projektilaskujen *Toiminnallisia tietoja* proformalaskussa. Näitä tietoja ovat esimerkiksi tunteja, kuluja, materiaaleja tai välitavoitteita koskeva päätös, joka on laskutettava, hinnat sekä ennakkomaksujen ja maksuennakoiden käyttö. Kun olet vahvistanut alkuperäisen proformalaskun, voit oikaista toimintatietoja luomalla ja vahvistamalla [korjaavan proformalaskun](../proforma-invoicing/corrective-invoices.md).

Projektilaskujen *kirjanpitotietoja* ylläpidetään asiakaspuolen laskuasiakirjassa. Näitä tietoja ovat arvonlisäveron laskenta ja laskuun liittyvät taloushallinnon dimensiot. Tässä aiheessa on tietoja siitä, miten näitä kirjanpitotietoja voi muuttaa projektilaskuluonnoksen perusteella.

## <a name="adjust-sales-tax"></a>Arvonlisäveron korjaus

Laskutuksen oletusarvonlisäveroryhmiä ja nimikkeen arvonlisäveroryhmiä voi muuttaa suoraan laskuehdotusasiakirjassa. Jos haluat muuttaa näitä ryhmiä, valitse **Muokkaa** ja kirjoita sitten kullakin projektilaskun ehdotusrivillä uusi arvo **Arvonlisäveroryhmä**- tai **Nimikkeen arvonlisäveroryhmä** -kenttään.

## <a name="adjust-financial-dimensions"></a>Taloushallinnon dimensioiden oikaisu

### <a name="header-dimensions"></a>Otsikkodimensiot

Laskun taloushallinnon dimensiot johdetaan oletusarvoisesti laskuttamattomista projektitapahtumatietueista, joita ollaan laskuttamassa. Järjestelmäasetusten avulla voit kuitenkin kirjata asiakkaiden saldot projektilaskuehdotusten otsikon taloushallinnon dimensioiden avulla. Voit ottaa tämän toiminnon käyttöön valitsemalla **Projektinhallinnan ja kirjanpidon parametrit**-sivun **Taloustiedot**-välilehdessä **Salli myyntireskontran projektidimensioiden päivitykset**.

Laskun otsikoiden taloushallinnon dimensioita voi muokata ennen laskun kirjaamista. Siirry **Projektilaskuehdotus**-sivulla **Otsikko**-näkymään ja muokkaa sitten **Taloushallinnon dimensiot** -välilehden arvoja.

**Otsikko**-näkymä on käytettävissä vasta, kun järjestelmänvalvoja ottaa käyttöön **Käytä projektilaskuehdotuksen ja laskukirjauskansion lomakkeita Otsikko- ja Rivit-näkymän kanssa** -toiminnon **Ominaisuuksien hallinta** -työtilassa. Tämä ominaisuus edellyttää Finance-päivitystä 10.0.25 tai uudempaa.

### <a name="line-dimensions"></a>Rividimensiot

Taloushallinnon dimensioita ei voi muokata suoraan projektilaskun ehdotusrivillä. Seuraa sen sijaan näitä vaiheita oikaistaksesi taloushallinnon dimensioita projektilaskuehdotuksessa.

1. Valitse projektilaskuehdotuksessa **Poista kaikki**, jos haluat poistaa projektilaskun ehdotusrivit.

    **Poista kaikki** -painike on käytettävissä vasta, kun Järjestelmänvalvoja ottaa **Poista laskuehdotusrivit käyttöön käytettäessä Project Operations -toimintoa resurssipohjaisiin tai ei-varastoituihin skenaarioihin** -ominaisuuden **Ominaisuuksien hallinnan** työtilassa.

2. Taloushallinnon dimensioiden oikaisu:

    - **Tilitapahtumat (laskutuksen välitavoitteet):** Siirry kohtaan  **Kaikki projektit** \> **Hallitse** \> **Tilitapahtumat** ja valitse välitavoite, jota on oikaistava. Päivitä sitten arvot tarpeen mukaan **Taloushallinnon dimensiot**-välilehdessä.
    - **Aika-, kulu- ja materiaalitapahtumat:** Päivitä taloushallinnon dimensiot valitsemalla **Kirjatut projektitapahtumat** -sivulla **Oikaise kirjanpitoa**.

3. Kun olet oikaissut taloushallinnon dimension arvot, siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Jaksoittainen** \> **Project Operations -integraatio** ja valitse **Tuo muuntotaulukosta** jaksoittaisen prosessin suorittamiseksi. Prosessi luo projektin laskun ehdotusrivit uudelleen päivitetyillä taloushallinnon dimension arvoilla. Päivitettyjä arvoja käytetään sitten projektin ali- ja pääkirjanpidossa, kun projektilasku kirjataan.
