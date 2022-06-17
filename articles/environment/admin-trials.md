---
title: Hanki Project Operationsin kokeiluversio
description: Tässä artikkelissa on tietoja Dynamics 365 Project Operations -kokeiluversion käyttöönotosta.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 7db7ea6b3cffe6eb43ee0519bbaccfc9092c9311
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959429"
---
# <a name="sign-up-for-project-operations-trials"></a>Hanki Project Operationsin kokeiluversio 

_**Koskee:** Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa, Lite-käyttöönotto – kaupasta proformalaskutukseen, Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_ 



Tässä artikkelissa käsitellään kumppanin esiversiotarjouksen tilaamista ja Dynamics 365 Project Operations -ympäristön ottamista käyttöön.

Uuden Project Operations -kokeiluversion avulla voit ottaa käyttöön minkä tahansa kolmesta tuetusta käyttöönottoskenaariosta automaattisesti täyttämällä kyselyn, jossa suositellaan parasta käyttöönottotapaa. Tässä artikkelissa kerrotaan, miten

- Kokeiluversion tarjous lunastetaan.
- Valmistelu aloitetaan.
- Kaksoiskirjoitus määritetään.
- Lisätietoja Project Operationsista. 

Seuraavassa taulukossa on esitetty uuden kokeiluversion tarjouksen tiedot.

| **Tarjouksen kohde**               | **Yksityiskohtaiset tiedot**                                  |
|------------------------------|----------------------------------------------|
| Tarjouksen tyyppi                   | Tämä tarjoustyyppi on järjestelmänvalvojaliidi, joten vuokraajan järjestelmänvalvoja on oltava olemassa, jotta tarjous voidaan lunastaa. |
| Tarjouksen käyttö                    | Kerran vuokraajaa kohden                          |
| Tarjouksen kesto               | 30 kalenteripäivää                             |
| Lunastukset vuokraajaa kohden       | 1                                            |
| Laajennus                    | 1 laajennus, 30 kalenteripäivää               |
| Kokeiluympäristöjen määrä | 3                                            |


## <a name="admin-trial-details"></a>Järjestelmänvalvojan kokeiluversion tiedot
Seuraavassa taulukossa on esitetty kokeiluversion tiedot ja tiedot siitä, miten ne koskevat kutakin käyttöönottotyyppiä.

| **Kohde**                      | **Lite**                                     | **Ei-varastoitavat materiaalit** | **Varastoitavat materiaalit** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Toimitettujen tietojen määrittäminen           | Kyllä                                          | Kyllä                       | Kyllä (USSI)            |
| Tapahtumatiedot            | No                                           | No                        | No                    |
| Valmisteluaika minuuteissa  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Edellytykset
Kun Dynamics 365 Project Operations -kokeiluversio otetaan käyttöön, seuraavat edellytykset on täytettävä.

- Rekisteröityminen [Dynamics 365 Project Operations -kokeiluversion käyttäjäksi](https://www.aka.ms/try-po).
- Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.

> [!IMPORTANT]
> Vain yhden henkilön organisaatiossa, vuokraajan järjestelmänvalvojan, tarvitsee suorittaa tämä tehtävä. Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – kokeiluversion esiversio 

Kirjaudu ennen aloittamista selaimeen käyttäjän työtilillä vuokraajassa, johon haluat Project Operationsin esiversion.

1. Lunasta ensimmäinen tarjouskoodi, **Dynamics 365 Project Operations – esiversion kokeiluversio** liittämällä se selaimen URL-osoitekenttään.

    ![Lunasta tarjous](./media/16RedeemFirstOfferNew.png)

2. Vahvista tilaus.

    ![Vahvista tilaus](./media/17ConfirmOrderNew.png)

  Näet vahvistuksen, että tarjous on nyt onnistuneesti lunastettu.

   ![Vahvistus](./media/18OrderConfirmationNew.png)

  Sinut ohjataan [Power Platform -hallintakeskukseen](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Kysely ja valmistelu

1.  Siirry [Power Platform -hallintakeskukseen](https://admin.powerplatform.com/projectoperationstrial) ja täytä kysely.  
2.  Tarkista suositeltava käyttöönottotyyppi ja valitse **Aloita asennus** aloittaaksesi valmistelun.
3.  Tutustu ehtoihin ja valitse sitten **Aloita**.

   Valmistelun käynnistymisen jälkeen sinut ohjataan ympäristöluetteloon Power Platform -hallintakeskuksessa. Valmistelun aikana ympäristön tila on **PreparingInstance**.
 
  Kun valmistelu on valmis, ympäristön tila on **Valmis**. Ympäristön valmisteluun sisältyy esittelytietojen käyttöönotto.
 
4.  Tarkista käyttöönotto valitsemalla vastaava Microsoft Dataversen URL-osoite ja talous- ja toimintosovellusten URL-osoitteet.

## <a name="configuring-dual-write"></a>Kaksoiskirjoituksen määrittäminen
- Jos haluat määrittää kaksoiskirjoituksen käyttöoikeusroolit, katso kohta [Project Operationsin tietoturva-asetusten päivittäminen Dataversessa](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Kaksoiskirjoitusmääritystä voidaan käyttää siirtymällä talous- ja toimintosovellusesiintymään ja valitsemalla sitten **Tiedonhallinta** > **Kaksoiskirjoitus**.
- Jos haluat tehdä kaksoiskirjoituksen yhdistämismääritykset, katso kohta [Project Operationsin kaksoiskirjoituksen yhdistämismääritysten suorittaminen](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Käyttöoikeuksien määrittäminen

Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.

1. Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.

   ![Hallintakeskuksen aloitussivu](./media/14AdminPortal.png)

2. Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.

   ![Käyttöoikeuksien määrittäminen](./media/15AssignLicenses.png)

3. Tarkista, että **Dynamics 365 Project Operations -esiversion** käyttöoikeus on valittu ja valitse sitten **Tallenna muutokset**.

## <a name="additional-resources"></a>Lisäresurssit

Seuraavissa resursseissa on hyödyllisiä ohjeita Project Operationsin käytön aloittamista varten:

- [Videosarja – Project Operationsin yleiskatsaus, syvällistä perehtymistä ominaisuuksiin ja tiekartta](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Käyttöönottotyypin määrittäminen](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Entä jos edellytän ALM- tai ELM-käytäntöjä talous- ja toimintosovellusten ympäristössä?

- Kumppanit, jotka tarvitsevat täydet ympäristön elinkaaren hallintaominaisuudet, saavat tietoa kohdasta [Kumppanin eristyskäyttöoikeuspyyntö](https://experience.dynamics.com/requestlicense), jossa voi tutustua uuteen kumppanitarjoukseen. 
- Kumppanit, jotka etsivät lisätietoja sisäisistä käyttöoikeuksista, saavat tietoa kohdasta [Sisäinen käyttöoikeuspilvi ja ohjelmistoetu (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Voiko kokeiluversion käyttöä pidentää yli 30 päivään?
Voit pidentää kokeiluversion käyttöä toimimalla seuraavasti.

1. Siirry **Microsoft 365 -hallintakeskuksessa** kohtaan **Laskutus** > **Omat tuotteet**.
2. Valitse **Dynamics 365 Project Operations (CE) – esiversion kokeiluversio**.
3. Kohdassa **Vanhentumispäivä** valitse **Siirrä päivämäärä**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Voiko lite-käyttöönotosta tehdä päivityksen resurssi/ei-varastoitavien skenaarion käyttöönottoon?
Ympäristön päivittämistä lite-versiosta ei-varastoitaviin perustuvaan käyttöönottoon ei tällä hetkellä tueta.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Voinko käyttää Lifecycle Servicesiä (LCS) talousympäristöistäni?  
Ei. Näiden kokeiluversioiden käyttöönotto käsitellään Power Platform -hallintakeskuksessa. Talousympäristön käyttöä on rajoitettu.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Voinko asentaa kokeiluversion olemassa olevaan ympäristöön?
Jos käytössäsi on aiemmin luotu ympäristö, voit asentaa olemassa olevassa Dataversen myyntiympäristössä olevan lite-ympäristön Power Platform -hallintakeskuksesta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
