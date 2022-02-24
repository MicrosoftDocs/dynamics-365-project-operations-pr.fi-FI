---
title: Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus
description: Tässä aiheessa on tietoja siitä, miten tilataan ja otetaan käyttöön Project Operations resurssien/ei-varastoitavien skenaarioille.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 917ead8ff6d9d3ef8374f8ccde608b6cebd50c8c
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948460"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä aiheessa kerrotaan, miten voit tilata esiversio-/kumppanitarjouksen ja ottaa käytöön Project Operations -ympäristön resurssien/ei-varastoitavien skenaarioille.

## <a name="prerequisites"></a>Edellytykset

- Saat sähköpostiviestin, jossa saat kutsun osallistumaan esiversioon. Voit pyytää esiversiota [Project Operations -sivustossa](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.
- Finance-ympäristön käyttöönotto edellyttää voimassaolevaa Azure-tilausta, joka laskutetaan ympäristökohtaisesti. Voit aloittaa käyttämällä organisaatiosi olemassa olevaa tilausta tai [Azure-kokeiluversiota](https://azure.microsoft.com/en-us/free/). CDS-ympäristö on maksuton rajoitetulle 30 päivän jaksolle.

## <a name="subscribe"></a>Tilaa

Kun [esiversiopyyntösi](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) hyväksytään, saat kolme Microsoftin tarjousta sähköpostitse. Näiden tarjousten avulla voit ottaa käyttöön Project Operationsin esikatselun:

- Dynamics 365 Project Operations (CRM) - Esiversion kokeiluversio
- Office 365 Project Operationsin esiversion kokeilu
- Dynamics 365 Finance – esiversion kokeilu

> [!IMPORTANT]
> Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa. Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - Esiversion kokeiluversio 

Ennen kuin aloitat, varmista, että olet kirjautunut selaimeen, jossa on käyttäjän työtili, siinä vuokraajan kohdassa, jossa haluat projektin toimintojen esikatselun.

1. Lunasta ensimmäinen tarjouskoodi, **Dynamics 365 Project Operations (CRM) – Esiversion kokeiluversio** liittämällä se selaimen URL-osoitekenttään.

![Lunasta tarjous](./media/16RedeemFirstOfferNew.png)

2. Vahvista tilaus.

![Vahvista tilaus](./media/17ConfirmOrderNew.png)

Näkyviin tulee vahvistus siitä, että tarjouksen lunastaminen onnistui.

![Varmistus](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operationsin esiversion kokeilu

Toista samat vaiheet kuin ensimmäisellä tarjouskoodilla. Muista lisätä toinen tarjouskoodi käyttämällä samaa käyttäjätiliä, jota käytettiin ensimmäisen tarjouskoodin kanssa.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance – esiversion kokeilu

Toista samat vaiheet viimeiselle Tervetuloa-viestin tarjoukselle.

## <a name="assign-licenses"></a>Käyttöoikeuksien määrittäminen

> [!IMPORTANT]
> Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.

1. Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.

![Hallintakeskuksen aloitussivu](./media/14AdminPortal.png)

2. Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.

![Käyttöoikeuksien määrittäminen](./media/15AssignLicenses.png)

3. Tarkista, että **Dynamics 365 Project Operations (CRM) Esiversio** ja **Office 365 Project Operations - Esiversio** -lisenssit on valittu, ja valitse **Tallenna muutokset**.

> [!NOTE]
> Finance-kokeilun tarjousta ei tarvitse delegoida käyttäjälle.

## <a name="start-a-new-project-in-lcs"></a>Aloita uusi projekti LCS:ssä

Luo uusi LCS-projekti aiheessa [Aloita uusi projekti LCS:ssä](create-lcs-project.md) kuvatulla tavalla

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure-tilauksen lisääminen LCS-projektiin

Voit suorittaa tämän tehtävän noudattamalla ohjeitaaiheessa [Lisää Azure-tilaus LCS-projektiin](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance-esittely-ympäristön käyttöönotto Project Operationsin resurssien/ei-varastoitavien skenaarioille

Noudata ohjeita aiheessa [Uuden ympäristön valmistelu](resource-provision-new-environment.md) vimeistelläksesi käyttöönoton. Käytä [esittely-ympäristö](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) -käyttöönottotyyppiä esiversiossa. 

## <a name="install-cds-setup-and-configuration-data"></a>Asenna CDS:n määritys- ja konfiguraatiotiedot

Asenna CDS:n määritys- ja konfiguraatiotiedot aiheessa [Konfiguraatiotietojen määritys ja käyttöönotto Common Data Servicessa](resource-apply-pro-setup-config-data.md) kuvatulla tavalla.
Suorita tämä vaihe vasta sen jälkeen, kun Financen demoympäristö on otettu käyttöön ja esittelytiedot ovat valmiina.


[!INCLUDE[footer-include](../includes/footer-banner.md)]