---
title: Uusien mukautettujen entiteettilomakkeiden lisääminen (Project Service Automation 2. x)
description: Tämä aihe sisältää tietoja mukautettujen entiteettilomakkeiden lisäämisestä mahdollisuuksille, tarjouksille tai laskuille Dynamics 365 Project Service Automationin versiossa 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284849"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Uusien mukautettujen entiteettilomakkeiden lisääminen (Project Service Automation 2. x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Tyyppikenttä 

Dynamics 365 Project Service Automation käyttää entiteettien Mahdollisuus, Tarjous, Tilaus ja Lasku **Tyyppi** (**msdyn\_ordertype**) -kenttää erottaakseen kyseisten entiteettien **työperusteiset** versiot **nimikeperusteisista** ja **palveluperusteisista** versioista. PSA käsittelee kyseisten entiteettien työperusteiset versiot. Suuri määrä ratkaisun asiakas- ja palvelinpuolen liiketoimintalogiikasta perustuu **Tyyppi** -kenttään. Siksi on tärkeää, että kenttä valmistellaan oikealla arvolla, kun entiteetit luodaan. Virheellinen arvo voi aiheuttaa virheellistä toimintaa, ja osa liiketoimintalogiikasta saatetaan suorittaa virheellisesti.

## <a name="automatic-form-switching"></a>Automaattinen lomakkeenvaihto

Myyntientiteettitietueiden virheellisestä valmistelusta ja muokkauksesta aiheutuvan mahdollisen tietojen vaurioitumisen ja odottamattomien toimintojen ehkäisemiseksi PSA sisältää nyt automaattisen lomakkeenvaihdon logiikkaa valmiissa lomakkeissa. Tämä logiikka vie käyttäjät oikeaan lomakkeeseen työperusteisellä versiolla tai millä tahansa muulla entiteettien Mahdollisuus, Tarjous, Tila tai Lasku tyypillä työskentelyä varten. Kun käyttäjä avaa entiteetin Mahdollisuus, Tarjous, Tilaus tai Lasku työperusteisen version, lomake vaihtuu lomakkeeksi **Projektitiedot**.

Automaattisessa lomakkeenvaihtologiikassa käytetään arvon **formId** ja kentän **msdyn\_ordertype** välistä yhteyttä. Tähän yhdistämismääritykseen on lisätty kaikki valmiit lomakkeet. Mukautetut lomakkeet on kuitenkin lisättävä manuaalisesti ilmaisemaan, missä entiteetin versiossa ne on tarkoitus käsitellä. Tämä perustuu **msdyn\_ordertype** -kenttään. Jos lomakkeenvaihto puuttuu yhdistämismäärityksestä, logiikka vaihtaa valmiiseen lomakkeeseen sen arvon perusteella, joka on tallennettu entiteetin **msdyn\_ordertype** -kenttään.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Mukautettujen lomakkeiden lisääminen ja lomakkeenvaihtologiikan käyttöönotto

Seuraavassa esimerkissä esitetään mukautetun **Omat projektitiedot** -lomakkeen lisääminen siten, että se toimii työperusteisten mahdollisuuksien kanssa. Samaa prosessia käytetään mukautettujen lomakkeiden lisäämiseen siten, että ne toimivat yhdessä tarjousten, tilausten ja laskujen kanssa.

Voit luoda mukautetun version **Projektitiedot**-lomakkeesta seuraavalla tavalla.

1. Avaa Mahdollisuus-entiteetissä lomake **Projektitiedot** ja tallenna kopio siitä nimellä **Omat projektitiedot**.
2. Avaa uusi lomake ja varmista sitten ominaisuuksissa, että ne sisältävät **Projektitiedot**-lomakkeen lomakkeenvalmistelun komentosarjat. 

    > [!IMPORTANT]
    > Älä poista komentosarjoja. Muulloin osa tiedoista saatetaan valmistella virheellisesti.

3. Tarkista, että lomake sisältää **Tyyppi** (**msdyn\_ordertype**)-kentän. 

    > [!IMPORTANT]
    > Älä poista tätä kenttää. Muussa tapauksessa valmistelukomentosarjat epäonnistuvat.

4. Etsi uuden lomakkeen **formId**-arvo. Voit tehdä tämän kahdella eri tavalla.

    - Vie **Omat projektitiedot** lomake hallitsemattoman ratkaisun osana ja etsi sitten **formId** -arvo viedyn ratkaisun customization.xml-tiedostosta.
    - Avaa lomake **Omat projektitiedot** lomake-editorissa ja etsi sitten **fromid** -parametrin vieressä URL-osoitteessa oleva GUID-tunnus seuraavassa kuvassa näkyvällä tavalla.

    ![Uuden lomakkeen formId-arvo URL-osoitteessa](media/how-to-add-custom-forms-in-v2.0.png)

5. Luo **msdyn\_ordertype** -yhdistämismääritys **formId**-arvolle muokkaamalla verkkoresurssia msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Poista koodi resurssista ja korvaa se seuraavalla koodilla.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Tallenna ja julkaise mukautukset.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]