---
title: Varausten ja delegointien vertailu
description: Tässä artikkelissa on tietoja resurssivarausten ja resurssien delegointien välisistä eroista.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918584"
---
# <a name="bookings-vs-assignments"></a>Varausten ja delegointien vertailu

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin. Sitovat varaukset kuluttavat resurssin kapasiteettia. Varaukset ilmaiset tiimien organisaatiokäsitteitä, jotta ne ymmärtävät, miten resursseja käytetään eri projekteissa. Dynamics 365 Project Operations käsittelee varauksia projektitason konseptina. 

Varauksista poiketen delegoinnit ovat projektiaikataulun projektitehtäviin sitoutettuja resursseja. Resurssit voivat olla nimettyjä tai yleisiä.  Kun resurssitarve johdetaan projektitehtävien delegoinnista, Project Operations käyttää resurssien delegoinnin jaksottumisia resurssitarpeen tietojen jaksottumisen muodostamiseen. Resurssin delegointeja ei kuitenkaan ylläpidetä. Resurssivaatimuksesta johdettujen varausten päivitykset eivät päivitä mitään resurssin delegointeja.

Yleensä resurssin varausten summa on yhtä suuri kuin resurssin delegointien summa yhdessä tai useassa tehtävässä. Project Operations ei kuitenkaan pakota tätä yhdenmukaisuutta. Projektipäällikkö näkee **Täsmäytys**-näkymässä kohteet, joissa resurssin varaukset ja delegoinnit eivät täsmää.




[!INCLUDE[footer-include](../includes/footer-banner.md)]