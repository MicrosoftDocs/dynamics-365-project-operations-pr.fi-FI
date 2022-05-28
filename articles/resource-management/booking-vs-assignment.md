---
title: Varausten ja delegointien vertailu
description: Tässä aiheessa on tietoja resurssivarausten ja resurssien delegointien välisistä eroista.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591262"
---
# <a name="bookings-vs-assignments"></a>Varausten ja delegointien vertailu

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin. Sitovat varaukset kuluttavat resurssin kapasiteettia. Varaukset ilmaiset tiimien organisaatiokäsitteitä, jotta ne ymmärtävät, miten resursseja käytetään eri projekteissa. Dynamics 365 Project Operations käsittelee varauksia projektitason konseptina. 

Varauksista poiketen delegoinnit ovat projektiaikataulun projektitehtäviin sitoutettuja resursseja. Resurssit voivat olla nimettyjä tai yleisiä.  Kun resurssitarve johdetaan projektitehtävien delegoinnista, Project Operations käyttää resurssien delegoinnin jaksottumisia resurssitarpeen tietojen jaksottumisen muodostamiseen. Resurssin delegointeja ei kuitenkaan ylläpidetä. Resurssivaatimuksesta johdettujen varausten päivitykset eivät päivitä mitään resurssin delegointeja.

Yleensä resurssin varausten summa on yhtä suuri kuin resurssin delegointien summa yhdessä tai useassa tehtävässä. Project Operations ei kuitenkaan pakota tätä yhdenmukaisuutta. Projektipäällikkö näkee **Täsmäytys**-näkymässä kohteet, joissa resurssin varaukset ja delegoinnit eivät täsmää.




[!INCLUDE[footer-include](../includes/footer-banner.md)]