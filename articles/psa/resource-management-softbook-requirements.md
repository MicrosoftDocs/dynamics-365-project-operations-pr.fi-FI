---
title: Alustavat varaustarpeet
description: Tässä aiheessa on tietoja alustavien varaustarpeiden käytöstä.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997912"
---
# <a name="soft-book-requirements"></a>Alustavat varaustarpeet

[!include [banner](../includes/psa-now-project-operations.md)]

Resurssivaatimus voi olla sitova. Sitova varaus luo ehdotuksen, joka kuluttaa resurssin kapasiteettia. Tämän jälkeen ehdotus lähetetään pyytäjälle hyväksyttäväksi. Alustava varaus lisää alustavasti resurssin projektiryhmään, ja sillä on eri tila aikataulutaulukossa, mutta se ei kuluta resurssin kapasiteettia. Jos haluat varata resurssin alustavasti aikataulutaulukosta, aseta **Varauksen tila** -kentän arvoksi **Alustava**.

![Varauksen tilaksi määritetty Alustava](media/Resource-Management-image77.png)

Kun **Ryhmä** -välilehti on **Nimetyt ryhmän jäsenet** -näkymässä, resurssi näkyy siinä. Alustavasti varatut tunnit raportoidaan **Alustavasti varatut tunnit** -sarakkeessa.

![Alustavasti varatut tunnit Nimetyt ryhmän jäsenet -näkymässä](media/Resource-Management-image78.png)

Alustavasti varattuja ryhmän jäseniä voi kohdentaa tehtäviin.

![Alustavasti varattuja ryhmän jäseniä kohdennettuina tehtäviin](media/Resource-Management-image79.png)

**Täsmäytys**-välilehdellä ei näytetä varauksia alustavasti varatulle resurssille, koska **Täsmäytys**-välilehti ottaa huomioon vain sitovat varaukset.

![Alustavasti varattu resurssi ilman varauksia Täsmäytys-välilehdellä](media/Resource-Management-image80.png)

> [!NOTE]
> Resurssia ei voi varata alustavasti vaatimuksesta, joka luotiin yleisestä ryhmän jäsenestä.

Aikataulutaulukossa käytetään eri väritystä alustavasti varatuille resursseille.

![Alustava varaus aikataulutaulukossa](media/Resource-Management-image81.png)

Muuttaaksesi alustavan varauksen sitovaksi varaukseksi, napsauta alustavaa varausta hiiren kakkospainikkeella aikataulutaulukossa ja valitse **Muuta tila** \> **Varaa sitovasti** \> **Sitova**.

![Varauksen tilan muuttaminen Sitovaksi](media/Resource-Management-image82.png)

Varausta muutetaan ja tila vaihtuu aikataulutaulukossa. Koska varauksen tila on nyt **Sitova**, resurssi näkyy varattuna, ja sen kapasiteetti ja saatavuus ovat muuttuneet.

Voit käyttää samaa menetelmää sitovan varauksen tai alustavan varauksen peruuttamiseksi aikataulutaulukon kautta.

Muuttaaksesi alustavasti varatun resurssin sitovasti varatuksi, valitse resurssi projektin **Ryhmä**-välilehdellä ja valitse sitten **Vahvista**.

![Vahvista-komento](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]