---
title: Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus
description: Tässä artikkelissa on tietoja siitä, miten Project Operations tilataan ja otetaan käyttöön resurssien ja ei-varastoitavien skenaarioissa.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842011"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_



Tässä artikkelissa käsitellään kokeilutarjouksen tilaamista ja Project Operations -ympäristön käyttöönottoa resurssi- tai ei-varastopohjaisissa skenaarioissa.

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

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance -esiversion kokeiluversio

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

Uusi LCS-projekti luodaan artikkelissa [Uuden projektin aloittaminen LCS:ssä](create-lcs-project.md) kuvatulla tavalla

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure-tilauksen lisääminen LCS-projektiin

Tämän tehtävä suoritetaan artikkelin [Azure-tilauksen lisääminen LCS-projektiin](resource-add-azure-subscription-lcs-project.md) ohjeiden mukaisesti.

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance-esittely-ympäristön käyttöönotto Project Operationsin resurssien/ei-varastoitavien skenaarioille

Käyttöönotto viimeistellään artikkelin [Uuden ympäristön valmistelu](resource-provision-new-environment.md) ohjeiden mukaisesti. Käytä [esittely-ympäristö](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) -käyttöönottotyyppiä esiversiossa. 

## <a name="install-cds-setup-and-configuration-data"></a>Asenna CDS:n määritys- ja konfiguraatiotiedot

CDS:n asetukset ja määritystiedot asennetaan artikkelin [Määritystietojen asentaminen ja käyttäminen Common Data Servicessa](resource-apply-pro-setup-config-data.md) ohjeiden mukaisesti.
Suorita tämä vaihe vasta, kun Finance-esittely-ympäristö on otettu käyttöön ja esittelytiedot ovat käyttövalmiita.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
