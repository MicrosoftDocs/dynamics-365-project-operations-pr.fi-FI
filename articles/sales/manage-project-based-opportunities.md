---
title: Projektipohjaisten mahdollisuuksien hallinta
description: Tässä aiheessa on tietoja projekteihin liittyvien mahdollisuuksien käyttämisestä.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948371"
---
# <a name="manage-project-based-opportunities"></a>Projektipohjaisten mahdollisuuksien hallinta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektipohjaisten yritysten toimitustoiminnot on yleensä jaettu useisiin maihin ja maantieteellisille alueille. Projektin toteutuksen ja toimituksen kustannukset voivat vaihdella sen mukaan, mikä paikkatieto tai divisioona hallitsee toimitusta. Tämä puolestaan voi vaikuttaa kaupan marginaaliin. Projektiin perustuvien palvelujen toimittamiseen liittyy yleensä suuria määriä henkilöresurssien aikaa, huomattavia matkakuluja, materiaalikustannuksia ja muita kuluja.

Dynamics 365 Project Operationsin projektipohjaiset mahdollisuudet on suunniteltu sisältämään Dynamics 365 Salesin laajennuksia. Aihe sisältää tietoja projektipohjaisten yritysten tarvitsemista lisätoiminnoista eri kentissä ja liiketoimintalogiikasta, joilla hallitaan projektipohjaisia mahdollisuuksia.

## <a name="view-all-project-based-opportunities"></a>Näytä kaikki projektipohjaiset mahdollisuudet

Luettelo kaikista projektipohjaisista mahdollisuuksista näkyy **mahdollisuus**-luettelosivulla. 

1. Siirry kohtaan **Myynti** > **Mahdollisuudet**.
2. Valitse **Näkymien vaihtajasta** muut suodatetut näkymät mahdollisuuksista. Voit luoda omia näkymiä, joissa on mukautettuja suodatusehtoja, näiden näkymien ja siirtymisvaihtoehtojen määrittämistä varten.

Tämän luettelosivun tai tietosivun avulla voit luoda tai poistaa projektimahdollisuuksia.

## <a name="business-process-flow-for-project-based-deals"></a>Projektiin perustuvien tarjousten liiketoimintaprosessi

Seuraavat liiketoimintaprosessit ovat tuettuja Project Operationsin projektipohjaisille sopimuksille:

- Liidistä mahdollisuudeksi -liiketoimintaprosessi
- Mahdollisuuden myynti prosessi

### <a name="lead-to-opportunity-business-process"></a>Liidistä mahdollisuudeksi -liiketoimintaprosessi 
Liidistä mahdollisuudeksi -liiketoimintaprosessi tukee seuraavia vaiheita:

| Vaihe | Yhdistetty entiteetti | Toiminnallisuus |
| --- | --- | --- |
| Hyväksy | Liidi | Hyväksy liidi, jotta luodaan asiakkuus, yhteyshenkilö ja mahdollisuus. |
| Kehitä | Mahdollisuus | Kehitä mahdollisuutta lisäämällä tietoja liittyvistä töistä, keskeisistä sidosryhmistä ja kilpailijoista. |
| Ehdota | Mahdollisuus | Laadi ehdotus ja hanki hyväksyntä sisäiseltä tarkistusryhmältä. |
| Sulje | Mahdollisuus | Kun mahdollisuus voitetaan, sopimus suljetaan. |

### <a name="opportunity-sales-process"></a>Mahdollisuuden myynti prosessi
Project Operationsin mahdollisuuden myyntiprosessi on laajennusmahdollisuus myyntiprosessin liiketoimintavirtaan myyntisovelluksessa. Tämä liiketoimintaprosessi on suunniteltu siten, että se tukee seuraavia projektipohjaisen mahdollisuuden vaiheita.

| Vaihe | Yhdistetty entiteetti | Toiminnallisuus |
| --- | --- | --- |
| Hyväksy | Mahdollisuus | Hyväksy liidi, jotta luodaan asiakkuus, yhteyshenkilö ja mahdollisuus. |
| Ehdota | Tarjous | Laadi ehdotus ja käyttämällä projektitarjouksia ja hanki hyväksyntä sisäiseltä tarkistusryhmältä. |
| Sopimus | Projektin palvelusopimus | Voita tarjous, joka luo palvelusopimuksen ja aloittaa projektin toteutuksen ja toimituksen. |
| Sulje | Projektin palvelusopimus | Viimeistele työn onnistuminen ja sulje projektisopimus. |

> [!NOTE]
> Jos projektipohjainen sopimus on käynnistetty liidistä, mahdollisuus liiketoimintaprosessiin on etusijalla.
>
> Jos projektipohjainen sopimus on käynnistetty mahdollisuudesta, mahdollisuuden myyntiprosessiin on etusijalla.

Voit muokata tuote liiketoimintaprosessin työnkulkua tai luoda omia liiketoimintaprosessien työnkulkuja, joilla voit seurata myyntiprosessia tarpeen mukaan. Lisätietoja liiketoimintaprosesseista on aiheessa [liiketoimintaprosessin kulun yleiskatsaus](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]