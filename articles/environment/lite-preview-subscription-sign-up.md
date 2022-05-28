---
title: Rekisteröityminen esiversion tilaajaksi – lite
description: Tässä aiheessa on tietoja siitä, miten voit tilata ja ottaa käyttöön Project Operationsin lite – kauppa proformalaskutukseen -käyttöönoton.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587996"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Rekisteröityminen esiversion tilaajaksi – lite 

Tässä aiheessa selostetaan kokeilutarjouksen tilaamista ja Dynamics 365 Project Operations -lite-käyttöönottoa kaupasta proformalaskutukseen.

> [!NOTE]
> Tämä prosessi muuttuu Project Operationsin tulevissa versioissa.

## <a name="prerequisites"></a>Edellytykset
- Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet. Voit luoda vuokraajan ensimmäisen tarjouksen aikana.

> [!IMPORTANT]
> Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa. Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.
> 
> Kokeiluversiot ovat kertakäyttöisiä vuokraajalle. Voit suorittaa kokeiluversion vain kerran. On suositeltavaa luoda uusi vuokraaja kokeilua varten.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations-kokeiluversio 

Ennen kuin aloitat, varmista, että olet kirjautunut selaimeen, jossa on käyttäjän työtili, siinä vuokraajan kohdassa, jossa haluat projektin toimintojen esikatselun.

1. Siirry [Project Operations -kokeiluversioon](https://aka.ms/try-po) lunastaaksesi ensimmäisen tarjouskoodin, **Dynamics 365 Project Operations**.
2. Vahvista tilaus.

  Näet vahvistuksen, että tarjous on nyt onnistuneesti lunastettu.

## <a name="assign-licenses"></a>Käyttöoikeuksien määrittäminen

> [!IMPORTANT]
> Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.


1. Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.
2. Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.
3. Tarkista, että **Dynamics 365 Project Operations** -käyttöoikeus on valittu. 
4. Valitse **Tallenna muutokset**.

## <a name="create-a-new-dataverse-environment"></a>Uuden Dataverse -ympäristön luominen

1. Valmistele uusi Project Operations Dataverse -käyttöönottoympäristö noudattamalla aiheen [Dataverse-käyttöönoton malli](lite-deployment.md) -ohjeita. Kun valitset ympäristötyypin, varmista, että käytät **kokeiluversiota (tilaukseen perustuva)**.

  ![Uusi ympäristö.](./media/19CreateEnvironment.png)

2. Valitse **Ota käyttöön Dynamics 365 -sovellukset** -asetus ja jätä **näiden sovellusten automaattinen käyttöönotto** tyhjäksi.  
3. Valitse **Tallenna** luodaksesi ympäristön.

  ![Lisää tietokanta.](./media/20CreateEnvironment1.png)

4. Kun ympäristö on luotu, asenna **Microsoft Dynamics 365 Project Operations** -ratkaisu. 

![Asenna ratkaisu.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Asenna CDS-määritys ja määritä esittelytiedot

Asenna CDS-määritykset ja määritä esittelytiedot noudattamalla ohjeita aiheessa [Ota käyttöön esittelyn määritystiedot](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
