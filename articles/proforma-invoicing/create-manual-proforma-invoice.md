---
title: Proformalaskut
description: Tässä aiheessa on tietoja proformalaskuista Project Operationsissa.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2050a313fe530065341410d60801b13eb958cb32ae24eb4a0a71ab7ea5061881
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995622"
---
# <a name="proforma-invoices"></a>Proformalaskut

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Proformalaskutus tarjoaa projektipäälliköille toisen hyväksyntätason ennen laskujen luomista asiakkaille. Ensimmäinen hyväksyntätaso on valmis, kun projektiryhmän jäsenten toimittamat aika-, kulu- ja materiaalimerkinnät on hyväksytty. Vahvistetut proformalaskut ovat käytettävissä Project Operationsin Projektin laskenta -moduulissa. Projektin kirjanpitäjät voivat tehdä lisäpäivityksiä, kuten myyntiveron, kirjanpidon ja laskun asettelun.


## <a name="creating-project-invoices"></a>Projektilaskujen luominen

Projektilaskuja voidaan luoda yksi kerrallaan tai joukkoina. Voit luoda niitä manuaalisesti tai ne voidaan määrittää siten, että ne luodaan automaattisesti.

### <a name="manually-create-project-invoices"></a>Projektilaskujen manuaalinen luominen 

**Projektisopimukset**-luettelosivulla voit luoda projektilaskuja erikseen kullekin projektisopimukselle tai voit luoda laskuja joukoittain useille projektisopimuksille.

Tietylle projektisopimukselle luodaan lasku seuraavalla tavalla.

- Avaa projektisopimus **Projektisopimukset**-luettelosivulla ja valitse sitten **Luo lasku**.

    Lasku luodaan kaikille valitun projektisopimuksen tapahtumille, joiden tila on **Laskutusvalmis**. Näitä tapahtumia ovat aika, kulut, materiaalit, välitavoitteet ja muut laskuttamattomat myyntikirjauskansion rivit.

Laskuja luodaan joukoittain seuraavalla tavalla.

1. Valitse **Projektisopimukset**-luettelosivulla vähintään yksi projektisopimus, jolle on luotava lasku, ja valitse sitten **Luo projektilaskuja**.

    Varoitusviesti ilmoittaa sinulle, että laskujen luontia voi edeltää viive. Myös prosessi on näkyvissä.

2. Sulje viesti-ikkuna valitsemalla **OK**.

    Lasku luodaan kaikille sopimusrivin tapahtumille, joiden tila on **Laskutusvalmis**. Näitä tapahtumia ovat aika, kulut, materiaalit, välitavoitteet ja muut laskuttamattomat myyntikirjauskansion rivit.

3. Voit tarkastella luotuja laskuja siirtymällä kohtaan **Myynti** \> **Laskutus** \> **Laskut**. Näet yhden laskun kullekin projektisopimukselle.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projektilaskujen automaattisen luomisen määrittäminen 

Automaattinen laskujen luominen määritetään seuraavalla tavalla.

1. Siirry kohtaan **Asetukset** \> **Erätyöt**.
2. Luo erätyö ja anna sille nimeksi **Project Operationsin laskujen luominen**. Eräajon nimen on sisällettävä käsite "Luo laskuja".
3. Valitse **Työtyyppi**-kentässä **Ei mitään**. Asetusten **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.
4. Valitse **Suorita työnkulku**. **Valitse tietue** -valintaikkunassa näkyy kolme työnkulkua:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valitse **ProcessRunCaller** ja sitten **Lisää**.
6. Valitse seuraavassa valintaikkunassa **OK**. **Lepo**-työnkulkua seuraa **Käsittely**-työnkulku.

    Vaiheessa 5 voit myös valita **ProcessRunner**. Kun tämän jälkeen valitset **OK**, **Käsittely**-työnkulkua seuraa **Lepo**-työnkulku.

Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja. Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**. **ProcessRunner** on se työnkulku, joka tosiasiassa luo laskut. Se käy läpi kaikki sopimusrivit, joille on luotava lasku, ja luo kyseiset laskut. Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja. Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä. Jos laskujen luomista edellyttäviä tapahtumia ei ole, työnkulku ohittaa laskujen luonnin.

Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller**, antaa päättymisajan ja sulkeutuu. **ProcessRunCaller** käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin. Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.

Laskujen luomisen erätyö on toistuva työ. Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä. Siksi erätyö kannatta käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.

> [!NOTE]
> Erälaskutus suoritetaan vain sellaisille projektisopimusriveille, jotka on määritetty laskun aikataulun mukaan. Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet. Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu. Sama koskee myös projektipohjaista sopimusriviä.      
 
### <a name="edit-a-draft-invoice"></a>Laskuluonnoksen muokkaaminen

Kun luot projektilaskuluonnoksen, kaikki aika-, kulu- ja materiaalimerkintöjen hyväksymisen yhteydessä luodut laskuttamattomat myyntitapahtumat tuodaan laskuun. Voit tehdä seuraavia muutoksia, kun lasku on edelleen luonnosvaiheessa:

- Laskurivin tietojen poistaminen tai muokkaaminen.
- Määrän ja laskutustyypin muokkaaminen.

Vahvista lasku valitsemalla **Vahvista**. Vahvistustoimintotoiminto on yksisuuntainen toiminto. Kun valitset **Vahvista**, järjestelmä muuttaa laskun vain luettavaan muotoon ja luo laskutetun myynnin todellisia arvoja kullekin laskuriville kunkin laskurivin tietojen perusteella. Jos laskurivin tiedot viittaavat laskuttamattomaan myynnin todelliseen arvoon, järjestelmä myös kumoaa laskuttamattoman myynnin todellisen arvon. (Kaikki aika- tai kulumerkinnän perusteella luodut laskutusrivin tiedot viittaavat laskuttamattoman myyniin todelliseen arvoon.) Pääkirjan integrointijärjestelmät voivat käyttää tätä kumoamista kumotakseen projektin keskeneräistä työtä kirjanpitotarkoituksia varten.

### <a name="correct-a-confirmed-invoice"></a>Vahvistetun laskun korjaaminen

Vahvistettuja laskuja voidaan muokata (korjata). Kun korjaat vahvistettua laskua, luodaan uusi korjaava laskuluonnos. Koska oletuksena on, että haluat kumota kaikki alkuperäisen laskun tapahtumat ja määrät, tämä korjaava lasku sisältää kaikki alkuperäisen laskun tapahtumat ja kaikki siinä olevat määrät ovat 0 (nolla).

Jos osa tapahtumista ei vaadi korjausta, voit poistaa ne korjaavasta laskuluonnoksesta. Jos haluat kumota tai palauttaa vain osamäärän, voit muokata rivin tietojen **Määrä**-kenttää. Voit tarkastella alkuperäisen laskun määrää avaamalla laskurivin tiedot. Tämän jälkeen voit muokata nykyisen laskun määrää siten, että se ylittää tai alittaa alkuperäisen laskun määrän.

Kun vahvistat korjaavan laskun, alkuperäinen laskutetun myynnin todellinen arvo kumotaan ja uusi laskutetun myynnin todellinen arvo luodaan. Jos määrää vähennettiin, ero aiheuttaa myös uuden laskuttamattoman myynnin todellisen arvon luomiseen. Jos alkuperäinen laskutettu myynti esimerkiksi oli kahdeksan tuntia ja korjaavien laskurivien tietojen määrä on vain kuusi tuntia, alkuperäisen laskutetun myynnin rivi peruutetaan ja seuraavat kaksi uutta todellista arvoa luodaan:

- Laskutetun myynnin todellisen arvon kuudelle tunnille.
- Laskuttamattoman myynnin todellisen arvon kahdelle jäljelle jääneelle tunnille. Tämä tapahtuma voidaan joko laskuttaa myöhemmin tai merkitä ei-veloitettavaksi riippuen siitä, mitä asiakkaan kanssa sovitaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
