---
title: Hyväksyttyjä toteutuneita arvoja sisältävien toimittajien laskujen tarkistaminen
description: Tässä artikkelissa käsitellään sitä, miten Microsoft Dynamics 365 Project Operationsissa projektipäälliköt voivat tarkistaa toimittajan laskut, joissa on hyväksytty alihankkijan tehtynä työnä ja kirjattuna aikana toteutuneita arvoja sekä projektiryhmän jäsenten käyttämät kulut ja materiaalit.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204170"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Hyväksyttyjä toteutuneita arvoja sisältävien toimittajien laskujen tarkistaminen

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsin avulla projektipäälliköt voivat tarkistaa toimittajien laskurivit seuraavilla tavoilla:

- Käytä **Tarkistuksen tila** -kenttää toimittajan laskun riveillä.
- Jos toimittajan laskurivit liittyvät alihankkijariviin, linkitä toteutuneet kustannukset alihankkija-aktiviteetista kyseisille toimittajan laskuriveille. Linkki luodaan, kun kustannusten toteutuneet summat täsmäytetään toimittajan laskuriveihin.

    > [!NOTE]
    > Vaikka tarkistuksen tilaa voidaan seurata toimittajan laskuriveillä, jotka eivät liity alihankintasopimukseen, kustannusten toteutuneita arvoja ei voi linkittää näihin toimittajan laskun riveihin.

## <a name="verification-status"></a>Tarkistuksen tila

Toimittajan laskurivin **Tarkistuksen tila** -kenttä ilmaisee tarkistuksen tilan. Tuetut tilat:

1. Ei aloitettu
2. Keskeneräinen
3. Suorita loppuun

Toimittajalaskun rivejä, joiden vahvistustila on **Ei aloitettu**, voidaan muokata.

Toimittajalaskun rivejä, joiden vahvistustila on **Kesken**, ei voi enää muokata. Jos toimittajan laskurivi viittaa alihankintasopimukseen, tarkistuksen tilaksi tulee automaattisesti **Kesken** heti, kun ensimmäinen toteutunut kustannus on täsmäytetty toimittajan laskuriville.

Toimittajalaskun rivejä, joiden vahvistustila on **Valmis**, ei voi enää muokata. Kun kaikilla toimittajan laskun riveillä on tämä tarkistuksen tila, toimittajan laskun voi vahvistaa.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Täsmäytä toteutuneet kulut toimittajalaskuriveille

Toteutuneiden kustannusten täsmäytyksen avulla voidaan auttaa toimittajan laskurivin tarkistusprosessia. Voit yhdistää toteutuneet kustannukset toimittajan laskuriviin seuraavasti.

1. Avaa toimittajan laskun rivi ja valitse **Täsmäyttämättömät toteutuneet kustannukset** -välilehti. Ruudukossa on luettelo toteutuneista kustannuksista, jotka viittaavat samaan alihankkijariviin kuin toimittajan laskurivi.
2. Valitse vähintään yksi kustannusten toteutunut arvo ja valitse sitten ruudukon yläpuolella olevalta työkaluriviltä **Täsmäytä**. Järjestelmä tarkistaa, että valitut toteutuneet kustannukset voidaan täsmätä. Kun tarkistus on läpäisty, toteutuneet kustannukset linkitetään toimittajan laskuriviin.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Tarkistusehdot, joiden avulla kustannusten toteutuneet arvot linkitetään toimittajan laskuriveille

Täsmäytysprosessin aikana toteutuneen kustannuksen ja toimittajan laskun rivin välille voidaan muodostaa linkki vain, jos molemmat seuraavat ehdot täyttyvät:

- Jokaisen valitun toteutuneiden kustannusten **Oikaisun tila** -kentän on oltava tyhjä. Toisin sanoen kustannusten toteutuneita toteutuneita kuluja ei saa korvata muilla toteutuneiden kustannusten toteutuneilla arvoilla kumoamis-, peruutus-, hyväksymis- tai korjauskirjausprosessin aikana.
- Seuraavien kenttien arvot on täsmäytetty toimittajan laskurivin ja valitun toteutuneen kustannuksen välillä. Jos toimittajan laskurivillä ei ole määritetty kenttää, sitä ei oteta mukaa täsmäytettäväksi.

    - Projektisopimus
    - Projektisopimusrivi
    - Tapahtumaluokka
    - Project
    - Tehtävä
    - Resurssiluokka
    - Tapahtumaluokka
    - Tuote
    - Alihankintarivi
    - Varattavissa oleva resurssi

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Poista toteutuneen kulun täsmäytys toimittajalaskuriviltä

Toteutuneiden kustannusten täsmäytys voi auttaa myös toimittajan laskun tarkistusprosessissa ottamalla käyttöön aiemmin luotujen linkkien poistamisen. Toteutuneet kustannuksien täsmäytys voidaan poistaa vain toimittajalaskun riveiltä, joiden vahvistustila on **Kesken**. Voit poistaa toteutuneen kustannuksen täsmäytyksen toimittajan laskuriviltä seuraavasti.

1. Avaa toimittajan laskun rivi ja valitse **Täsmäytetyt toteutuneet kustannukset** -välilehti. Ruudukossa on luettelo toteutuneista kustannuksista, jotka viittaavat toimittajan laskuriviin.
2. Valitse vähintään yksi kustannusten toteutunut arvo ja valitse sitten ruudukon yläpuolella olevalta työkaluriviltä **Poista täsmäytys**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
