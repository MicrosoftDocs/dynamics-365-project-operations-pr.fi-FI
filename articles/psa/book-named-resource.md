---
title: Nimettyjen resurssien varaaminen resurssitarpeista.
description: Tässä aiheessa on tietoja nimettyjen resurssien varaamisesta yleistä resurssitarvetta varten.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: d7ff58ec08661adc702867c6c26805a74a3637c9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125894"
---
# <a name="book-named-resources-from-resource-requirements"></a>Nimettyjen resurssien varaaminen resurssitarpeista.

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Voit varata nimetyn resurssin korvaamaan yleisen resurssin, jolla on resurssitarve.

1. Napsauta Project Service Automationin (PSA:n) **Projektit** -sivulla **Ryhmä** -välilehteä.
2. Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Varaa**. Voit myös avata resurssitarpeen ja napsauttaa **Varaa**.


![Yleisen ryhmän jäsenen varaus](media/RM-how-to-14.png)


3. Valitse **Ajoitusavustaja**-sivulla projektiryhmääsi varattava nimetty resurssi ja napsauta **Varaa**.

![Yleisen ryhmän jäsenen varaaminen ajoitusavustajalla](media/RM-how-to-15.png)

Kun varaus on valmis ja nimetty resurssi on täyttänyt sen, yleinen resurssi korvataan nimetyllä resurssilla.

![Nimetty ryhmän jäsen korvaa yleisen ryhmän jäsenen](media/RM-how-to-16.png)

Myös aikataulun kohdennukset päivitetään nimetyllä resurssilla.

![Nimetty ryhmän jäsen kohdennettuna projektitehtäville](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Yleisen resurssin täyttäminen useilla nimetyillä resursseilla
Yleisen resurssin tarpeen täyttäminen useilla nimetyillä resursseilla vastaa yksittäisen nimetyn resurssin kohdentamista. Otetaan esimerkiksi viisi päivää ja 120 tuntia työtä vaativa tehtävä. Yksittäinen yleensä kahdeksantuntista työpäivää viiden päivän työviikoilla tekevä resurssi ei voi suorittaa tätä tehtävää. 

![Tehtävä vaatii 120 työtuntia viiden päivän aikana](media/RM-how-to-21.png)

Tarpeena on 120 tuntia robotiikkasuunnittelua viiden päivän aikana eli 24 tuntia päivässä.

![Päiväkohtainen tarve](media/RM-how-to-22.png)

Tämä on esimerkki siitä, että useita nimettyjä resursseja tarvitaan täyttämään yleinen resurssipyyntö. Sinun on varattava useita resursseja täyttämään tarve.

![Useiden resurssien varaaminen täyttämään tarve](media/RM-how-to-23.png)

Suurin ero tässä skenaariossa on, että yleinen resurssi pysyy ryhmässä tehtävälle kohdistettuna ja että varattuja nimettyjä ryhmän jäseniä ei kohdenneta osana asemaa. Projektipäällikkö voi kohdentaa työn nimetyille resursseille harkintansa mukaan. **Täsmäytys**-näkymä voi auttaa projektipäällikköä jakamaan varaukset tehtäväkohdennuksiksi useille resursseille. Tämä ei tapahdu automaattisesti, koska yllä esitettyä monimutkaisemmissa skenaarioissa, kuten siinä tapauksessa, jossa on joukko tehtäviä, jotka muodostavat tarpeen, järjestelmän on otettava huomioon, miten projektipäällikkö haluaa toteuttaa kohdennukset. Koska järjestelmä ei ymmärrä tarkoitusta, oletukset eroavat todennäköisesti tarkoituksesta, ja tuloksena on virheellinen tai arvaamaton tulos. Ennustettava tulos on se, että yleinen resurssi säilyy määritettynä, kunnes projektipäällikkö luo tietoisesti kohdennuksia **Täsmäytys**-näkymän avulla.


