---
title: Proformamuotoiset projektilaskut
description: Tässä aiheessa on tietoja proformamuotoisista projektilaskuista Project Operationsissa.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f2ce672a412f7ad73b072854590cd423a3499fc1
ms.sourcegitcommit: 650a84add65588defdd2ac2c4524806baab070e0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2022
ms.locfileid: "8628850"
---
# <a name="proforma-project-invoices"></a>Proformamuotoiset projektilaskut

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Proformamuotoinen projektilaskutus tarjoaa projektipäälliköille toisen hyväksyntätason ennen laskujen luomista asiakkaille. Ensimmäinen hyväksyntätaso on valmis, kun projektiryhmän jäsenten toimittamat aika-, kulu- ja materiaalimerkinnät on hyväksytty.

Dynamics 365 Project Operations Lite -käyttöönottoa ei ole suunniteltu asiakkaiden laskujen tuottamiseen. Seuraavassa luettelossa on esitetty, miksi laskuja ei voi luoda:

- Ei sisällä verotietoja.
- Muita valuuttoja ei voi muuntaa laskutusvaluutaksi.
- Laskujen muotoileminen tulostusta varten ei onnistu oikein.

Sen sijaan voit käyttää talous- tai kirjanpitojärjestelmää luomaan asiakkaille suunnattuja laskuja, joissa käytetään luotujen laskuehdotusten tietoja.

## <a name="creating-project-invoices"></a>Projektilaskujen luominen

Projektilaskuja voidaan luoda yksi kerrallaan tai joukkoina. Voit luoda niitä manuaalisesti tai ne voidaan määrittää siten, että ne luodaan automaattisesti.

### <a name="manually-create-project-invoices"></a>Projektilaskujen manuaalinen luominen 

**Projektisopimukset**-luettelosivulla voit luoda projektilaskuja erikseen kullekin projektisopimukselle tai voit luoda laskuja joukoittain useille projektisopimuksille.

   - Avaa **Projektisopimukset**-luettelosivulla projektisopimus, jolle haluat luoda laskun, ja valitse sitten **Luo lasku**.

   Lasku luodaan kaikille valitun projektisopimuksen tapahtumille, joiden tila on **Laskutusvalmis**. Näitä tapahtumia ovat aika, kulut, materiaalit, välitavoitteet, tuotepohjaiset sopimusrivit ja muut laskuttamattomat myyntikirjauskansion rivit, jotka on mahdollisesti vahvistettu.

Usean laskun luominen yhtä aikaa:

1. Valitse **Projektisopimukset**-luettelosivulla vähintään yksi projektisopimus, jolle luodaan lasku, ja valitse sitten **Luo projektilaskuja**.
2. Varoitusviesti ilmoittaa sinulle, että laskujen luontia voi edeltää viive. Myös prosessi on näkyvissä. Sulje viesti-ikkuna valitsemalla **OK**.

   Lasku luodaan kaikille sopimusrivin tapahtumille, joiden tila on **Laskutusvalmis**. Näitä tapahtumia ovat aika, kulut, materiaalit, välitavoitteet, tuotepohjaiset sopimusrivit ja muut laskuttamattomat myyntikirjauskansion rivit, jotka on mahdollisesti vahvistettu.

3. Tarkastele luotuja laskuja siirtymällä kohtaan **Myynti** \> **Laskutus** \> **Laskut**. Näet yhden laskun kullekin projektisopimukselle.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projektilaskujen automaattisen luomisen määrittäminen 

Automaattinen laskujen luominen määritetään seuraavalla tavalla.

1. Siirry kohtaan **Asetukset** \> **Erätyöt**.
2. Luo erätyö ja anna sille nimeksi **Project Operationsin laskujen luominen**. Eräajon nimen on sisällettävä käsite "Luo laskuja".
3. Valitse **Työtyyppi**-kentässä **Ei mitään**. Asetusten **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.
4. Valitse **Suorita työnkulku**. **Valitse tietue** -valintaikkunassa näkyy seuraavat työnkulut:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valitse **ProcessRunCaller** ja sitten **Lisää**.
6. Valitse seuraavassa valintaikkunassa **OK**. **Lepo**-työnkulkua seuraa **Käsittely**-työnkulku.

    Vaiheessa 5 voit myös valita **ProcessRunner**. Kun tämän jälkeen valitset **OK**, **Käsittely**-työnkulkua seuraa **Lepo**-työnkulku.

Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja. Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**. **ProcessRunner** on se työnkulku, joka luo laskut. Tämä työnkulku käy läpi kaikki sopimusrivit, joille on luotava laskuja, ja luo kyseiset laskut. Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja. Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä. Jos laskujen luomista edellyttäviä tapahtumia ei ole, laskuja ei luoda.

Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller**, antaa päättymisajan ja sulkeutuu. **ProcessRunCaller** käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin. Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.

Laskujen luomisen erätyö on toistuva työ. Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä. Tämän estämiseksi erätyö kannattaa käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.

> [!NOTE]
> Erälaskutus suoritetaan vain sellaisille projektisopimusriveille, jotka on määritetty laskun aikataulun mukaan. Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet. Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu. Sama koskee myös projektipohjaista sopimusriviä.      
 
### <a name="edit-a-draft-invoice"></a>Laskuluonnoksen muokkaaminen

Kun luot projektilaskuluonnoksen, kaikki aika- ja kulumerkintöjen hyväksymisen yhteydessä luodut laskuttamattomat myyntitapahtumat tuodaan laskuun. Voit tehdä seuraavia muutoksia, kun lasku on edelleen luonnosvaiheessa:

- Laskurivin tietojen poistaminen tai muokkaaminen.
- Määrän ja laskutustyypin muokkaaminen.
- Ajan, kulun, materiaalin ja maksujen lisäys tapahtumina suoraan laskuun. Voit käyttää tätä toimintoa, jos laskurivi on yhdistetty sopimusriviin, joka salli nämä tapahtumaluokat.

Vahvista lasku valitsemalla **Vahvista**. Tämä toiminto on yksisuuntainen toiminto. Kun valitset **Vahvista**, lasku muuttuu vain luku -muotoon ja luo laskutetun myynnin todellisia arvoja kullekin laskuriville kunkin laskurivin tietojen perusteella. Jos laskurivin tiedot viittaavat laskuttamattomaan myynnin todelliseen arvoon, laskuttamattoman myynnin todellinen arvo kumotaan. Kaikki ajasta, kulusta tai materiaalin käytöstä luodut laskun rivin tiedot viittaavat laskuttamattomaan myyntitapahtumaan. Kirjanpitointegrointijärjestelmät voivat tämän peruutuksen avulla peruuttaa käynnissä olevan projektin työn (KET) kirjanpitoa varten.

### <a name="correct-a-confirmed-invoice"></a>Vahvistetun laskun korjaaminen

Vahvistettuja laskuja voidaan muokata. Kun korjaat vahvistettua laskua, luodaan uusi korjaava laskuluonnos. Koska oletuksena on, että haluat kumota kaikki alkuperäisen laskun tapahtumat ja määrät, tämä korjaava lasku sisältää kaikki alkuperäisen laskun tapahtumat ja kaikki siinä olevat määrät ovat nollia.

Jos on tapahtumia, jotka eivät ei vaadi korjausta, voit poistaa ne korjaavasta laskuluonnoksesta. Jos haluat kumota tai palauttaa vain osamäärän, voit muokata rivin tietojen **Määrä**-kenttää. Voit tarkastella alkuperäisen laskun määrää avaamalla laskurivin tiedot. Tämän jälkeen voit muokata nykyisen laskun määrää siten, että se ylittää tai alittaa alkuperäisen laskun määrän.

Kun vahvistat korjaavan laskun, alkuperäinen laskutetun myynnin todellinen arvo kumotaan ja uusi laskutetun myynnin todellinen arvo luodaan. Jos määrää vähennettiin, ero aiheuttaa myös uuden laskuttamattoman myynnin todellisen arvon luomisen. Jos alkuperäinen laskutettu myynti esimerkiksi oli kahdeksan tuntia ja korjaavien laskurivien tietojen määrä on vain kuusi tuntia, alkuperäisen laskutetun myynnin rivi peruutetaan ja seuraavat kaksi uutta todellista arvoa luodaan:

- Laskutetun myynnin todellisen arvon kuudelle tunnille.
- Laskuttamattoman myynnin todellisen arvon kahdelle jäljelle jääneelle tunnille. Tämä tapahtuma voidaan joko laskuttaa myöhemmin tai merkitä ei-laskutettavaksi riippuen siitä, mitä asiakkaan kanssa sovitaan.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
