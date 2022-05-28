---
title: Project Operations Dataverse -sovelluksen käyttöönotto manuaalisesti kaksoiskirjoituksen tuella
description: Tässä aiheessa kerrotaan, miten Project Operations Dataverse-sovellus voidaan ottaa käyttöön manuaalisesti siten, että se tukee kaksoiskirjoitusta.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591216"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Project Operations Dataverse -sovelluksen käyttöönotto manuaalisesti kaksoiskirjoituksen tuella

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa kerrotaan, miten Microsoft Dynamics 365 Project Operations Microsoft Dataversessa voidaan ottaa käyttöön manuaalisesti siten, että se tukee kaksoiskirjoitusta. Project Operations havaitsee ympäristön määritykset ja lisää lisätuen kaksoiskirjoitukselle, jos vaatimukset täyttyvät.

Jos olet toiminut tämän aiheen ohjeiden mukaisesti käyttöönoton aikana Microsoft Dynamics Lifecycle Services (LCS) -palvelussa, voit ohittaa Microsoft Power Platform -integroinnin käyttöönoton (jota kutsuttiin aiemmin Common Data Service -ympäristöksi).

Project Operationsin käyttöönotossa Dataversessa siten, että se tukee kaksoiskirjoitusta, on neljä päävaihetta:

1. [Luo Dataversessa uusi ympäristö, joka tukee kaksoiskirjoitusta](#create).
2. [Lisää kaksoiskirjoituksen vaatimukset ympäristöön](#prerequisites).
3. [Lisää Project Operations Dataverse -sovellus](#dataverse).
4. [Linkitä ympäristösi](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Luo Dataversessa uusi ympäristö, joka tukee kaksoiskirjoitusta

Voit suorittaa tämän menettelyn kirjautumalla sisään järjestelmänvalvojana.

1. Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.com) ja kirjaudu sisään järjestelmänvalvojana.
2. Luo uusi ympäristö ja nimeä se.
3. Valitse ympäristötyyppi. Jos rekisteröidyit kokeilutarjousta varten, valitse **Kokeilu (tilauspohjainen)**.
4. Vahvista käyttöönottoalue.
5. Ota käyttöön **Luo tietokanta tätä ympäristöä varten** -vaihtoehto. 
6. Vahvista kieli ja vahvista sitten, että valuutta vastaa talous- ja toimintosovellusten valuuttaa.
7. Ota **Dynamics 365 -sovellukset** -vaihtoehto käyttöön ja vahvista, että **Ota nämä sovellukset käyttöön automaattisesti** -kentän asetus on **Ei mitään**.
8. Lisää käyttöoikeusryhmä, jos käyttöoikeusryhmä on pakollinen.
9. Valitse **Tallenna** luodaksesi ympäristön.
10. Odota käyttöönoton valmistumista ja että ympäristön tila on **Valmis**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Lisää kaksoiskirjoituksen vaatimukset ympäristöön

Kaksoiskirjoituksen tuki sisältää lisäkenttiä, jotka lisätään avainentiteetteihin, kuten **Yritys**-entiteettiin. Jos lisäät kaksoiskirjoituksen tukea olemassa olevaan ympäristöön, tiedot on ehkä päivitettävä, jotta tuki voidaan ottaa käyttöön. Tietoja olemassa olevien tietojen käytössä on aiheessa[Käytä olemassa olevia yritystietoja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Lisätietoja kaksoiskirjoituksesta on aiheessa [Kaksoiskirjoituksen järjestelmävaatimukset](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Suorita tämä menettely lisätäksesi kaksoiskirjoituksen vaatimukset ympäristöösi.

1. Avaa juuri luomasi ympäristö ja siirry sitten kohtaan **Resurssi** \> **Dynamics 365 -sovellukset**.
2. Valitse sovellusluettelosta **Kaksoiskirjoituksen ydinratkaisu** ja asenna se.
3. Odota asennuksen valmistumista. Valitse sitten sovellusluettelosta **Kaksoiskirjoituksen järjestämisratkaisu** ja asenna se.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Lisää Project Operations Dataverse -sovellus

Voit suorittaa tämän menettelyn vain, jos olet suorittanut aiemmat menettelyt ennen Project Operationsin asentamista. Asennuksen aikana järjestelmä analysoi ympäristön määritykset ja lisää tarvittaessa kaksoiskirjoituksen tuen.

1. Avaa aiemmin luomasi ympäristö ja siirry sitten kohtaan **Resurssi** \> **Dynamics 365 -sovellukset**.
2. Valitse sovellusluettelosta **Microsoft Dynamics 365 Project Operations** ja asenna se.

## <a name="link-your-environments"></a><a name="link"></a>Linkitä ympäristösi

Kun Dataverse-ympäristö on otettu käyttöön, voit määrittää linkin talous- ja toimintosovelluksiin. Seuraa ohjeita kohdassa [Käytä kaksoiskirjoituksen opastettua toimintoja ympäristöihisi linkittämistä varten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
