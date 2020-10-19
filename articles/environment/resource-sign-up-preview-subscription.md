---
title: Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus
description: Tässä aiheessa on tietoja siitä, miten tilataan ja otetaan käyttöön Project Operations resurssien/ei-varastoitavien skenaarioille.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948842"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa kerrotaan, miten voit tilata esiversio-/kumppanitarjouksen ja ottaa käytöön Project Operations -ympäristön resurssien/ei-varastoitavien skenaarioille.

## <a name="prerequisites"></a>Edellytykset

- Saat sähköpostiviestin, jossa saat kutsun osallistumaan esiversioon. Voit pyytää esiversiota [Project Operations -sivustossa](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.
- Finance-ympäristön käyttöönotto edellyttää voimassaolevaa Azure-tilausta, joka laskutetaan ympäristökohtaisesti. Voit aloittaa käyttämällä organisaatiosi olemassa olevaa tilausta tai [Azure-kokeiluversiota](https://azure.microsoft.com/en-us/free/). CDS-ympäristö on maksuton rajoitetulle 30 päivän jaksolle.

## <a name="subscribe"></a>Tilaa

Kun [esiversiopyyntösi](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) hyväksytään, saat kaksi Microsoftin tarjousta sähköpostitse. Näiden tarjousten avulla voit ottaa käyttöön Project Operationsin esikatselun:

- Dynamics 365 Project Operations – esiversion kokeilu
- Dynamics 365 for Finance and Operations – esiversion kokeilu

> [!IMPORTANT]
> Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa. Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – esiversion kokeilu

1. Lunasta ensimmäinen tarjous, **Dynamics 365 Project Operations -kokeilu** käyttämällä URL-osoitetta Tervetuloa-sähköpostista.

![Ensimmäinen tarjous](./media/1FirstOffer.png)

2. Varmista, että olet kirjautuneena sisään käyttäjänä, joka kuuluu palvelun tilanneeseen organisaatioon.
3. Jatka tarjouksen lunastamista. 
4. Valitse **Kyllä, lisää se tiliini**.

![Lunasta tarjous](./media/2RedeemFirstOffer.png)

![Tarjouksen vahvistaminen](./media/3ConfirmFirstOffer.png)

![Tarjous lunastettu](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance – esiversion kokeilu

Toista samat vaiheet toiselle Tervetuloa-viestin tarjoukselle.

## <a name="assign-licenses"></a>Käyttöoikeuksien määrittäminen

> [!IMPORTANT]
> Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Office 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.

1. Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.

![Office-hallintaportaali](./media/5OfficeAdminPortal.png)

2. Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.

![Käyttöoikeuksien määrittäminen](./media/6AssignLicenses.png)

3. Tarkista, että Project Operations -käyttöoikeus on valittu, ja valitse sitten **Tallenna muutokset**. 

> [!NOTE]
> Finance-kokeilun tarjousta ei tarvitse delegoida käyttäjälle.

## <a name="start-a-new-project-in-lcs"></a>Aloita uusi projekti LCS:ssä

Luo uusi LCS-projekti aiheessa [Aloita uusi projekti LCS:ssä](create-lcs-project.md) kuvatulla tavalla

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure-tilauksen lisääminen LCS-projektiin

Voit suorittaa tämän tehtävän noudattamalla ohjeitaaiheessa [Lisää Azure-tilaus LCS-projektiin](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance-esittely-ympäristön käyttöönotto Project Operationsin resurssien/ei-varastoitavien skenaarioille

Noudata ohjeita aiheessa [Uuden ympäristön valmistelu](resource-provision-new-environment.md) vimeistelläksesi käyttöönoton. Käytä [esittely-ympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) -käyttöönottotyyppiä esiversiossa.

## <a name="install-cds-setup-and-configuration-data"></a>Asenna CDS:n määritys- ja konfiguraatiotiedot

Asenna CDS:n määritys- ja konfiguraatiotiedot aiheessa [Konfiguraatiotietojen määritys ja käyttöönotto Common Data Servicessa](resource-apply-pro-setup-config-data.md) kuvatulla tavalla.

