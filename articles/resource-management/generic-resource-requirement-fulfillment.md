---
title: Yleisten resurssitarpeiden täyttäminen
description: Tässä aiheessa on tietoja siitä, miten nimettyjä resursseja varataan yleistä resurssitarvetta varten.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e36875a0d5dcb24d9669e2ea989c6fc7db7bcd7c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005832"
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