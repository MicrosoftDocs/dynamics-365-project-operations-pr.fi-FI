---
title: Projektilaskuehdotusten luonnoksen kirjanpidon oikaisu
description: Tässä aiheessa selostetaan, miten laskuluonnokseen liittyviä kirjanpitoon liittyviä tietoja oikaistaan.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251204"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Projektilaskuehdotusten luonnoksen kirjanpidon oikaisu

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektipäällikkö ylläpitää projektilaskujen *Toiminnallisia tietoja* proformalaskussa. Näitä tietoja ovat esimerkiksi tunteja, kuluja, materiaaleja tai välitavoitteita koskeva päätös, joka on laskutettava, hinnat sekä ennakkomaksujen ja maksuennakoiden käyttö. Kun olet vahvistanut alkuperäisen proformalaskun, voit oikaista toimintatietoja luomalla ja vahvistamalla [korjaavan proformalaskun](../proforma-invoicing/corrective-invoices.md).

Projektilaskujen *kirjanpitotietoja* ylläpidetään asiakaspuolen laskuasiakirjassa. Näitä tietoja ovat arvonlisäveron laskenta ja laskuun liittyvät taloushallinnon dimensiot. Tässä aiheessa on tietoja siitä, miten näitä kirjanpitotietoja voi muuttaa projektilaskuluonnoksen perusteella.

## <a name="adjust-sales-tax"></a>Arvonlisäveron korjaus

Laskutuksen oletusarvonlisäveroryhmiä ja nimikkeen arvonlisäveroryhmiä voi muuttaa suoraan laskuehdotusasiakirjassa. Jos haluat muuttaa näitä ryhmiä, valitse **Muokkaa** ja kirjoita sitten kullakin projektilaskun ehdotusrivillä uusi arvo **Arvonlisäveroryhmä**- tai **Nimikkeen arvonlisäveroryhmä** -kenttään.

## <a name="adjust-financial-dimensions"></a>Taloushallinnon dimensioiden oikaisu

Taloushallinnon dimensioita ei voi muokata suoraan projektilaskun ehdotusrivillä. Seuraa sen sijaan näitä vaiheita oikaistaksesi taloushallinnon dimensioita projektilaskuehdotuksessa.

1. Valitse projektilaskuehdotuksessa **Poista kaikki**, jos haluat poistaa projektilaskun ehdotusrivit.

    > [!NOTE]
    > **Poista kaikki** -painike on käytettävissä vasta, kun Järjestelmänvalvoja ottaa **Poista laskuehdotusrivit käyttöön käytettäessä Project Operations -toimintoa resurssipohjaisiin tai ei-varastoituihin skenaarioihin** -ominaisuuden **Ominaisuuksien hallinnan** työtilassa.

2. Taloushallinnon dimensioiden oikaisu:

    - **Tilitapahtumat (laskutuksen välitavoitteet):** Siirry kohtaan  **Kaikki projektit** \> **Hallitse** \> **Tilitapahtumat** ja valitse välitavoite, jota on oikaistava. Päivitä sitten arvot tarpeen mukaan **Taloushallinnon dimensiot**-välilehdessä.
    - **Aika-, kulu- ja materiaalitapahtumat:** Päivitä taloushallinnon dimensiot valitsemalla **Kirjatut projektitapahtumat** -sivulla **Oikaise kirjanpitoa**.

3. Kun olet oikaissut taloushallinnon dimension arvot, siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Jaksoittainen** \> **Project Operations -integraatio** ja valitse **Tuo muuntotaulukosta** jaksoittaisen prosessin suorittamiseksi. Prosessi luo projektin laskun ehdotusrivit uudelleen päivitetyillä taloushallinnon dimension arvoilla. Päivitettyjä arvoja käytetään sitten projektin ali- ja pääkirjanpidossa, kun projektilasku kirjataan.
