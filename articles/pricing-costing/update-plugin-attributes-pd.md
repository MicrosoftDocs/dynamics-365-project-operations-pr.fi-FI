---
title: Uusien hinnoitteludimensioiden päivittäminen laajennusmääritteisiin
description: Tässä aiheessa on tietoja laajennusmääritteiden päivittämisestä hinnoitteludimensioille.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643214"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Uusien hinnoitteludimensioiden päivittäminen laajennusmääritteisiin

Tässä aiheessa on tietoja laajennusmääritteiden päivittämisestä hinnoitteludimensioille.

> [!NOTE]
> Tämä aihe koskee vain tarjous- ja sopimusominaisuuksia Dynamics 365 Project Operationsissa.

## <a name="prerequisites"></a>Edellytykset
Ennen kuin suoritat tässä aiheessa kuvatut vaiheet, seuravissa aiheissa kuvattujen toimintosarjojen on oltava suoritettuina:

  - [Mukautettujen kenttien ja entiteettien luominen](create-custom-fields-entities-pricing-dimensions.md) 
  - [Mukautettujen kenttien lisääminen hintamääritys- ja tapahtumaentiteetteihin ](add-custom-fields-price-setup-transactional-entities.md)
  - [Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi](set-up-custom-fields-pricing-dimensions.md). 
  
Jos et ole suorittanut näitä toimintosarjoja loppuun, suorita ne ja palaa sen jälkeen tähän aiheeseen.

## <a name="register-a-plug-in"></a>Laajennuksen rekisteröiminen
Kun tarjousrivin tieto luodaan **Tarjousrivi**-sivulla projektin tarjouriville, järjestelmä luo kaksi arvioriviä. Yksi rivi on arvion kustannuspuolelle, ja toinen rivi on myyntipuolelle. Tämä on sama projektin sopimusriveille.

Kun teet muutoksen määrään tai kenttään kustannuspuolelle, muutos tehdään myös myyntipuolelle. Tämä on mahdollista siksi, että PreOperation-laajennukset, jotka liittyvät Quotelinedetail- ja contractline detail - entiteetteihin, yhdistävät erityiset määritteet kustannuspuolella tapahtuman myyntipuoleen. Jos myyntipuolen hinnoitteludimensioihin tehtyjen muutosten on tultava tehdyiksi myös kustannuspuolelle, seuraavat laajennuksen on rekisteröitävä uudelleen hinnoitteludimensioihin tehtyjen muutosten jälkeen.

Nämä laajennukset on päivitettävä ja rekisteröitävä uudelleen:

- PreOperationContractLineDetailUpdate - **Päivitä msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Päivittää msdyn_quotelinetransaction**

Päivitä laajennukset ja rekisteröi ne uudelleen suorittamalla seuraavat vaiheet.

1. Avaa **PluginRegistrationTool** ja muodosta yhteys Project Operations Dataverse -ympäristöösi.
2. Valitse **Haku** ja kirjoita päivitettävän laajennuksen ensimmäiset kirjaimet.
3. Kun laajennus löytyy, valitse se ja napauta sitten **Valitse päälomakkeessa**.
4. Valitse **Päivitä msdyn_orderlinetransaction** -vaihe, napauta oikealla hiiren painikkeella ja valitse sitten **Päivitä**.
5. Vailtse **Päivitä**-dialogisivulla kolme pistettä (**...**) suodatusmääritteistä.
6. Näkyviin tulee suodatusmääritteet-ikkuna, jossa on luettelo kaikista entiteetin määritteistä ja hinnoitteludimensioista. Valitse hinnoitteludimension määritteiden valintaruudut.
7. Valitse **OK** sulkeaksesi sivun ja valitse sitten **Päivitysvaihe**.
8. Toista vaiheet 2–7 toiselle laajennukselle, **PreOperationQuoteLineDetail**. Tätä laajennusta varten on päivitettävä **Päivitä msdyn_quotelinetransaction** -vaihe.
9. Sulje **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]