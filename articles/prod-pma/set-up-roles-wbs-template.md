---
title: Roolien määrittäminen työrakennemalleihin
description: Tässä aiheessa on tietoja roolitietojen määrittämisestä työn erittelyrakenteiden malleissa.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997597"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Roolien määrittäminen työrakennemalleihin

[!include [banner](../includes/banner.md)]

Projektipäälliköt voivat määrittää työrakeennemalleja (WBS), joita he voivat käyttää luodessaan työrakenteita uusille projekteille. Projektipäälliköt voivat lisätä rooleja luodessaan mallin. Käytä seuraavaa menettelyä osoittaaksesi roolin työrakennemallille.

1. Valitse **Projektinhallinta ja kirjanpito** > **Määritys** > **Projektit** > **Työrakennemallit**.
2. Valitse **Tiedot** valittua työrakennemallia varten.
3. Valitse tehtävä luettelosta ja valitse sitten **Rooli**-kentässä rooli, jolle tehtävä osoitetaan.

## <a name="work-with-a-wbs"></a>Työrakenteen kanssa työskentely

Voit luoda uuden työrakenteen tai voit kopioida työrakenteen olemassa olevasta työrakennemallista. Projektipäällikkö voi helposti hallita resursseja määrittämällä rooleja työrakenteen uusille tehtäville. Roolit voidaan korvata joko sen jälkeen, kun resurssi on hankittu tai kun tehtävän suorittamiseen on tunnistettu vahvistettu resurssi. Tämän joustavuuden ansiosta projektipäälliköt voivat suorittaa seuraavat tehtävät:

- Työrakennetyöpakettien edellyttämien resurssien määrän tunnistaminen.
- Projektin kustannusten arviointi.
- Alustavan budjetin määrittäminen.
- Aktiviteetin kestoin arvioiminen roolien ja resurssien perusteella.
- Projektinhallintasuunnitelmien kehittäminen käytettävissä olevien projektitietojen perusteella.

Työrakenteeseen on lisätty lisäasetuksia, jotta resursointitoimintoa voidaan hyödyntää paremmin.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Asetus</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resurssimääritykset</td>
<td>Tarkastella työrakenteen tehtävien osoitettuja resursseja, päivämääriä, tuntimääriä ja varaustyyppejä.</td>
</tr>
<tr class="even">
<td>Tiimin automaattinen luonti</td>
<td>Lisää suunniteltuja resursseja automaattisesti käyttämällä rooleja, jotka on osoitettu tehtävälle. Finance ehdottaa automaattisesti suunniteltuja resursseja käyttämällä rooleihin perustuvaa moniperusteista päätösanalyysia. Kun roolit ja työmäärä (tuntia) on määritetty työrakenteen tehtäville ja kun rakenne on julkaistu, valitse <strong>Luo tiimi automaattisesti</strong>. Tarvittava suunniteltujen resurssien määrä lisätään työrakenteeseen ja <strong>Projektin ja tiimin aikataulutus</strong> -välilehteen.</td>
</tr>
<tr class="odd">
<td>Resurssi (avautuva luettelo)</td>
<td><strong>Käynnistä resurssimääritys</strong> -sivulla voit valita sitovasti tai alustavasti varattavia resursseja määritetyn keston perusteella. Voit muokata näkymäasetuksia nähdäksesi ja voidaksesi määrittää resurssiaktiviteettien kestoja. Voit valita ja osoittaa resursseja työpakettien tasolla käyttämällä seuraavia asetuksia:
<ul>
<li><strong>Hyväksy</strong> – Vahvista muutokset tehtävälle osoitettuun resurssiin.</li>
<li><strong>Peruuta</strong> – Peruuta muutokset tehtävälle osoitettuun resurssiin.</li>
<li><strong>Osoita automaattisesti</strong> – Käytettävissä oleva henkilöresurssi, jolla on vastaava rooli, valitaan ja osoitettaan valitulle tehtävälle automaattisesti.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projekti.
2. Valitse **Suunnittele** > **Aktiviteetit** > **Työrakenne**.
3. Lisää seuraavat tason yksi aktiviteetit työrakenteeseen valitsemalla **Uusi**:

    - Aloitus
    - Suunnittelu
    - Suoritetaan
    - Seuranta ja valvonta
    - Sulje

4. Määritä päivämäärät ja työmäärä (tuntia) seuraavassa kuvassa näkyvällä tavalla.

    [![Päivämäärien ja työmäärän määrittäminen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Valitse **Aloitus**-tehtävärivi ja sitten **Rooli**-kentässä **Projektipäällikkö**.
6. Valitse **Julkaise**.
7. Valitse saman rivin **Resurssi**-kentässä **Taneli Kultaranta** ja valitse sitten **Hyväksy**.
8. Valitse **Suunnittelu**-tehtävärivi ja valitse sitten **Rooli**-kentässä **Liiketoiminta-analyytikko**.
9. Valitse **Julkaise** ja sitten **Luo tiimi automaattisesti**.
10. Valitse avautuvassa viestiruudussa **Kyllä**.
11. Tarkista, että **Resurssi**-kentän arvo on **Liiketoiminta-analyytikko 1**.
12. Avaa **Liiketoiminta-analyytikko 1** -resurssin haku ja valitse **Käynnistä resurssimääritykset**. Valitse sitten tehtävälle työntekijä.
13. Valitse **Osoita alustavasti** &gt; **Koko kapasiteetti**.

    > [!NOTE] 
    > Et saa varoitusta siitä, että määritetty resurssi on nyt 2, koska resurssien määränä säilyy 1.

14. Vahvista työrakenteen resurssimääritys **Työrakenne**-sivulla ja valitse sitten **Tallenna**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]