---
title: Konsernin sisäiset kulut
description: Työntekijä, joka on yhden yrityksen palveluksessa organisaatiossa, voi suorittaa työn toiselle saman organisaation yritykselle. Tässä tilanteessa voit käyttää konserniyritysten välistä kuluominaisuutta, kun haluat delegoida työntekijän kulut sille yritykselle, jolle työ suoritettiin.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075499"
---
# <a name="intercompany-expenses"></a>Konsernin sisäiset kulut

[!include [banner](../includes/banner.md)]

Työntekijä, joka on yhden yrityksen palveluksessa organisaatiossa, voi suorittaa työn toiselle saman organisaation yritykselle. Tässä tilanteessa voit käyttää konserniyritysten välistä kuluominaisuutta, kun haluat delegoida työntekijän kulut sille yritykselle, jolle työ suoritettiin. Yritystä, jonka palveluksessa työntekijä on, kutsutaan lainaavaksi yritykseksi. Yritystä, jolle työntekijästä aiheutuu kuluja, kutsutaan lainaavaksi yritykseksi. 

Ennen kuin työntekijä voi luoda ja lähettää kuluja työstä, joka suoritetaan eri yritykselle, valitse lainaavalle yritykselle **kulun hallinnan parametrit** -sivulla **Salli konsernin kulurivit** -vaihtoehto. 

## <a name="tax-posting-for-intercompany-expenses"></a>Konsernin sisäisten kulujen verokirjaus

[!include [banner](../includes/banner.md)]

Jos haluat käyttää veroryhmiä, jotka on liitetty (lähde) yritykseen kuluraportin lainaavan (kohde) yrityksen sijaan, sinun täytyy määrittää tämä kirjanpidon arvonlisäveromäärityksessä. Kun kirjanpitoparametri, **konsernin sisäisen veron kirjausyritykselle** on asetettu **lähde** ja **Käytä arvonlisäveron verosääntöjä** -asetukseksi on määritetty **ei** , lainaavan yrityksen veroyhdistelmää käytetään. Kun sama parametri on asetettu **kohteeseen** , käytetään lainaavan yrityksen veroyhdistelmää. Jos kyseessä on Yhdysvaltalainen yritys, kun parametrin arvoksi on määritetty **lähde** , **arvonlisäverosaatavat** -kentän asetukset on määritettävä myös uuden **kirjanpidon kirjausryhmät** -sivulla. Kirjanpitomoduuli käyttää tämän kentän tietoja veroihin liittyvään kirjanpitomerkintään.   
Toiminta on yhdenmukainen projektin kanssa tai ei-kirjattujen kulurivien kanssa.  
