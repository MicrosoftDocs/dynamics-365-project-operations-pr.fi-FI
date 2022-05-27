---
title: Projektivarauksen luominen aikataulutaulukosta
description: Tässä aiheessa on tietoja projektivarauksen luomisesta aikataulutaulukosta.
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
ms.openlocfilehash: 693f4c4be1371bae232f636a5e168e889e81b09c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578014"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Projektivarauksen luominen aikataulutaulukosta

[!include [banner](../includes/psa-now-project-operations.md)]

Voit varata resurssin projektiin joko suoraan projektin **Ryhmä**-välilehdessä tai luomalla resurssitarpeen yleisestä ryhmän jäsenen delegoinnista ja täyttämällä luodun tarpeen projektin ryhmän jäsenellä.

Voit varata resurssin projektiin myös suoraan aikataulutaulukosta. Tähän on kolme ratkaisua:

- **Varaus luodusta resurssitarpeesta:** Voit luoda resurssitarpeen, kun olet luonut yleisen resurssin ja kohdentanut tehtäviä projektin sisällä.

- **Varaus ensisijaisesta tarpeesta:** Ensisijaiset tarpeet tulevat näkyviin aikataulutaulukon **Projekti**-välilehdessä. 

- **Varaus uudesta resurssitarpeesta:** Voit luoda resurssitarpeen alusta ja yhdistää sen projektiin. Resurssitarve näkyy aikataulutaulukossa **Avoimet tarpeet** -välilehdessä.

## <a name="book-from-a-generated-resource-requirement"></a>Varaus luodusta resurssitarpeesta

Voit luoda yleisen resurssin ja kohdentaa sille projektissa yhden tehtävän tai useita tehtäviä. Tämän jälkeen voit luoda resurssitarpeen yleisen ryhmän jäsenestä. 

1.  Aikataulutaulukossa tämä resurssi näkyy **Avoimet tarpeet** -välilehdessä. Jos avoimia tarpeita on useita, ruudukossa kannattaa käyttää sarakesuodattimia. 

    ![Aikataulutaulukon Avoimet tarpeet -välilehti.](media/FAQ-Project-Booking-Schedule-Board-1.png "Varausten ja delegointien taulukon näyttökuva")

2. Valitse tarve. **Etsi saatavuus** -välilehti tulee näkyviin valitun rivin yläosassa.
 
3. Kun välilehti valitaan, aikataulutaulukon ajoitusavustajatila käynnistyy ja suodattaa käytettävissä olevat resurssitarvetta vastaavat resurssit. Tämän jälkeen voit valita resurssin.

4. Voit myös vetää ja pudottaa valitun rivin aikataulutaulukon alaosasta yllä olevan ruudukon resurssisoluun. Kun pudotat sen, **Luo resurssin varaus** -paneeli avautuu oikealle.

    Kun valitset **Varaa**, resurssi varataan projektiryhmälle.

![Resurssivarauspaneelin luominen.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Varaus ensisijaisesta tarpeesta

Kun Project Service -sovelluksessa luodaan projekti, luodaan myös resurssitarve nimeltä Ensisijainen tarve. Tämä on tyhjä tarve, jonka avulla resurssi voidaan varata nopeasti aikataulutaulukon avulla ilman, että tarve on luotava alusta alkaen tai muulla tavalla. Koska tarve on tyhjä, tarvittavat päivämäärät, kohdennustapa ja tunnit on määritettävä. 

1. Jos haluat varata resurssin aikataulutaulukon Ensisijainen tarve -kohdassa, valitse **Projekti**-välilehti. Jos projekteja on useita, kannattaa käyttää **Projekti**-sarakkeen sarakesuodatinta.

   ![Sarakesuodattimet aikataulutaulukossa.](media/FAQ-Project-Booking-Schedule-Board-2.png "Varausten ja delegointien taulukon näyttökuva")

2. Valitse tarve, jonka nimi on projektin nimi ja jonka kesto on 0 (nolla).

3. Valitse rivillä näkyvä **Etsi saatavuus** -välilehti. Tällöin aikataulutaulukko siirtyy ajoitusavustajatilaan ja näyttää käytettävissä olevat resurssit, jotka voidaan varata projektiin.

4. Koska **Ensisijainen tarve** on tyhjä tarve, jonka kesto on 0 (nolla), kesto on määritettävä **Luo resurssin varaus** -paneelissa resurssin valitsemisen ja varaamisen yhteydessä.

5. Voit myös valita aikataulutaulukon alaosassa olevan **Projektin ensisijainen tarve** -kohdan ja varata sen vetämällä ja pudottamalla sen resurssiin.
 
    Koska **Ensisijainen tarve** on tyhjä tarve, jonka kesto on 0 (nolla), kesto on määritettävä **Luo resurssin varaus** -paneelissa resurssin valitsemisen ja varaamisen yhteydessä.
 
    Kun resurssi varataan aikataulutaulukon **Ensisijainen tarve** -kohdan kautta, se voidaan lisätä projektiryhmään ilman kohdennuksia.
 
## <a name="book-from-a-new-resource-requirement"></a>Varaus uudesta resurssitarpeesta
Resurssi voidaan varata uudesta resurssitarpeesta seuraavasti. 

1. Siirry **Resurssitarpeet**-kohtaan ja valitse **Uusi** luodaksesi uuden resurssitarpeen.

2. Valitse **Projekti** -välilehdessä projekti yhdistääksesi resurssin projektiin.
 
    Aikataulutaulukossa tämä uusi tarve näkyy muodossa **Avoin tarve**, joka voidaan täyttää.

3. Lisää resurssi projektiryhmään varaamalla se.

4. Nyt kun resurssi on varattu, tehtävät on kohdennettava manuaalisesti.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
