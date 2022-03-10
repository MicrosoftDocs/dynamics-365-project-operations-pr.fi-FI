---
title: Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus
description: Tässä aiheessa on tietoja siitä, miten tilataan ja otetaan käyttöön Project Operations resurssien/ei-varastoitavien skenaarioille.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f47d5a29c0e40a49aed7b3e52c5d52a9c27b8dbc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323412"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä aiheessa kerrotaan, miten kokeilutarjouksen tilaaminen ja Project Operations -ympäristön käyttöönotto resurssi- tai ei-varastopohjaisissa skenaarioissa suoritetaan.

## <a name="prerequisites"></a>Edellytykset
- Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet. Voit luoda vuokraajan ensimmäisen tarjouksen aikana. 
- Finance-ympäristön käyttöönotto edellyttää voimassaolevaa Azure-tilausta, joka laskutetaan ympäristökohtaisesti. Voit aloittaa käyttämällä organisaatiosi olemassa olevaa tilausta tai [Azure-kokeiluversiota](https://azure.microsoft.com/free/). CDS-ympäristö on maksuton rajoitetulle 30 päivän jaksolle.

> [!IMPORTANT]
> Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa. Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.
> 
> Kokeiluversiot ovat kertakäyttöisiä vuokraajalle. Voit suorittaa kokeiluversion vain kerran. On suositeltavaa luoda uusi vuokraaja kokeilua varten.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – esikatselun kokeiluversio 

Ennen kuin aloitat, varmista, että olet kirjautunut selaimeen, jossa on käyttäjän työtili, siinä vuokraajan kohdassa, jossa haluat projektin toimintojen esikatselun.

1. Lunasta ensimmäinen tarjouskoodi, **Dynamics 365 Project Operations** täällä [Project Operations -kokeiluversio](https://aka.ms/try-po).
2. Vahvista tilaus.

  Näkyviin tulee vahvistus siitä, että tarjouksen lunastaminen onnistui.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance – esiversion kokeilu

Siirry [Dynamics 365 for Finance Preview -kokeiluversioon](https://aka.ms/trypoche) ja toista edellisen osan vaiheet tarjoukselle. Rekisteröidy pilvipalvelussa isännöityyn ympäristöön.  

## <a name="assign-licenses"></a>Käyttöoikeuksien määrittäminen

> [!IMPORTANT]
> Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.

1. Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.

2. Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.

3. Tarkista, että **Dynamics 365 Project Operations** -lisenssi on valittu, ja valitse **Tallenna muutokset**.

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
Suorita tämä vaihe vasta, kun Finance-esittely-ympäristö on otettu käyttöön ja esittelytiedot ovat käyttövalmiita.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
