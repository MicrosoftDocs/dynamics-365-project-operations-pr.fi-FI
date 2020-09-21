---
title: Päivityksen kotisivu
description: Tässä aiheessa kerrotaan, mistä löytää tärkeitä tietoja Dynamics 365 Project Service Automationin uusista ja muuttuneista ominaisuuksista, ja uuteen versioon päivittämisen prosessista.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751210"
---
# <a name="upgrade-home-page"></a>Päivityksen kotisivu

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Päivitä PSA-versiosta 2.x tai 1.x versioon 3.x

### <a name="new-instances"></a>Uudet esiintymät

Kun Project Service Automation valitaan uuden esiintymän valmistelun aikana, 17. toukokuuta 2019 alkaen versio 3. x asennetaan oletusarvoisesti.

### <a name="existing-instances"></a>Käytössä olevat esiintymät

Aiemmin asiakkaiden, joilla on PSA-version 2.x, esiintymä ja joiden täytyi päivittää versioon 3.x, joka on Unified client interface -perustainen (UCI) versio PSA:sta, täytyi ottaa yhteyttä Microsoft-tukeen ja antaa tiedot esiintymästään, jotta tuki pystyi ottamaan esiintymän käyttöön versioon 3.x päivittämiseksi. 1. maaliskuuta 2020 alkaen asiakkaat, joilla on PSA-version 2.x esiintymä ja joiden täytyy päivittää versioon 3.x, voivat päivittää esiintymänsä suoraan hallintaportaalista ottamatta yhteyttä Microsoft-tukeen.  

> [!NOTE]
> PSA-versio 3.x sisältää merkittäviä muutoksia. Se on luotu Unified Interface -kehykseen, joka auttaa parantamaan käyttökokemusta. Uudistettu sovellus tarjoaa yhdenmukaisen ja yhtenäisen käyttöliittymän, ja se noudattaa joustavia suunnitteluperiaatteita, jotka takaavat optimaalisen katselun missä tahansa näytön koossa tai laitteessa. Sovelluksessa on tehty muitakin muutoksia. Muuttuneisiin alueisiin kuuluvat hinnoittelu, varaukset ja resurssien kohdentaminen, aika, kulut ja hyväksynnät.

Suosittelemme, että suoritat seuraavat tehtävät ennen päivitysprosessin aloittamista:

- Tarkista, ovatko sekä Dynamics 365 Field Service että Project Service Automation asennettu tunnistettuun esiintymään. Jos molemmat ratkaisut on asennettu, sinun on päivitettävä molemmat, ennen kuin voit jatkaa esiintymän säännöllistä käyttöä.
- Tutustu seuraaviin aiheisiin huolellisesti. Versioiden välisten muutosten tiedostaminen ja ymmärtäminen auttaa päivitysprosessissa. Nämä aiheet sisältävät tietoja PSA:N merkittävistä muutoksista sekä huomioista ja suosituksista, jotka koskevat päivityksen suunnittelua versioon 3. x.

    - [Uutuudet ja muutokset Project Service Automation -versiossa 3](whats-new-changed-v3.md)
    - [Päivitykseen liittyviä huomioita - Project Service Automation versio 2.x tai 1.x versioon 3](upgrade-v3.md)

- Päivitä Sandbox-esiintymä arvioidaksesi muutoksia toteutukseesi ennen kuin päivität tuotantoesiintymän.

Kun olet tarkistanut aiemmin mainitut aiheet ja olet valmis päivittämään PSA-versioon 3. x tai UCI-pohjaiseen versioon, lähetä pyyntö Microsoftin tuelle, jotta päivitys voidaan asettaa saataville hallintakeskuksesta. Anna pyynnössäsi esiintymäsi tiedot.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Vanhemmat PSA:n versiot (PSA versio 2.x) äskettäin luodussa esiintymässä

17. toukokuuta 2019 alkaen kaikissa uusissa ilmentymissä on käytössä UCI oletusasiakasohjelmana. Jotta muutos olisi linjassa tämän muutoksen kanssa, PSA-versio 3.x ja Field Service versio 8.x tarjotaan oletusarvoisesti, koska nämä versiot on suunniteltu käytettäviksi UCI-asiakasohjelman kanssa.

1. maaliskuuta 2020 alkaen Dynamics PSA:n asiakkaat eivät voi enää luoda uusia ympäristöjä PSA:n vanhemmilla versioilla, kuten PSA-versiolla 2.x tai sitä vanhemmilla. Kaikki uudet ympäristöt saavat vain PSA:n version 3.x.

> [!NOTE]
> Saadaksesi parhaan käyttökokemuksen vanhemmista Field Service - ja PSA-sovelluksista, siirry sivulle **Järjestelmäasetukset**, ja valitse kentälle **Käytä vain uutta Unified Interfacea** arvoksi **Ei**, sillä näitä versioita ei ole suunniteltu ladattavaksi oikein UCI:n. Kun olet poistanut UCI:n käytöstä, voit avata ja suorittaa nämä Field Service - ja PSA-versiot käyttämällä vanhaa www-asiakasohjelmaa. Tietoja UCI-asiakkaan poistamisesta käytöstä on aiheessa [Ota käyttöön ainoastaan unified interface](../admin/enable-unified-interface-only.md).
