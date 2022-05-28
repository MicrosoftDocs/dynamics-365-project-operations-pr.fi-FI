---
title: Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot
description: Tässä aiheessa on tietoja laajennusmääritteiden päivittämisestä hinnoitteludimensioille.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0c9ac219dd19cf5dd14d54b199329de0c15fe2ae
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580867"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Jos et käytä Project Service Automationin (PSA) tarjous- ja sopimusominaisuuksia, voit ohittaa tämän aiheen.

Aihe olettaa, että olet suorittanut toimintosarjat aiheissa [Luo mukautettuja kenttiä ja entiteettejä](create-custom-fields-entities.md), [Lisää mukautettuja kenttiä hintojen määrittelyyn ja tapahtumaentiteetteihin](field-references.md) ja [Lisää mukautettuja kenttiä hintadimensioiksi](set-up-pricing-dimensions.md). Jos et ole suorittanut näitä toimintosarjoja loppuun, palaa niihin ja suorita ne, ja palaa sen jälkeen tähän aiheeseen.

Kun tarjousrivin tiedot luodaan **Tarjousrivi**-sivulla projektin tarjousriville, järjestelmä luo kaksi arvioriviä taustalle -- yhden rivin arvion kulupuolelle ja toisen myyntipuolelle. Tämä on sama projektin sopimusriveille.

Kun teet muutoksen määrään tai kenttään kustannuspuolelle, muutos välitetään myyntipuolelle. Tämä on mahdollista seuraavien laajennusten vuoksi, jotka on rekisteröitävä uudelleen hinnoitteludimensioiden muutoksen jälkeen.

- PreOperationContractLineDetailUpdate - Päivitykset **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Päivitykset **msdyn_quotelinetransaction**.

Seuraavissa vaiheissa selitetään, miten laajennukset rekisteröidään.

1. Avaa **PluginRegistrationTool** ja muodosta yhteys online-ilmentymään.
2. Napauta **Hae** ja etsi päivitettävä laajennus.

 ![Kuvakaappaus hakupuusta.](media/PRT-1.png)

3. Kun laajennus löytyy, valitse se ja napauta sitten **Valitse päälomakkeessa**.

4. Valitse päivitettävän laajennuksen vaihe, napsauta hiiren kakkospainiketta ja valitse sitten **Päivitä**.

 ![Päivitettävän laajennuksen kuvakaappaus.](media/PRT-2.png)
 
5. Napauta päivitysikkunassa painiketta, jossa on kolme pistettä (**...**) suodatusmääritteissä.

 ![Kuvakaappaus määrittelytiedoista Nykyisen vaiheen päivittämiselle.](media/PRT-3.png)
 
6. Valitse hinnoittelumääritteiden valintaruudut.

 ![Kuvakaappaus, jossa valintaruutu valitaan hinnoittelumääritteille.](media/PRT-4.png)

7. Napauta **OK** sulkeaksesi sivun ja valites sitten **Päivitysvaihe**.

 ![Kuvakaappaus, jossa näkyy "Päivitysvaihe"-painike.](media/PRT-5.png)
 
8. Toista tämä prosessi toiselle laajennukselle **PreOperationQuoteLineDetail - Päivitä msdyn_quotelinetransaction**.

9. Sulje laajennuksen rekisteröintityökalu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
