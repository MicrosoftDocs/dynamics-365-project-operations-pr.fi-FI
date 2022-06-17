---
title: Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot
description: Tässä artikkelissa on tietoja hinnoitteludimensioiden laajennusmääritteiden päivittämisestä.
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
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913202"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Jos Project Service Automationin (PSA) tarjous- ja sopimusominaisuuksia ei käytetä, tämä artikkeli voidaan ohittaa.

Artikkelissa oletetaan, että artikkelien [Mukautettujen kenttien ja entiteettien luominen](create-custom-fields-entities.md), [Mukautettujen kenttien lisääminen hintojen määrittelyyn ja tapahtumaentiteetteihin](field-references.md) ja [Mukautettujen kenttien lisääminen hintadimensioiksi](set-up-pricing-dimensions.md) toimintosarjat on suoritettu. Jos et ole suorittanut näitä toimintosarjoja loppuun, palaa niihin, suorita ne ja palaa sitten tähän artikkeliin.

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
