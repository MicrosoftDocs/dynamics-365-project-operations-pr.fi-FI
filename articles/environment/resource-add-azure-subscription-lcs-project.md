---
title: Azure-tilauksen lisääminen LCS-projektiin
description: Tässä aiheessa on tietoja siitä, miten Azure-tilauksen voi yhdistää LCS-projektiin.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948841"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Azure-tilauksen lisääminen LCS-projektiin

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Pilvipalvelussa isännöidyt ympäristöt on otettava käyttöön aiemmin luodun Azure-tilauksen avulla. Tässä aiheessa on tietoja siitä, miten olemassa olevan Azure-tilauksen voi yhdistää LCS-projektiin. 

## <a name="grant-admin-consent"></a>Myönnä järjestelmänvalvojan suostumus

1. Valitse LCS-projektissa **Ympäristöt**-osassa **Microsoft Azure -asetukset**.

![Microsoft Azure -asetukset](./media/1MicrosoftAzureSettings.png)

2. Valitse **Projektin asetukset**-sivun **Azure-yhdistimet** -välilehdessä **Valtuuta**. Näin ympäristöt voidaan ottaa käyttöön tässä projektissa.

![Azure-yhdistimet](./media/2AzureConnectors.png)

3. Anna järjestelmänvalvojan suostumus valitsemalla uudelleen **Valtuuta**.

![Myönnä järjestelmänvalvojan suostumus](./media/3GrantAdminConsent.png)

4. Hyväksy käyttöoikeuspyyntö.

![Hyväksy käyttöoikeuspyyntö](./media/4AcceptPermissionRequest.png)

Valtuutus on nyt valmis. 

![Valtuutus onnistui](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Dynamics Deployment Services -käyttöoikeuksien antaminen Azure-tilaukselle

1. Siirry kohtaan [Microsoft Azure -laskutus](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) ja valitse tilaus. Dynamics Deployment Services -palveluiden on voitava käyttää tätä tilausta, jotta se voi ottaa ympäristöjä käyttöön.

![Azure-tilauksen tiedot](./media/6AzureSubscription.png)

2. Valitse siirtymisruudusta **Käyttöoikeuksien hallinta (IAM)** ja valitse sitten **Lisää roolin delegointi**.
3. Valitse oikealla puolella olevasta liukusäätimestä **Osallistuja-rooli**  etsi ja valitse näkyviin tulevasta luettelosta **Dynamics Deployment Services**. 
4. Valitse **Tallenna**.

![Tilauksen käyttöoikeudet](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Tilausyhdistimen lisääminen LCS-projektiin

1. Voit lisätä uuden yhdistimen valitsemalla LCS-projektissa **Microsoft Azure -asetukset** -sivulla **Lisää**.
2. Anna Azure-tilaustunnuksesi. Voit etsiä Azure-tilaustunnuksen [Azure-portaalista](https://ms.portal.azure.com/) näytön vasemmassa alakulmassa olevasta **Asetukset**-kohdasta.
3. Valitse **Määritä käyttämään Azure Resource Manageria** -kentässä **Kyllä**.
4. Varmista, että Azuren tilauksen AAD-vuokraajan toimialue vastaa käytettyä toimialueen omistavan Azure-tilausksen toimialuetta ja valitse **Seuraava**.
5. Vahvista valitsemalla **Microsoft Azure -määritys** -näytössä **Seuraava**. Jos näyttöön tulee virhe tässä näytössä, palaa tämän aiheen osaan [Dynamics Deployment Services -käyttöoikeuksien antaminen Azure-tilaukselle](#provide) javarmista, että olet suorittanut kaikki vaiheet.
6. Lataa Azure Management Certificate -varmenne tietokoneen paikalliseen kansioon ja lähetä se sitten Azure Management Portal -portaaliin siirtymällä kohtaan **Asetukset** > **Management Certificates**. Tämän varmenteen avulla LCS voi kommunikoida Azuren kanssa puolestasi. Voit ohittaa tämän vaiheen, jos käyttäjälläsi on tilauksen käyttöoikeus.
7. Valitse **Seuraava**.
8. Valitse Azure-alue, johon otetaan käyttöön, ja valitse sitten palvelinkeskus, joka on lähellä sijaintia, jossa aiot käyttää tätä järjestelmää.
9.  Valitse **Yhdistä**.

Olet yhdistänyt Azure-tilauksen onnistuneesti. Voit nyt ottaa käyttöön Dynamics 365 Financen pilvi-isännöidyt ympäristöt.


