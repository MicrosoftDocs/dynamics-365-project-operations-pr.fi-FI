---
title: Varausten ja delegointien vertailu
description: Tässä aiheessa on tietoja resurssivarausten ja resurssien delegointien välisistä eroista.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012762"
---
# <a name="bookings-vs-assignments"></a>Varausten ja delegointien vertailu

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin. Sitovat varaukset kuluttavat resurssin kapasiteettia. Varaukset ilmaiset tiimien organisaatiokäsitteitä, jotta ne ymmärtävät, miten resursseja käytetään eri projekteissa. Dynamics 365 Project Operations käsittelee varauksia projektitason konseptina. 

Varauksista poiketen delegoinnit ovat projektiaikataulun projektitehtäviin sitoutettuja resursseja. Resurssit voivat olla nimettyjä tai yleisiä.  Kun resurssitarve johdetaan projektitehtävien delegoinnista, Project Operations käyttää resurssien delegoinnin jaksottumisia resurssitarpeen tietojen jaksottumisen muodostamiseen. Resurssin delegointeja ei kuitenkaan ylläpidetä. Resurssivaatimuksesta johdettujen varausten päivitykset eivät päivitä mitään resurssin delegointeja.

Yleensä resurssin varausten summa on yhtä suuri kuin resurssin delegointien summa yhdessä tai useassa tehtävässä. Project Operations ei kuitenkaan pakota tätä yhdenmukaisuutta. Projektipäällikkö näkee **Täsmäytys**-näkymässä kohteet, joissa resurssin varaukset ja delegoinnit eivät täsmää.




[!INCLUDE[footer-include](../includes/footer-banner.md)]