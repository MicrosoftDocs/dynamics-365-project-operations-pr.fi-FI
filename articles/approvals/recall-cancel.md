---
title: Aiemmin hyväksyttyjen tapahtumien palauttaminen
description: Tässä artikkelissa käsitellään sitä, miten projektiryhmän jäsen voi pyytää aiemmin lähetettyjen ja hyväksyttyjen aika-, kulu- ja materiaalikäyttötietueiden palautusta sekä sitä, miten projektipäällikkö voi hyväksyä tai hylätä takaisinvetopyyntöjä.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930360"
---
# <a name="recall-previously-approved-entries"></a>Aiemmin hyväksyttyjen tapahtumien palauttaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektiryhmän jäsen tai toinen henkilö, joka lähettää aika-, kulu tai materiaalikäyttömerkinnän, voi peruuttaa tämän merkinnän sen hyväksymisen jälkeen. Peruutusprosessissa on kaksi päävaihetta:

1. Lähettäjä pyytää peruuttamista.
2. Hyväksyjä hyväksyy peruutuspyynnön.

## <a name="request-a-recall"></a>Pyydä peruutusta

Seuraa näitä vaiheita pyytääksesi hyväksytyn aika-, kulu- tai materiaalikäyttömerkinnän poistamista.

1. Peruutettavan merkinnän tyypistä riippuen noudata seuraavia vaiheita:

    - Jos kyseessä on aikakirjaus, valitse **Projektit** \> **Omat työt** \> **Aikamerkintä** ja valitse kaikki tietyn projektin ja tehtävän yhdistelmän aikamerkinnät. Vaihtoehtoisesti voit valita ruudukossa yksittäiset solut tiettynä päivämääränä tiettyä projektia varten.
    - Jos kyseessä on kulutapahtuma, valitse **Projektit** \> **Omat työt** \> **Kulut** ja valitse se kulutapahtumarivi, jonka haluat peruuttaa.
    - Jos kyseessä on materiaalikäyttötapahtuma, valitse **Projektit** \> **Omat työt** \> **Materiaalinkäyttöloki** ja valitse se materiaalinkäyttötapahtuma, jonka haluat peruuttaa.

2. Valitse **Peruuta**. Vahvistusvalintaikkuna avautuu. Jos valitut aika-, kulu ja materiaalinkäyttötapahtumat on jo hyväksytty, sinua pyydetään syöttämään peruutuksen syy.
3. Syötä peruutuksen syy ja vahvista sen jälkeen toiminto valitsemalla **OK**. Järjestelmä lähettää tietueet hyväksyneelle henkilölle pyynnön hyväksyä peruutus.

> [!IMPORTANT]
> Asiakkaalta jo laskutettua hyväksyttyä aikaa, kulua tai materiaalin käyttömerkintää ei voi palauttaa pyynnöllä. Jos yrität luoda peruutuspyynnön, saat sanoman, jonka mukaan aikaa, kulua tai materiaalinkäyttöä ei voi peruuttaa, koska se on jo laskutettu. Tällöin voit pyytää merkinnän palautusta vain, jos korjauslaskua käytetään kokonaishyvitykseen tai palautukseen asiakkaalle alkuperäisen laskun mukaan.

## <a name="approve-or-reject-a-recall-request"></a>Peruutuspyynnön hyväksyminen tai hylkääminen

Voit hyväksyä tai hylätä peruutuspyynnön seuraavien vaiheiden mukaisesti.

1. Siirry kohtaan **Projektit** \> **Omat työt** \> **Hyväksynnät**.
2. Vaihda **Hyväksynnät** -luettelosivulla näkymäksi **Hyväksyttävät peruutuspyynnöt**. Näkyviin tulee luettelo lähetetyistä peruutuspyynnöistä.
3. Valitse vähintään yksi merkintä ja valitse sitten **Hyväksy** tai **Hylkää**.
4. Jos valitsit **Hyväksy**, näkyviin tulee varoitussanoma, jossa on selostettu hyväksynnän vaikutus. Vahvista toiminto valitsemalla **OK**. Peruutuspyyntö on hyväksytty.

    -tai-

    Jos valitsit **Hylkää**, peruutuspyyntö hylätään.

> [!IMPORTANT]
> Kun peruutus hyväksytään, järjestelmä tarkistaa samoin kuin pyynnön yhteydessä, onko aika-, kulu tai materiaalinkäyttömerkinnöissä laskutusaktiviteetteja. Jos tapahtuma on jo laskutettu tai jos se on luonnoslaskulla, hyväksyjä saa virhesanoman, jonka mukaan ajan tai kulun peruutusta ei voi hyväksyä, koska se on jo laskutettu. Tällöin hyväksyjä voi hyväksyä palautuksen vain, jos korjauslaskua käytetään kokonaishyvitykseen tai palautukseen asiakkaalle alkuperäisen laskun mukaan.

## <a name="impact-of-a-recall-request"></a>Peruutuspyynnön vaikutus

Kun hyväksyntä peruutetaan, siihen liittyy sekä toiminnallisia vaikutuksia että taloudellisia vaikutuksia.

### <a name="operational-impact"></a>Toiminnallinen vaikutus

Jos peruutuspyyntö hyväksytään, hyväksyntätietue merkitään **Hylätyksi**. Tapahtuman tilaksi tulee joko **Palautunut** tai **Hylätty** sen mukaan, onko kyseessä aika-, kulu- tai materiaalinkäyttötapahtuma.

Projektiryhmän jäsen voi tarkastella tapahtumia, muokata ja lähettää merkintöjä uudelleen tai poistaa tietueita kokonaan.

Jos peruutuspyyntö hylätään, merkinnän tila säilyy ennallaan **Hyväksyttynä**, eikä projektiryhmän jäsen tai projektin hyväksyjä voi muokata merkintää.

### <a name="financial-impact"></a>Taloudellinen vaikutus

Jos peruutuspyyntö hyväksytään, vastaavat toteutuneet kustannukset ja myynnit päivitetään seuraavalla tavalla:

- **Oikaisun tila** -kenttä päivittyy **Oikaistuksi**.
- **Laskutuksen tila** -kenttä päivittyy **Peruutetuksi**.

Seuraavaksi todellisten arvojen taulukossa luodaan palautusmerkintöjä. Peruutusmerkintöjen luomista varten järjestelmä kopioi kenttien arvot alkuperäisistä todellisista arvoista. Ainoat arvot, joita ei kopioida, ovat määräarvot. Sen sijaan kyseiset arvot kumotaan. Kumottuja todellisia arvoja luodaan sekä **Kustannus**- että **Laskuttamaton myynti** -muotoisille todellisille arvoille. **Oikaisun tila** -kentän arvoksi käänteisissä nykyarvoissa asetetaan **Oikaisukelvoton** ja **Laskutuksen tila** -kentän arvoksi **Peruutettu**. Näiden muutosten vuoksi projektin kirjatut menot ja tulot eivät enää vastaa summia, joita nämä nykyarvot edustavat.

Jos peruutuspyyntö hylätään, projektiin ei liity taloudellista vaikutusta.

## <a name="changes-to-time-entry-records"></a>Aikamerkintätietueiden muutokset

Seuraavassa kuvassa näkyvät muutokset, jotka tapahtuvat hyväksytyille aikakirjauksille ja vastaaville hyväksyntätietueille, kun ne peruutetaan.

![Ajan syötön tilasiirtymät.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Kulu- ja materiaalinkäyttömerkintätietueiden muutokset

Seuraavassa kuvassa näkyvät muutokset, jotka tapahtuvat hyväksytyille kulu- ja materiaalinkäyttökirjauksille ja vastaaville hyväksyntätietueille, kun ne peruutetaan.

![Kulujen syötön tilasiirtymät.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
