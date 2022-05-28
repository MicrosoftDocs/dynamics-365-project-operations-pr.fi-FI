---
title: Project Operations -integroinnin määrittäminen oikeushenkilöä kohden
description: Tämä aihe sisältää tietoja integroinnin määrittämisestä yrityksen mukaan Project Operationsissa.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585834"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operations -integroinnin määrittäminen oikeushenkilöä kohden 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa kuvaillaan Dynamics 365 Project Operationsin yrityskohtaisen määrittämisen vaiheita.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Toimintonäppäinten ottaminen käyttöön Dynamics 365 Financessa

Ota tarvittavat ominaisuudet käyttöön tekemällä seuraavat toimet.

1. Avaa Dynamics 365 Financessa **Ominaisuuksien hallinta** -työtila.
2. Etsi **ominaisuusluettelosta** seuraavat ominaisuudet ja ota ne käyttöön:
  
    - **Projektin useiden sopimusrivien ottaminen käyttöön**
    - **Ota käyttöön Project Operations – Dynamics 365 Customer Engagement**

> [!NOTE]
> Jos **toimintonäppäimiä** ei näy luettelossa, tarkista, että taloushallinnon versio on vähimmäisversiovaatimus (sovelluksen versio 10.0.13, jossa on käytössä kaikki laatupäivitykset tai uudempi). Päivitä ominaisuusluettelo valitsemalla **Tarkista päivitykset**.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Project Operationsin käyttöönoton skenaarion määrittäminen yritykselle

Voit ottaa käyttöön Project Operations – Dynamics 365 Customer Engagementin yritystasolla. Voit määrittää yhden yrityksen käyttämällä Project Operations – Dynamics 365 Customer Engagementia resurssi/ei-varastoitu -skenaarioissa. Samassa ympäristössä voi olla toinen yritys, joka käyttää projektitoimintoja varastoitujen/tuotantotilausten skenaarioita varten.

1. Siirry Dynamics 365 Financessa kohtaan **Projektinhallinta ja kirjanpito** > **Määritys** > **Yleiset projektinhallinnan ja kirjanpidon parametrit**.
2. Valitse käytettävissä olevien yritysten luettelosta entiteetit, joissa Project Operations – Dynamics 365 Customer Engagementin ominaisuuksissa otetaan käyttöön useita sopimusrivejä. Jätä yritykset, jotka käyttävät projektitoimintoja varastoitujen/tuotantotilausten skenaarioita varten.

> [!NOTE]
> Yritys voidaan valita vain, jos sillä ei ole aiemmin luotuja projekteja.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektinhallinnan ja kirjanpidon parametrien määrittäminen

Jokainen Project Operations - Dynamics 365 Customer Engagementia käyttävä yritys tarvitsee oletusparametrien joukon. Nämä parametrit määritetään **projektinhallinta ja kirjanpidon parametrit** -sivun **projektitoiminnot**-välilehdessä. Parametrit ovat:

  - **Laskutustyyppioletukset**: Project Operations käyttää kiinteää joukkoa laskutustyyppioletusarvoja, jotka on yhdistettävä rivin ominaisuuksiin Financessa. Tietueen luominen kullekin laskutustyypille: **ei määritetty**, **Laskutettava**, **Ei-laskutettava**, **maksuton** ja **ei käytettävissä**.
  - **Projektiluokan oletusarvot**: Valitse kullekin tapahtumatyypille käytettävät oletusprojektiluokat. Näitä oletusarvoja käytetään **Projektitoimintojen integrointikirjauskansiossa** ja arvioissa, joissa projektin toteutumiselle ei ole määritetty tapahtumaluokkaa.
  - **Ennusteet**: Valitse ennustemalli, jota käytetään aika- ja kuluarvioille.


[!INCLUDE[footer-include](../includes/footer-banner.md)]