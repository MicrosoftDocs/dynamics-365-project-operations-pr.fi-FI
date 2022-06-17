---
title: Projektin asetukset
description: Tässä artikkelissa on tietoja projektinhallinnan asetuksista.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 3d4b9b920150d31ae2366b4a1ee4168d71d70a17
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915824"
---
# <a name="project-settings"></a>Projektin asetukset

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Seuraavien asetusten avulla voit käyttää projektin suunnitteluominaisuuksia.

## <a name="work-template"></a>Työmalli

Määritä projektin aikataulun luomista varten projektikalenteri, joka määrittää päivittäisten työtuntien määrän ja mahdolliset yrityksen kiinnioloajat. Projektikalenterimallin luomiseksi työmalli liitetään projektin **Kalenterimalli**-kenttään. Luo työmalli seuraavien vaiheiden mukaisesti.

1. Napauta PSA:n vasemmanpuoleisessa navigointipaneelissa **Resurssit**. 
2. Avaa **Resurssit**-listaussivulla käyttäjän tietue, ja valitse sitten **Näytä työtunnit**.

  > [!NOTE]
  > Varmista, että ponnahdusikkunat on sallittu selaimen sivulla. Näin näet resurssille määritetyt työtunnit.
  
3. Napauta **Kuukausinäkymä**-välilehdellä **Määritä**. Kolme vaihtoehtoa sisältävä lista tulee näkyviin: 

  - Uusi viikkoaikataulu
  - Yhden päivän työaikataulu
  - Poissaolo

> ![Määritystoiminnot.](media/project-13.png)

4. Valise **Uusi viikkoaikataulu**, ja määritä sen jälkeen tiedot tälle resurssiaikataululle. Voit määrittää toistuvan viikoittaisen aikataulun, päivittäiset tuntiparametrit, yrityksen kiinnioloajat ja muita seikkoja.
5. Määritä päivämääräväli, valitse **Tallenna**, ja napauta sen jälkeen **Sulje**. 
6. Palaa **Resurssit**-luettelosivulle ja valitse resurssi, jolle määrität työtunnit. 
7. Valitse **Määritä kalenteri** määrittääksesi työmallin. 
8. Syötä **Työmalli**-dialogilaatikossa työmallin nimi, ja valitse sen jälkeen **Käytä**. 

Voit nyt liittää työmallin projektin kalenterimalliin.

## <a name="resource-roles"></a>Resurssiroolit

Termi *resurssirooli* viittaa joukkoon taitoja, osaamista ja sertifikaatteja, jotka henkilöllä on oltava, jotta hän voisi suorittaa tietyn tehtäväjoukon projektissa. PSA:n avulla voit laskea kustannukset ja laskuttaa resurssin ajasta perustuen siihen rooliin, johon resurssi on liitetty. Jokaisen organisaation on määritettävä nämä roolit käyttämällä **Project Service**-valikon vasemmanpuoleista siirtymispainiketta.

Jokaisen organisaation on määritettävä nämä roolit **Aktiiviset resurssiluokat** -sivulla. Valitse vasemmanpuoleisessa siirtymispaneelissa **Resurssiroolit** avataksesi tämän sivun.

## <a name="price-lists"></a>hinnastot

Hinnastot antavat mahdollisuuden määrittää kustannus- ja myyntihinnat resurssirooleille, kululuokille, tuotteille ja muille organisaation elementeille. Ennen kuin asetat talausarvion työlle, joka projektissa on toimitettava, sinun tulisi luoda sitä tukeva kustannus- ja myyntihinnasto. Sinun tulisi myös määrittää parametrit-osiossa oletuskustannus- ja myyntihinnasto, jota sovelletaan kaikkiin organisaatiossa luotuihin projekteihin. Varmista **Aktiiviset projektiparametrit** -sivulla, että määritit oletusarvoisen kustannus- ja myyntihinnaston.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
