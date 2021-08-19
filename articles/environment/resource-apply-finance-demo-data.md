---
title: Esittelytietojen käyttäminen Finance-pilvipalveluympäristössä
description: Tässä aiheessa kerrotaan, miten Project Operations -esittelytietoja käytetään pilvipalvelussa isännöidyssä Dynamics 365 Finance -ympäristössä.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c04aab6ffb332a3095ca2a7890deb73f15a8b5e3713021c60eec02eb13dbd0cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009662"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Esittelytietojen käyttäminen Finance-pilvipalveluympäristössä

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

> [!IMPORTANT]
> Tämä aihe koskee vain Microsoft Dynamics 365 Finance -versiota 10.0.13, ja se voidaan suorittaa vain pilvipohjaisessa ympäristössä. Suorita tämän aiheen vaiheet, **ENNEN** kuin otat käyttöön ympäristön laatupäivitykset.

1. Avaa LCS-projektissa **Ympäristön tiedot** -sivu. Huomaa, että se sisältää tiedot, joita tarvitaan yhteyden muodostamiseen ympäristöön etätyöpöytäprotokollan (RDP) avulla.

![Ympäristön tiedot.](./media/1EnvironmentDetails.png)

Ensimmäiset korostetut tunniste tiedot ovat paikallisten tilien tunnistetietoja, ja niissä on hyperlinkki etätyöpöytäyhteyteen. Tunnistetiedoissa on ympäristön järjestelmänvalvojan käyttäjänimi ja salasana. Toisen tunnistetietojoukon avulla voit kirjautua SQL Serveriin tässä ympäristössä.

2. Voit muodostaa yhteyden ympäristöön **Paikalliset tilit** -kohdan hyperlinkin avulla ja todentautua käyttäen **paikallisen tilin tunnistetietoja**.
3. Siirry kohtaan **Internet Information Services** > **Sovellusryhmät** > **AOSService** ja pysäytä palvelu. Palvelu pysäytetään tässä vaiheessa, jotta voit jatkaa SQL-tietokannan korvaamista.

![Pysäytä AOS-palvelu.](./media/2StopAOS.png)

4. Siirry kohtaan **Palvelut** ja pysäytä seuraavat kaksi kohdetta:

- Microsoft Dynamics 365 Unified Operations: Batch Management Service
- Microsoft Dynamics 365 Unified Operations: Data Import Export Framework

![Pysäytä palvelut.](./media/3StopServices.png)

5. Avaa Microsoft SQL Server Management Studio. Kirjaudu sisään SQL Server -tunnistetiedoilla ja käytä axdbadmin-käyttäjää ja salasanaa LCS:n **Ympäristöjen tiedot** -sivulla.

![SQL Server Management Studio.](./media/4SSMS.png)

6. Valitse Object Explorerissa **Tietokannat** ja etsi **AXDB**. Korvaat tietokannan uudella tietokannalla, joka sijaitsee [Download Centerissä](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopioi zip-tiedosto yhdistettyyn virtuaalikoneeseen ja pura zip-tiedoston sisältö.
8. Napsauta SQL Server Management Studiossa hiiren kakkospainikkeella **AxDB** ja valitse sitten **Tehtävät** > **Palauta** > **Tietokanta**.

![Tietokannan palauttaminen.](./media/5RestoreDatabase.png)

9. Valitse **Lähdelaite** ja siirry kopioimastasi zip-tiedostosta purkamaasi tiedostoon.

![Lähdelaitteet.](./media/6SourceDevice.png)

10. Valitse **Asetukset** ja valitse sitten **Korvaa aiemmin luotu tietokanta** ja **Sulje aiemmin luodut yhteydet kohdetietokantaan**. 
11. Valitse **OK**.

![Asetusten palauttaminen.](./media/7RestoreSetting.png)

Näyttöön tulee vahvistus siitä, että AXDB-palautus onnistui. Kun olet saanut tämän vahvistuksen, voit sulkea SQL Services Management Studion.

12. Siirry takaisn kohtaan **Internet Information Services** > **Sovellusryhmät** > **AOSService** ja käynnistä AOSService.
13. Siirry kohtaan **Palvelut** ja käynnistä kaksi aiemmin pysäytettyä palvelua.

14. Etsi tässä virtuaalikoneessa AdminUserProvisioning-työkalu. Katso K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Suorita .exe-tiedosto **Sähköpostiosoite**-kentässä olevan käyttäjäosoitteen avulla. 
16. Valitse **Lähetä**.

![Järjestelmänvalvojakäyttäjän valmistelu.](./media/8AdminUserProvisioning.png)

Tämä kestää muutaman minuutin. Saat vahvistusviestin, jonka mukaan järjestelmänvalvojakäyttäjän päivitys onnistui.

17. Suorita lopuksi komentokehote järjestelmänvalvojana ja suorita iisreset-komento

![IIS-palautus.](./media/9IISReset.png)

18. Sulje etätyöpöytäistunto ja kirjaudu ympäristöön LCS:n **Ympäristön tiedot** -sivulla, jotta voit varmistaa, että se toimii odotetulla tavalla.

![Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]