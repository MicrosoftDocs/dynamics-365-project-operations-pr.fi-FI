---
title: Konsernin sisäiset kulut
description: Tämä aihe sisältää tietoja siitä, miten konsernin sisäisiä kuluja käytetään työntekijän kulujen kohdistamiseksi sille yritykselle, jolle työ on tehty.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960828"
---
# <a name="intercompany-expenses"></a>Konsernin sisäiset kulut

Työntekijä, joka on yhden yrityksen palveluksessa organisaatiossa, voi suorittaa työn toiselle saman organisaation yritykselle. Voit käyttää konsernin sisäisiä kuluja työntekijän kulujen kohdistamiseksi sille yritykselle, jolle työ on tehty. Yritystä, jonka palveluksessa työntekijä on, kutsutaan lainaavaksi yritykseksi. Yritystä, jolle työntekijästä aiheutuu kuluja, kutsutaan lainaavaksi yritykseksi. 

Ennen kuin työntekijä voi luoda ja lähettää konsernin sisäisiä kuluja, sinun on otettava käyttöön konsernin sisäisten kulujen rivit. Valitse lainan myöntävän yrityksen **Kulujen hallintaparametrit** -sivulta **Salli konsernin sisäisten kulujen rivit**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Konsernin sisäisten kulujen verokirjaus

[!include [banner](../includes/banner.md)]

Ennen kuin voit käyttää lainan myöntävään (lähde) yritykseen liittyviä veroryhmiä lainan ottavan (kohde) yrityksen sijaan kuluraportissa, sinun on otettava käyttöön toiminto pääkirjan arvonlisäveroasetuksissa. Kun **Yritys konsernin sisäistä verokirjausta varten** -parametriksi on asetettu **Lähde** ja **Käytä arvonlisäveron verotussääntöjä** -asetukseksi on valittu **Ei**, lainan myöntävän yrityksen veroyhdistelmää käytetään. Kun sama parametri on asetettu **kohteeseen**, käytetään lainaavan yrityksen veroyhdistelmää. Jos kyseessä on Yhdysvaltalainen yritys, kun parametrin arvoksi on määritetty **lähde**, **arvonlisäverosaatavat**-kentän asetukset on määritettävä myös uuden **kirjanpidon kirjausryhmät** -sivulla. Kirjanpitomoduuli käyttää tämän kentän tietoja veroihin liittyvään kirjanpitomerkintään.   
Toiminta on yhdenmukainen projektin kanssa tai ei-kirjattujen kulurivien kanssa.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]