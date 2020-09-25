---
title: Peruuta hyväksytyt aika- tai kulukirjaukset
description: Tässä aiheessa on tietoja aiemmin hyväksytyn aika- tai kulutapahtuman peruuttamisesta.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751257"
---
# <a name="recall-approved-time-or-expense-entries"></a>Peruuta hyväksytyt aika- tai kulukirjaukset

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektiryhmän jäsen tai toinen henkilö, joka lähettää aika- tai kulumerkinnän, voi peruuttaa tämän aika- tai kulumerkinnän sen hyväksymisen jälkeen. Hyväksytyn aika- tai kulumerkinnän peruuttamisprosessissa on kaksi vaihetta:

1. Lähettäjä pyytää peruuttamista.
2. Hyväksyjä hyväksyy peruutuksen.

## <a name="request-a-recall"></a>Pyydä peruutusta

Seuraa näitä vaiheita pyytääksesi hyväksytyn aika- tai kulumerkinnän poistamista.

1. Jos kyseessä on aikamerkintä, siirry kohtaan **Projektit** \> **Oma työ** \> **Aikakirjaus**.

    -tai-

    Jos kyseessä on kulumerkintä, siirry kohtaan **Projektit** \> **Oma työ** \> **Kulut**.

2. Jos kyseessä on aikakirjaus, valitse kaikki tietyn projektin ja tehtävän yhdistelmän aikamerkinnät. Vaihtoehtoisesti voit valita ruudukossa yksittäiset solut tiettynä päivämääränä tiettyä projektia varten.

    -tai-

    Jos kyseessä on kulutapahtuma, valitse se kulutapahtumarivi, jonka haluat peruuttaa.

3. Valitse **Peruuta**. Vahvistusvalintaikkuna avautuu. Jos valitut aika- ja kulutapahtumat on jo hyväksytty, sinua pyydetään syöttämään peruutuksen syy.
4. Syötä peruutuksen syy ja vahvista sen jälkeen toiminto valitsemalla **OK**. Järjestelmä lähettää tietueet hyväksyneelle henkilölle pyynnön hyväksyä peruutus.

> [!NOTE]
> Vaikka hyväksyttyjä aika- ja kulukirjauksia voidaan peruuttaa, jos hyväksytty aika tai kulu on jo laskutettu asiakkaalta, peruutuspyyntöä ei voi tehdä. Käyttäjä, joka yrittää luoda peruutuspyynnön, saa sanoman, jonka mukaan aikaa tai kulua ei voi peruuttaa, koska se on jo laskutettu.

## <a name="approve-or-reject-a-recall-request"></a>Peruutuspyynnön hyväksyminen tai hylkääminen

Voit hyväksyä tai hylätä peruutuspyynnön seuraavien vaiheiden mukaisesti.

1. Siirry kohtaan **Projektit** \> **Omat työt** \> **Hyväksynnät**.
2. Vaihda **Hyväksynnät** -luettelosivulla näkymäksi **Hyväksyttävät peruutuspyynnöt**. Näkyviin tulee luettelo lähetetyistä peruutuspyynnöistä.
3. Valitse vähintään yksi merkintä ja valitse sitten **Hyväksy** tai **Hylkää**.
4. Jos valitsit **Hyväksy**, näkyviin tulee varoitussanoma, jossa on selostettu hyväksynnän vaikutus. Vahvista toiminto valitsemalla **OK**. Peruutuspyyntö on hyväksytty.

    -tai-

    Jos valitsit **Hylkää**, peruutuspyyntö hylätään.

> [!NOTE]
> Kuten peruutusta pyydettäessä, ku peruutus hyväksytään, järjestelmä tarkistaa, onko aika- tai kulumerkinnöissä laskutusaktiviteetteja. Jos tapahtuma on jo laskutettu tai jos se on luonnoslaskulla, hyväksyjä saa virhesanoman, jonka mukaan ajan tai kulun peruutusta ei voi hyväksyä, koska se on jo laskutettu.

## <a name="impact-of-a-recall-request"></a>Peruutuspyynnön vaikutus

Kun hyväksyntä peruutetaan, siihen liittyy sekä toiminnallisia vaikutuksia että taloudellisia vaikutuksia.

### <a name="operational-impact"></a>Toiminnallinen vaikutus

Jos peruutuspyyntö hyväksytään, hyväksyntätietue merkitään **Hylätyksi**. Tapahtuman tilaksi tulee joko **Palautunut** tai **Hylätty** sen mukaan, onko kyseessä aika- vai kulutapahtuma.

Projektiryhmän jäsen voi tarkastella tapahtumia, muokata ja lähettää merkintöjä uudelleen tai poistaa tietueita kokonaan.

Jos peruutuspyyntö hylätään, merkinnän tila säilyy ennallaan **Hyväksyttynä**, eikä projektiryhmän jäsen tai projektin hyväksyjä voi muokata merkintää.

### <a name="financial-impact"></a>Taloudellinen vaikutus

Jos peruutuspyyntö hyväksytään, vastaavat toteutuneet kustannukset ja myynnit päivitetään seuraavalla tavalla:

- **Oikaisun tila** -kenttä päivittyy **Oikaistuksi**.
- **Laskutuksen tila** -kenttä päivittyy **Peruutetuksi**.

Seuraavaksi todellisten arvojen taulukossa luodaan palautusmerkintöjä. Peruutusmerkintöjen luomista varten järjestelmä kopioi kenttien arvot alkuperäisistä todellisista arvoista. Ainoat arvot, joita ei kopioida, ovat määräarvot. Sen sijaan kyseiset arvot kumotaan. Kumottuja todellisia arvoja luodaan sekä **Kustannus**- että **Laskuttamaton myynti** -muotoisille todellisille arvoille. **Oikaisun tila** -kentän arvoksi käänteisissä nykyarvoissa asetetaan **Oikaisukelvoton** ja **Laskutuksen tila** -kentän arvoksi **Peruutettu**. Näiden muutosten vuoksi projektin kirjatut menot ja tulot eivät enää vastaa summia, joita nämä nykyarvot edustavat.

Jos peruutuspyyntö hylätään, projektiin ei liity taloudellista vaikutusta.

## <a name="changes-to-time-entry-records"></a>Aikamerkintätietueiden muutokset

Seuraavassa kuvassa näkyvät muutokset, jotka tapahtuvat hyväksytyille aikakirjauksille kun ne peruutetaan.

![Ajan syötön tilasiirtymät](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Kulumerkintätietueiden muutokset

Seuraavassa kuvassa näkyvät muutokset, jotka tapahtuvat hyväksytyille kulukirjauksille kun ne peruutetaan.

![Kulujen syötön tilasiirtymät](media/ExpenseEntryStateTransitions.png)