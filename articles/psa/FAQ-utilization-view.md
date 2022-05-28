---
title: Resurssien veloitettavan käytön katselu
description: Tässä aiheessa on tietoja resurssin käyttönäkymästä.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0f6240a3337eb78496570ddfabc85d431e61d640
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595632"
---
# <a name="view-chargeable-utilization-for-resources"></a>Resurssien veloitettavan käytön katselu

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Käyttönäkymä** **Project Service -sovelluksen resurssin käyttö** -sivulla näkyy kunkin varattavissa olevan resurssin veloitettava käyttö. Koska näkymä perustuu aikataulutaulukkoon, näkymä sisältää useita samoja toimintoja kuin taulukko.

> ![Käyttönäkymän näyttökuva.](media/FAQ-utilization-1.png)
 

Veloitettavan käytön laskutoimitus tehdään seuraavasti:

   Veloitettava käyttö = (veloitettavat todelliset tunnit) / (resurssin kapasiteetti)

Solut edustavat näkymän valitun jakson (päivät, viikot tai kuukaudet) laskettua veloitettavaa käyttöä.

Kunkin solun värit näyttävät resurssin veloitettavan käytön verrattuna sen veloitettavaan tavoitekäyttöön. 

Tavoitekäyttö voidaan määrittää joko resurssin oletusroolissa tai yksittäisessä roolissa. Laskutoimitus käsittelee ensin tavoitteen yksittäisen resurssin ja sitten resurssin oletusroolin.

## <a name="set-target-on-a-resource"></a>Tavoitteen asettaminen resurssille

1. Siirry kohtaan **Resurssit** \> **Resurssit**. 
2. Avaa tietue valitsemalla resurssi. 
3. **Project Service** -välilehdellä voit myös määrittää resurssin tavoitekäytön.

> ![Näyttökuva Project Service -välilehden käyttämisestä, kun tavoitekäyttöä määritetään.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Tavoitekäytön määritys roolille

1. Siirry kohtaan **Resurssit** \> **Resurssin roolit**. 
2. Valitsemalla rooli ja avaa tietue. 
3. Määritä roolin tavoitekäyttö.

> ![Näyttökuva resurssin roolien käyttämisestä, kun tavoitekäyttöä määritetään.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Resurssin veloitettavan käytön laskeminen

Jos haluat resurssin laskea veloitettavan käytön, sinun on täytettävä tietyt edellytykset. 

### <a name="set-default-role-for-individual-resource"></a>Oletusroolin määrittäminen yksittäiselle resurssille

Ensin on määritettävä tavoitekäyttö joko yksittäiselle resurssille tai resurssin rooleille. Jos käytössä on tavoitteiden resurssin roolit, jokaisella yksittäisellä resurssilla on oltava oletusrooli. 

1. Tee tämä siirtymällä kohtaan **Resurssit** \> **Resurssit**. 
2. Valitse resurssi, avaa tietue ja valitse sitten **Project Service** -välilehti. 
3. Varmista **Resurssin rooli** -ruudukossa, että resurssille on vain yksi rooli ja että kohdan **On oletus** arvoksi on määritetty **Kyllä**.
 
### <a name="change-billing-type-for-resource-role"></a>Resurssin roolin laskutustyypin muuttaminen

Resurssin roolien laskutustyypiksi on määritettävä **Veloitettava**. 

1. Siirry kohtaan **Resurssit** \> **Resurssin roolit**. 
2. Avaa tietue, jota haluat päivittää ja määritä sitten laskutustyypin oletusarvoksi **Veloitettava**.

### <a name="set-working-hours-for-resource-role"></a>Työtuntien määrittäminen resurssin roolille
 
Resurssilla on oltava työtunteja kapasiteetin laskentaa varten. 

1. Siirry kohtaan **Resurssit** \> **Resurssit**. 
2. Avaa tietue valitsemalla resurssi. Valitse sitten **Näytä työtunnit**. 
3. Voit joukkopäivittää resurssiluettelon valitsemalla **Resurssiluettelo**-näkymästä arvon kohdalle **Työtuntimalli**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Veloitettavien todellisten tuntien vianmääritys

Veloitettavat todelliset tunnit saadaan **Todelliset arvot** -entiteetistä. Todelliset arvot, joiden laskutustyyppi on **Veloitettava**, sisällytetään laskelmaan. Tämän vuoksi tarvitaan projekteja, joiden todelliset arvot ovat veloitettavia.

Tarkista seuraavat kohdat, jos et löydä veloitettavaa käyttöä:

- Resurssin kapasiteetille on määritetty työtunteja.
- Resurssilla on joko yksittäinen määritetty käytön tavoite tai sille on delegoitu oletusrooli. Roolille on määritetty käytön tavoite.
- Todellisten arvojen laskutustyyppi on **Veloitettava** sen jakson aikana, jolle odotat käytön laskentaa. Tarkista seuraavat kohdat, jos löydät todellisia arvoja, joiden laskutustyyppi on jokin muu kuin Veloitettava:

  - Todellisessa arvossa käytetyn roolin laskutustyyppi on jokin muu kuin Veloitettava.
  - Projektin taustalla olevan projektisopimusrivin rooliksi on määritetty Ei-veloitettava.
  - Projektiin ei ole liitetty sopimusriviä.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
