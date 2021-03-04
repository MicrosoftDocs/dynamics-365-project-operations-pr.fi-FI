---
title: Rekisteröityminen esiversion tilaajaksi – lite
description: Tässä aiheessa on tietoja siitä, miten voit tilata ja ottaa käyttöön Project Operationsin lite – kauppa proformalaskutukseen -käyttöönoton.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175887"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Rekisteröityminen esiversion tilaajaksi – lite 

Tässä aiheessa on tietoja siitä, miten voit tilata kumppanin esiversiotarjouksen ja ottaa käyttöön Dynamics 365 Project Operationsin lite – kauppa proformalaskutukseen -käyttöönoton.

> [!NOTE]
> Tämä prosessi muuttuu Project Operationsin tulevissa versioissa.

## <a name="prerequisites"></a>Edellytykset

- Saat sähköpostiviestin, jossa saat kutsun osallistumaan esiversioon. Voit pyytää esiversiota [Project Operations -sivustossa](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.
- Tarkista kaikki käyttöehdot.

## <a name="subscribe"></a>Tilaa

Kun vastaanotat [esikatselupyynnön](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) hyväksynnän, saat kaksi Microsoftin tarjousta sähköpostitse. Näiden tarjousten avulla voit ottaa käyttöön Project Operationsin esikatselun:

- Dynamics 365 Project Operations (CRM) – esiversion kokeilu
- Office 365 Project Operationsin esiversion kokeilu

> [!IMPORTANT]
> Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa. Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – esiversion kokeilu 

Ennen kuin aloitat, varmista, että olet kirjautunut selaimeen, jossa on käyttäjän työtili, siinä vuokraajan kohdassa, jossa haluat projektin toimintojen esikatselun.

1. Lunasta ensimmäinen tarjouskoodi, **Dynamics 365 Project Operations (CRM) - esiversion kokeilu** liittämällä se selaimen URL-osoitteeseen.

![Lunasta tarjous](./media/16RedeemFirstOfferNew.png)

2. Vahvista tilaus.
![Vahvista tilaus](./media/17ConfirmOrderNew.png)

Näkyviin tulee vahvistus siitä, että tarjouksen lunastaminen onnistui.

![Varmistus](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operationsin esiversion kokeilu

Toista samat vaiheet kuin ensimmäisellä tarjouskoodilla. Muista lisätä toinen tarjouskoodi käyttämällä samaa käyttäjätiliä, jota käytettiin ensimmäisen tarjouskoodin kanssa.

## <a name="assign-licenses"></a>Käyttöoikeuksien määrittäminen

> [!IMPORTANT]
> Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.


1. Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.

![Hallintakeskuksen aloitussivu](./media/14AdminPortal.png)

2. Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.

![Käyttöoikeuksien määrittäminen](./media/15AssignLicenses.png)

3. Tarkista, että **Dynamics 365 Project Operations (CRM) -esiversion** ja **Office 365 Project Operations -esiversion** käyttöoikeudet ovat valittuina. 
4. Valitse **Tallenna muutokset**.

## <a name="create-a-new-cds-environment"></a>Luo uusi CDS-ympäristö

1. Valmistele uusi Project Operations CDS-käyttööntoton ympäristö noudattamalla aiheen [CDS-käyttöönoton malli](lite-deployment.md). ohjeita Kun valitset ympäristötyypin, varmista, että käytät **kokeiluversiota (tilaukseen perustuva)**.
![Uusi ympäristö](./media/19CreateEnvironment.png)

2. Valitse **Ota käyttöön Dynamics 365 -sovellukset** -asetus ja jätä **näiden sovellusten automaattinen käyttöönotto** tyhjäksi.  
3. Valitse **Tallenna** luodaksesi ympäristön.

![Lisää tietokanta](./media/20CreateEnvironment1.png)

4. Kun ympäristö on luotu, asenna **Microsoft Dynamics 365 Project Operations** -ratkaisu. 

![Asenna ratkaisu](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Asenna CDS-määritys ja määritä esittelytiedot

Asenna CDS-määritykset ja määritä esittelytiedot noudattamalla ohjeita aiheessa [Ota käyttöön esittelyn määritystiedot](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]