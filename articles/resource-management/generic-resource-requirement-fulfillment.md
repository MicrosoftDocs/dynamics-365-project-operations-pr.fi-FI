---
title: Yleisten resurssitarpeiden täyttäminen
description: Tässä aiheessa on tietoja siitä, miten nimettyjä resursseja varataan yleistä resurssitarvetta varten.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130303"
---
# <a name="generic-resource-requirement-fulfillment"></a>Yleisten resurssitarpeiden täyttäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Voit varata nimetyn resurssin korvaamaan yleisen resurssin, jolla on resurssitarve.

1. Valitse **Projektit**-sivulla **Ryhmä**-välilehti.
2. Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Varaa**. Voit myös avata resurssitarpeen ja valita **Varaa**-kohdan.
3. Valitse **Ajoitusavustaja**-sivulla projektiryhmääsi varattava nimetty resurssi ja valitse **Varaa**.

Kun varaus on valmis ja nimetty resurssi on täyttänyt sen, yleinen resurssi korvataan nimetyllä resurssilla.

Myös aikataulun kohdennukset päivitetään nimetyllä resurssilla.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Yleisen resurssin täyttäminen useilla nimetyillä resursseilla
Yleisen resurssin tarpeen täyttäminen useilla nimetyillä resursseilla vastaa yksittäisen nimetyn resurssin kohdentamista. Otetaan esimerkiksi viisi päivää ja 120 tuntia työtä vaativa tehtävä. Yksittäinen yleensä kahdeksantuntista työpäivää viiden päivän työviikoilla tekevä resurssi ei voi suorittaa tätä tehtävää. 

Tarpeena on 120 tuntia robotiikkasuunnittelua viiden päivän aikana eli 24 tuntia päivässä.

Tämä on esimerkki siitä, että useita nimettyjä resursseja tarvitaan täyttämään yleinen resurssipyyntö. Sinun on varattava useita resursseja täyttämään tarve.

Suurin ero tässä skenaariossa on, että yleinen resurssi pysyy ryhmässä tehtävälle kohdistettuna ja että varattuja nimettyjä ryhmän jäseniä ei kohdenneta osana asemaa. Projektipäällikkö voi kohdentaa työn nimetyille resursseille harkintansa mukaan. **Täsmäytys**-näkymä voi auttaa projektipäällikköä jakamaan varaukset tehtäväkohdennuksiksi useille resursseille. Tämä ei tapahdu automaattisesti, koska yllä esitettyä monimutkaisemmissa skenaarioissa, kuten siinä tapauksessa, jossa on joukko tehtäviä, jotka muodostavat tarpeen, järjestelmän on otettava huomioon, miten projektipäällikkö haluaa toteuttaa kohdennukset. Koska järjestelmä ei ymmärrä tarkoitusta, oletukset ovat todennäköisesti erilaisia kuin tarkoitus, ja tuloksena syntyy virheellinen tai arvaamaton tulos. Ennustettava tulos on se, että yleinen resurssi säilyy määritettynä, kunnes projektipäällikkö luo tietoisesti kohdennuksia **Täsmäytys**-näkymän avulla.




[!INCLUDE[footer-include](../includes/footer-banner.md)]