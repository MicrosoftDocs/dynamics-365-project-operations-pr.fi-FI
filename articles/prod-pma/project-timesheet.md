---
title: Project Timesheet -mobiilisovellus
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksesta. Project Timesheet -mobiilisovelluksen avulla käyttäjät voivat lähettää ja hyväksyä projektien aikaraportteja mobiililaitteillaan.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110971"
---
# <a name="project-timesheet-mobile-application"></a>Project Timesheet -mobiilisovellus

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yleiskuvaus

Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen avulla käyttäjät voivat lähettää ja hyväksyä projektien aikaraportteja mobiililaitteillaan (iPhone tai Android). Tämä mobiilisovellus näyttää Dynamics 365 Financen projektinhallinnan ja kirjanpidon alueen aikaraporttitoiminnot. Se auttaa parantamaan käyttäjien tuottavuutta ja tehokkuutta sekä ottaa käyttöön projektien aikaraporttien oikea-aikaisen kirjaamisen ja hyväksymisen.

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asennus

Lataa ja asenna Microsoft Dynamics 365 Project Timesheet -mobiilisovellus Androidiin tai iPhonelle mobiilikaupasta laitteeseesi.

## <a name="enable-the-app"></a>Ota sovellus käyttöön 

Project Timesheet -mobiilisovelluksen on oltava käytössä Financessa. Jos haluat ottaa toiminnon käyttöön, siirry kohtaan **Projektinhallinnan ja kirjanpidon parametrit\> Aikaraportti** ja valitse parametri **Ota Microsoft Dynamics 365 Project Timesheet käyttöön**.

### <a name="resolve-sign-in-issues"></a>Sisäänkirjausongelmien ratkaiseminen

**Ongelma:** Projektin aikataulukkomobiilisovelluksen sisäänkirjauksen aikana käyttäjät saavat virhesanoma, jossa kerrotaan, että "sovellusta 2bc50526-cdc3-4e36-a970-c284c34cbd6e ei voi käyttää kyseisessä vuokraajassa".

**Issue:** Projektin aikataulukkomobiilisovelluksen sisäänkirjauksen aikana käyttäjät vastaanottavat virheen, joka muistuttaa jotain seuraavista esimerkeistä:

- "AADSTS50020: Käyttäjätili [käyttäjänimi] tunnistetietojen toimittajalta https://sts.windows.net/[sovelluksen tunnus] ei ole vuokraajassa [vuokraajan tunnus], eikä se voi käyttää kyseisen vuokraajan sovellusta [sovelluksen tunnus]."
- "Valittua käyttäjätiliä ei ole vuokraajassa [vuokraajan tunnus] eikä tili voi käyttää vuokraajan sovellusta [sovelluksen tunnus]."

**Selitys:** Nämä ongelmat aiheutuvat Azure Active Directoryiin (Azure AD) vuoden 2022 toukokuussa tehdystä muutoksesta, joka liittyy ulkoisiin käyttäjiin. Koska tätä muutosta ei tehty talous- ja toimintosovelluksiin, se voi vaikuttaa asiakkaisiin missä tahansa ympäristön tai sovelluksen versiossa.

**Korjaus:** Kaikki ulkoiset käyttäjät on kutsuttava vuokraajaan Azure AD:n kautta. Lisätietoja on kohdassa [Käyttäjien kutsuminen Azure Active Directoryn yritysten välisen yhteistyön avulla](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Kirjaudu sovellukseen

1.  Käynnistä sovellus mobiililaitteessa.

2.  Anna Financen URL-osoitteesi.

3.  Kun kirjaudut sisään ensimmäisen kerran, sinulta kysytään käyttäjätunnusta ja salasanaa. Anna tunnistetiedot.

4. Sinut kirjataan oletusyritykseesi.

## <a name="submit-a-project-timesheet"></a>Projektin työaikaraportin lähettäminen

Voit luoda ja lähettää projektin työaikaraportin sovelluksessa. Voit luoda uuden aikaraportin aikaisemman aikaraportin tietojen, tallennettujen rivien tai projektimääritysten perusteella. Jos sinut on määritetty edustajaksi, voit myös kirjoittaa tuntilomakkeen toiselle työntekijälle. Voit luoda aikaraportin edustajana valitsemalla **Valikko**-painikkeen ja valitsemalla sitten resurssin nimen.

Aikaraporttisivu luo uuden aikaraportin aikaraporttijaksolle kulloisenkin päivämäärän perusteella. Näkyviin tulee työviikko. Jos aikaraportti kattaa useita viikkoja, voit valita toisen työviikon työviikkovälilehdistä.
Jos kulloisellekin päivämäärälle on olemassa aikaraportti, se tulee näkyviin. Jos sinun on luotava uusi aikaraportti toisella aikaraporttijaksolla, valitse **Valikko**-painike ja sitten **Uusi aikaraportti**.

Voit syöttää projektitietoja valitsemalla **Lisää aika** -toiminto tai **Kopioi aika kohteesta** -toiminto. **Kopioi aika kohteesta** -toiminto kopioi projektin rivitiedot, mutta ei tuntimäärää. **Kopioi aika kohteesta** -valikko sisältää seuraavat asetukset:

- **Kopioi aiemmin olemassa olevasta aikaraportista** – Kopioi aikaraporttirivejä olemassa olevasta aikaraportista.

- **Kopioi suosikista** – Luo uusia aikaraporttirivejä käyttäen suosikiksi valitsemiasi aikaraporttiasetuksia.

- **Kopioi määrityksistä** – Luo uusia aikaraporttirivejä määritetyistä projekteista.

Näytettävät projektitiedot riippuvat **Projektinhallinnan ja kirjanpidon parametrit** -sivulla määritetyistä mobiiliparametreista.

Valitse **Oikeushenkilö**-kentässä se oikeushenkilö, jolle olet tehnyt projektityötä. **Oikeushenkilö**-kenttä on käytettävissä vain, jos yritystenvälinen aikaporttien tuki on otettu käyttöön oikeushenkilöllesi.

Valitse aikaraportille asiakas, joka liittyy projektiin. Android-ensijulkaisussa asiakkaan suorittamaa kirjausta ei tueta, koska projekti on valittava ensin. Jos valitsit ensin projektin, **Asiakas**-kenttä täytetään automaattisesti.

Valitse **Projekti**-kentässä projekti, jolle olet kirjaamassa aikaa. **Asiakas**-kenttä täytetään automaattisesti.

Asiakas- ja projektihaut mahdollistavat haun sekä asiakkaissa että projekteissa.

Valitse tiedot kentissä **Luokka**, **Aktiviteetti**, **Riviominaisuus**, **Myyntiveroryhmä** ja **Nimikkeen myyntiveroryhmä** tarpeen mukaan. Nämä kentät voi ohittaa.

**Riviominaisuus**-kentän arvoksi määritetään oletusarvo, joka perustuu projektinhallinnan ja kirjanpidon parametreihin. Kun projektin/luokan ja luokan/resurssin parametrit on otettu käyttöön, **Riviominaisuus**-arvoksi määritetään oletusarvo, jonka olet määrittänyt tälle vahvistukselle. Kun projektin/luokan ja luokan/resurssin parametreja ei ole otettu käyttöön **Riviominaisuus**-arvon oletusarvo määräytyy **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Ota oletusriviominaisuus** -kentän mukaisesti. **Riviominaisuus**-arvo voidaan ohittaa.

Valitse päivä, jolle aika lisätään. Määritä kunakin päivänä tekemäsi tuntimäärä.

Jos haluat lisätä kommentteja syöttämiisi tunneihin, valitse **Lisää kommentteja** ja kirjoita sitten kommentit sisäiselle käyttäjäryhmälle, asiakkaan käyttäjäryhmälle tai molemmille.
Projektipäälliköt voivat tarkastella sisäisiä kommentteja. Asiakkaiden kommentit lisätään laskuihin.

Jos haluat tallentaa rivin suosikiksi, valitse valintaruutu ja valitse sitten **Tallenna suosikiksi**.

Taloushallinnon dimensio- ja liitetukea ei tarjota mobiilisovelluksessa.

Saata aikaraporttisi valmiiksi jatkamalla projektirivien lisäämistä tarpeen mukaan.

Lähetä aikaraportti hyväksynnän työkulkuun valitsemalla **Lähetä**.

## <a name="review-timesheets"></a>Aikaraporttien tarkistaminen

Valikossa on käytettävissä luettelo aikaraporteista, jotka on tarkistettava. Tämä vaihtoehto on käytettävissä vain, jos sinut on määritetty työnkulun hyväksyjäksi. Sekä otsikko- että rivihyväksyntä ovat tuettuja. Rivitason hyväksyntä tarjoaa mahdollisuuden merkitä yhden tai useamman rivin hyväksyntää varten. Kun olet tarkistanut aikaraportin tiedot, jatka työnkulkua valitsemalla **Hyväksy**, **Delegoi** tai **Palaa**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
