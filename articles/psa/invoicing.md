---
title: Laskutus Project Service Automationissa
description: Tässä aiheessa on tietoja laskutuksesta.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075412"
---
# <a name="invoicing-in-project-service-automation"></a>Laskutus Project Service Automationissa

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Laskutus Dynamics 365 Project Service Automationissa on käytännöllistä, koska se tarjoaa projektipäälliköille toisen hyväksyntätason ennen laskujen luomista asiakkaille. Ensimmäinen hyväksyntätaso on valmis, kun projektiryhmän jäsenten toimittavat aika- ja kulumerkinnät on hyväksytty.

PSA:ta ei seuraavista syistä ole suunniteltu luomaan asiakkaille suunnattuja laskuja:

- Se ei sisällä verotietoja.
- Se ei pysty muuntamaan muita valuuttoja laskutusvaluutaksi oikein määritetyillä vaihtokursseilla.
- Se ei pysty muotoilemaan laskuja tulostettavaan muotoon.

Sen sijaan voit käyttää talous- tai kirjanpitojärjestelmää luomaan asiakkaille suunnattuja laskuja, joissa käytetään PSA:ssa luotavien laskuehdotusten tietoja.

## <a name="creating-project-invoices-in-psa"></a>Projektilaskujen luonti PSA:ssa

Projektilaskuja voidaan luoda yksi kerrallaan tai joukkoina. Voit luoda niitä manuaalisesti tai ne voidaan määrittää siten, että ne luodaan automaattisesti.

### <a name="manually-create-project-invoices-in-psa"></a>Projektilaskujen manuaalinen luonti PSA:ssa

**Projektisopimukset** -luettelosivulla voit luoda projektilaskuja erikseen kullekin projektisopimukselle tai voit luoda laskuja joukoittain useille projektisopimuksille.

Tietylle projektisopimukselle luodaan lasku seuraavalla tavalla.

- Avaa projektisopimus **Projektisopimukset** -luettelosivulla ja valitse sitten **Luo lasku**.

    ![Projektilaskujen luominen tietylle projektisopimukselle](media/CreateProjectInvoicesOneByOne.png)

    Lasku luodaan kaikille valitun projektisopimuksen tapahtumille, joiden tila on **Laskutusvalmis**. Näitä tapahtumia ovat aika, kulut, välitavoitteet ja projektiperusteiset sopimusrivit.

Laskuja luodaan joukoittain seuraavalla tavalla.

1. Valitse **Projektisopimukset** -luettelosivulla vähintään yksi projektisopimus, jolle on luotava lasku, ja valitse sitten **Luo projektilaskuja**.

    ![Projektilaskujen luonti joukoittain](media/CreateProjectInvoicesBulk.png)

    Varoitusviesti ilmoittaa sinulle, että laskujen luontia voi edeltää viive. Myös prosessi on näkyvissä.

2. Sulje viesti-ikkuna valitsemalla **OK**.

    Lasku luodaan kaikille sopimusrivin tapahtumille, joiden tila on **Laskutusvalmis**. Näitä tapahtumia ovat aika, kulut, välitavoitteet ja projektiperusteiset sopimusrivit.

3. Voit tarkastella luotuja laskuja siirtymällä kohtaan **Myynti** \> **Laskutus** \> **Laskut**. Näet yhden laskun kullekin projektisopimukselle.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Projektilaskujen automaattisen luonnin määrittäminen PSA:ssa

Automaattinen laskujen luonti määritetään PSA:ssa seuraavalla tavalla.

1. Siirry kohtaan **Project Service** \> **Asetukset** \> **Erätyöt**.
2. Luo erätyö ja anna sille nimeksi **PSA Create Invoices**. Eräajon nimen on sisällettävä käsite "Luo laskuja".
3. Valitse **Työtyyppi** -kentässä **Ei mitään**. Asetusten **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.
4. Valitse **Suorita työnkulku**. **Valitse tietue** -valintaikkunassa näkyy kolme työnkulkua:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valitse **ProcessRunCaller** ja sitten **Lisää**.
6. Valitse seuraavassa valintaikkunassa **OK**. **Lepo** -työnkulkua seuraa **Käsittely** -työnkulku.

    Vaiheessa 5 voit myös valita **ProcessRunner**. Kun tämän jälkeen valitset **OK** , **Käsittely** -työnkulkua seuraa **Lepo** -työnkulku.

Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja. Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**. **ProcessRunner** on se työnkulku, joka tosiasiassa luo laskut. Se käy läpi kaikki sopimusrivit, joille on luotava lasku, ja luo kyseiset laskut. Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja. Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä. Jos laskujen luomista edellyttäviä tapahtumia ei ole, työnkulku ohittaa laskujen luonnin.

Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller** , antaa päättymisajan ja sulkeutuu. **ProcessRunCaller** käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin. Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.

Laskujen luomisen erätyö on toistuva työ. Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä. Siksi erätyö kannatta käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.

> [!NOTE]
> Project Service Automationin erälaskutus suoritetaan vain laskutusaikataulujen määrittämillä projektisopimusriveillä. Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet. Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu. Tietoja laskutustiheyksien määrittämisestä tarjousriviin perustuvassa projektissa on kohdassa [Tarjoukset ja tarjousrivit](basic-quote-lines.md#invoice-schedule). Sama koskee myös projektipohjaista sopimusriviä.      
 
### <a name="edit-a-draft-psa-invoice"></a>PSA-laskun luonnoksen muokkaaminen

Kun luot projektilaskuluonnoksen, kaikki aika- ja kulumerkintöjen hyväksymisen yhteydessä luodut laskuttamattomat myyntitapahtumat tuodaan laskuun. Voit tehdä seuraavia muutoksia, kun lasku on edelleen luonnosvaiheessa:

- Laskurivin tietojen poistaminen tai muokkaaminen.
- Määrän ja laskutustyypin muokkaaminen.
- Ajan, kulun ja maksujen lisäys tapahtumina suoraan laskuun. Voit käyttää tätä toimintoa, jos laskurivi on yhdistetty sopimusriviin, joka salli nämä tapahtumaluokat.

Vahvista lasku valitsemalla **Vahvista**. Vahvistustoimintotoiminto on yksisuuntainen toiminto. Kun valitset **Vahvista** , järjestelmä muuttaa laskun vain luettavaan muotoon ja luo laskutetun myynnin todellisia arvoja kullekin laskuriville kunkin laskurivin tietojen perusteella. Jos laskurivin tiedot viittaavat laskuttamattomaan myynnin todelliseen arvoon, järjestelmä myös kumoaa laskuttamattoman myynnin todellisen arvon. (Kaikki aika- tai kulumerkinnän perusteella luodut laskutusrivin tiedot viittaavat laskuttamattoman myyniin todelliseen arvoon.) Pääkirjan integrointijärjestelmät voivat käyttää tätä kumoamista kumotakseen projektin keskeneräistä työtä kirjanpitotarkoituksia varten.

### <a name="correct-a-confirmed-psa-invoice"></a>Vahvistetun PSA-laskun korjaus

Vahvistettuja PSA-laskuja voidaan muokata (korjata). Kun korjaat vahvistettua laskua, luodaan uusi korjaava laskuluonnos. Koska oletuksena on, että haluat kumota kaikki alkuperäisen laskun tapahtumat ja määrät, tämä korjaava lasku sisältää kaikki alkuperäisen laskun tapahtumat ja kaikki siinä olevat määrät ovat 0 (nolla).

Jos osa tapahtumista ei vaadi korjausta, voit poistaa ne korjaavasta laskuluonnoksesta. Jos haluat kumota tai palauttaa vain osamäärän, voit muokata rivin tietojen **Määrä** -kenttää. Voit tarkastella alkuperäisen laskun määrää avaamalla laskurivin tiedot. Tämän jälkeen voit muokata nykyisen laskun määrää siten, että se ylittää tai alittaa alkuperäisen laskun määrän.

Kun vahvistat korjaavan laskun, alkuperäinen laskutetun myynnin todellinen arvo kumotaan ja uusi laskutetun myynnin todellinen arvo luodaan. Jos määrää vähennettiin, ero aiheuttaa myös uuden laskuttamattoman myynnin todellisen arvon luomiseen. Jos alkuperäinen laskutettu myynti esimerkiksi oli kahdeksan tuntia ja korjaavien laskurivien tietojen määrä on vain kuusi tuntia, PSA kumoaa alkuperäisen laskutetun myynnin rivin ja luo kaksi uutta todellista arvoa:

- Laskutetun myynnin todellisen arvon kuudelle tunnille.
- Laskuttamattoman myynnin todellisen arvon kahdelle jäljelle jääneelle tunnille. Tämä tapahtuma voidaan joko laskuttaa myöhemmin tai merkitä ei-veloitettavaksi riippuen siitä, mitä asiakkaan kanssa sovitaan.
