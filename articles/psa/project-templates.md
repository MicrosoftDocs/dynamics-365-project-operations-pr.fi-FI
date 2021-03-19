---
title: Projektimallit
description: Tässä aiheessa on tietoja projektimallien käyttämisestä projektien nopeaan määrittämiseen.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d9d208ebcef127062428afdadde2c54eb07ea505
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283589"
---
# <a name="project-templates"></a>Projektimallit 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektimalli on esimääritetty kehys, jonka avulla voit nopeasti ja helposti käynnistää projektin. Voit luoda uuden projektin yhdellä napsautuksella käyttämällä valmista mallia. Kuten projekteillekin, myös projektimalleille on määritettävä esitiedot. Jokaiselle projektimallille on määritettävä projekti alenteri, ja roolien ja hinnastojen on oltava ennalta määritettyjä organisaatiossa, jotta mallin komponenteilla on hyödyllisiä tietoja.

Projektimalli koostuu kolmesta osasta: aikataulusta, projektiarvioista ja projektiryhmän jäsenistä.

## <a name="schedule"></a>Aikatauluta

Projektimallin aikataulussa on samat elementit kuin projektin aikataulussa. Voit luoda tehtävähierarkian, liittää rooleja tehtäviin, määrittää aikataulu-ominaisuuksia ja luoda riippuvuuksia. Projektimallin aikataulu tukee myös kunkin tehtävän tehtävätiloja. Siksi se tukee aikataulutusmoduulia. Projektikalenteri on liitettävä projektiin. Projektimallilla ja projektilla ei ole eroa työaikataulua luotaessa.

## <a name="project-estimates"></a>Projektin arviot

Projektiarviot projektimallissa toimivat samalla tavalla kuin projektin arviot projektissa. Kustannus- ja myyntihinnat kuitenkin haetaan oletuskustannus- ja myyntihinnastoista, jotka on määritetty parametreissa.

## <a name="creating-a-project-from-a-template"></a>Projektin luominen mallista
 
Projektin voi luoda projektimallista useilla tavoilla:

- Kun luot projektin tarjouksesta voit valita projektimallin **Nopea projektin luonti** -dialogiruudusta.

> ![Pikaluonti: projektin dialogiruutu](media/project-11.png)

- Kun luot projektin valitsemalla **Uusi projekti**, **Projekti**-sivu ilmestyy ennen tietueen tallennusta. Valitse **Valitse malli** -kentässä jokin organisaation esimääritetyistä projektimalleista.
- Käytä **Luo projekti mallista** -toimintoa **Mallikohde**-sivulla.

## <a name="copying-components-of-template-to-project"></a>Projektimallin osien kopioiminen projektiin

Kun kopioit projektimallin osia projektiin, projektin asetuksista riippuen voi tapahtua joitakin ohituksia.

### <a name="copying-the-schedule"></a>Aikataulun kopioiminen

Kopioitaessa aikataulu projektimallista, jos projektilla on eri kalenteri kuin mallilla, työtunteja projektin kalenterista käytetään tehtävän aikatauluun. Näin aikataulu sopeutetaan täsmäämään taustaprojektin kalenteriin. Vastaavasti aikataulun ensimmäinen tehtävä saa projektin aloituspäivämäärän, ja muun hierarkian aikataulua päivitetään perustuen mallissa määritettyyn kestoon ja riippuvuuksiin. 

### <a name="copying-project-estimates"></a>Projektin arvioiden kopiointi 

Kopioitaessa projektiarviorivien välillä hinnastot päivitetään. Kustannushinnastossa nämä päivitykset perustuvat projektin omistavaan yksikköön. Myyntihinnastossa ne perustuvat asiakkaaseen. Projekteille, jotka liittyvät myyntikohteeseen, yksikkökustannus- ja myyntihinnat määritellään näiden hinnastojen perusteella.

### <a name="copying-a-project-team"></a>Projektiryhmän kopioiminen

Kun projektiryhmä kopioidaan projektimallista projektiin, kopioidaan yleiset resurssit, samoin kuin mallissa määritetyt taidot ja osaamisalueet. Yleisten resurssien kohdennukset myös säilytetään sellaisina, kuin ne olivat projektimallissa. Nimettyjä resursseja ei tueta projektimalleissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]