---
title: Project Operations -integroinnin määrittäminen oikeushenkilöä kohden
description: Tämä aihe sisältää tietoja integroinnin määrittämisestä yrityksen mukaan Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096748"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operations -integroinnin määrittäminen oikeushenkilöä kohden 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aihe käy läpi vaiheet, joita tarvitaan Dynamics 365 Project Operationsin määrittämiseen yrityksen mukaan.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Ota käyttöön ominaisuusavaimet Dynamics 365 Financessa

Ota tarvittavat ominaisuudet käyttöön tekemällä seuraavat toimet.

1. Siirry Dynamics 365 Financessa **Tietojen hallinta** -työtilaan.
2. Etsi **ominaisuusluettelosta** seuraavat ominaisuudet ja ota ne käyttöön:
  
    - **Projektin useiden sopimusrivien ottaminen käyttöön**
    - **Ota käyttöön Project Operations Dynamics 365 Customer Engagementissa**

> [!NOTE]
> Jos **toimintonäppäimiä** ei näy luettelossa, tarkista, että taloushallinnon versio on vähimmäisversiovaatimus (sovelluksen versio 10.0.13, jossa on käytössä kaikki laatupäivitykset tai uudempi). Päivitä ominaisuusluettelo valitsemalla **Tarkista päivitykset**.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Project Operationsin käyttöönoton skenaarion määrittäminen yritykselle

Voit ottaa Project Operationsin käyttöön Dynamics 365 Customer Engagementissa yritystasolla. Sinulla voi olla yksi yritys, joka käyttää Project Operationsia Dynamics 365 Customer Engagementissa resurssilla/ei-varastoitavien skenaarioiden perusteella. Samassa ympäristössä voi olla toinen yritys, joka käyttää projektitoimintoja varastoitujen/tuotantotilausten skenaarioita varten.

1. Valitse Dynamics 365 Financessa **Projektinhallinta ja kirjanpito** > **Määritys** > **Globaalin projektinhallinnan ja kirjanpidon parametrit**.
2. Valitse käytettävissä olevien yritysten luettelosta kohteet, joihin on otettu käyttöön useita sopimusrivejä ja projektitoimintoja Dynamics 365 Customer Engagementissa. Jätä yritykset, jotka käyttävät projektitoimintoja varastoitujen/tuotantotilausten skenaarioita varten.

> [!NOTE]
> Yritys voidaan valita vain, jos sillä ei ole aiemmin luotuja projekteja.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektinhallinnan ja kirjanpidon parametrien määrittäminen

Jokainen yritys, joka käyttää projektitoimintoja Dynamics 365 Customer Engagementissa tarvitsee oletusparametrien joukon. Nämä parametrit määritetään **projektinhallinta ja kirjanpidon parametrit** -sivun **projektitoiminnot** -välilehdessä. Parametrit ovat:

  - **Laskutustyyppioletukset** : Project Operations käyttää kiinteää joukkoa laskutustyyppioletusarvoja, jotka on yhdistettävä rivin ominaisuuksiin Financessa. Tietueen luominen kullekin laskutustyypille: **ei määritetty** , **Laskutettava** , **Ei-laskutettava** , **maksuton** ja **ei käytettävissä**.
  - **Projektiluokan oletusarvot** : Valitse kullekin tapahtumatyypille käytettävät oletusprojektiluokat. Näitä oletusarvoja käytetään **Projektitoimintojen integrointikirjauskansiossa** ja arvioissa, joissa projektin toteutumiselle ei ole määritetty tapahtumaluokkaa.
  - **Ennusteet** : Valitse ennustemalli, jota käytetään aika- ja kuluarvioille.
