---
title: Microsoft Project Client -integraatio
description: Projektin aikataulun suunnitteleminen ja ylläpitäminen voi olla haastavaa, joten projektipäälliköiden on käytettävä työkaluja, joiden avulla he voivat hallita tätä tehtävää. Microsoft Project Clientiin integrointi tukee projektin työrakenteen avaamista ja hallintaa.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075409"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client -integraatio

[!include [banner](../includes/banner.md)]

Projektin aikataulun suunnitteleminen ja ylläpitäminen voi olla haastavaa, joten projektipäälliköiden on käytettävä työkaluja, joiden avulla he voivat hallita tätä tehtävää. Microsoft Project Clientiin integrointi tukee projektin työrakenteen avaamista ja hallintaa. Projektipäällikkö voi julkaista muutokset takaisin Dynamics 365 Finance -projektin työrakenteeseen.

> [!NOTE]
> Jos käytössä on heinäkuun päivitys (versio 10.0.4), on asennettava tietokannat 4054797 ja 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project Client -lisäosan määrittäminen
Microsoft Project Clientiin integroinnin käyttöönottoa varten on asennettava Microsoft Dynamics 365 -lisäosa käyttäjän Microsoft Project -asiakassovellusta. Tämä tehdään avaamalla **Projektinhallinnan työtila**.

•   Valitse **Määritä projektin asiakaslisäosa** työtilan osassa **Linkit** > **Määritys**.

•   Valitse **Avaa** ja sitten kehotteesta **Suorita**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Olemassa olevan työrakenneluonnoksen avaaminen ja muokkaus Microsoft Project Clientissä
Jos Dynamics 365 Financessa olevalle projektille on jo luotu työrakenne, se voidaan avata o luodulle projektille on luotu työn erittely rakenne, työerittely rakenne voidaan avata Microsoft Project Client -sovelluksessa, jos työrakenne on luonnostilassa. Avaa **Projekti** -sivulta valitsemalla **Avaa Microsoft Projectissa** -linkki **Suunnitelma** -välilehdestä. Tämä sivu voidaan avata myös Microsoft Project Client -sovelluksesta valitsemalla **Avaa** **Microsoft Dynamics 365** -välilehdestä. Valitse luettelosta **Oikeushenkilö** ja **Projekti**.

> [!NOTE]
> Jos käytät Internet Explorer -selainta, sinun on valittava **Tallenna** avataksesi manuaalisesti tiedoston lataussijainnista. Tai **Tallenna ja avaa** avataksesi tidoston Microsoft Project Clientissa. Älä nimeä tiedostoa uudelleen tallennettaessa.

Ennen kuin teet tiedostoon muutoksia Microsoft Project Client -ohjelmalla, sinun on kuitattava se ulos. Valitse **Kuittaa ulos** **Microsoft Dynamics 365** -välilehdessä. Tämä estää muita käyttäjiä muokkaamasta työrakennetta Financessa samalla. Jos haluat julkaista työrakenteen muokkaamisen jälkeen, valitse **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.

Jos projektiin on jo lisätty projektiryhmä Financessa, resurssiluetteloon täytetään ryhmän jäsenet. Jos projektiryhmää ei ole vielä lisätty projektiin, voit valita resursseja ja luoda ryhmän Microsoft Project Client -ohjelmassa napsauttamalla **Resurssit** -painiketta **Microsoft Dynamics 365** -välilehdessä. 

Seuraavat tiedot synkronoidaan takaisin Financeen osana sisäänkuittausprosessia:

•   Tehtävän nimi

•   Alkamispäivä

•   Päättymispäivä

•   Edeltäjät

•   Resurssinimet

•   Luokka

•   Resurssiluokka

•   Työajat

•   Muistiinpanot

•   Prioriteetti

> [!NOTE]
> Jos lisäät Microsoft Project Client -tiedostoon muita sarakkeita, niitä ei tallenneta tiedostoon eikä niitä näytetä, kun tiedosto avataan uudelleen.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Työrakenteen luominen olemassa olevalle projektille Microsoft Project Client -ohjelmalla
Voit luoda uuden työrakenteen Microsoft Project Client -ohjelmalla seuraavasti:


1.  Avaa Microsoft Project Client.

2.  Valitse **Microsoft Dynamics 365** -välilehdessä **Avaa**.

3.  Valitse projektin **Oikeushenkilö**.

4.  Valitse **Projekti**.

5.  Valitse **Microsoft Dynamics 365** -välilehdessä **Kuitta ulos**.

6.  Kun olet valmis julkaisemaan Financeen, valitse **Microsoft Dynamics 365** -välilehdessä **Kuittaa sisään**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Olemassa olevan työrakenteen korvaaminen olemassa olevalle projektille Microsoft Project Client -ohjelmalla
Voit luoda uuden työrakenteen Microsoft Project Client -ohjelmalla ja korvata olemassa olevan projektin olemassa olevan työrakenteen seuraavasti:

1.  Avaa Microsoft Project Client.

2.  Luo aikataulu Microsoft Project Client -ohjelmassa.

3.  Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Korvaa olemassa oleva projekti**.

4.  Valitse projektin **Oikeushenkilö**.

5.  Valitse **Projekti**.

6.  Valitse **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Uuden projektin luominen Microsoft Project Client -ohjelmassa


1.  Avaa Microsoft Project Client.

2.  Luo aikataulu Microsoft Project Client -ohjelmassa.

3.  Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Tallenna uuteen projektiin**.

4.  Valitse projektin **Oikeushenkilö**.

5.  Syötä **Projektitunnus** tarvittaessa.

6.  Syötä **Projektin nimi**.

7.  Valitse **Projektityyppi** , **Projektiryhmä** ja **Projektisopimuksen tunnus**. Voit vaihtoehtoisesti luoda uuden projektisopimuksen valitsemalla **Uusi**.

8.  Valitse resursoinnissa käytettävä **kalenteri**.

11. Valitse **OK**.
