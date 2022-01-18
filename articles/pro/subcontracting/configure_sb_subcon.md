---
title: Määritä aikataulutaulukko näyttämään sopimustyöntekijät ja alihankittu kapasiteetti
description: Tässä aiheessa kuvataan, miten aikataulutaulukko määritetään Microsoft Dynamics 365 Project Operationsissa näyttämään sopimustyöntekijät ja alihankittu kapasiteetti.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902851"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Määritä aikataulutaulukko näyttämään sopimustyöntekijät ja alihankittu kapasiteetti 

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Aikataulutaulukkoa voi käyttää Microsoft Dynamics 365 Project Operationsissa resurssien hakemiseen kahdella tavalla.

- Yleinen resurssihaku ilman projektikohtaista resurssitarvetta.
- Tarvekohtainen resurssihaku, jossa projektitarve antaa kontekstin ehdotetuille resursseille.

Jos haluat ilmoittaa aikataulutaulukolle alihankitusta resurssikapasiteetista ja sopimustyöntekijöistä, sinun on päivitettävä aikataulutaulukon asetuksia. Tällaisia päivityksiä ovat esimerkiksi seuraavat: 
- Aikataulutaulukoiden asetusten päivittäminen yleistä resurssihakua varten.
- Aikataulutaulukoiden asetusten päivittäminen tarvepohjaista resurssihakua varten.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Aikataulutaulukoiden asetusten päivittäminen yleistä resurssihakua varten
### <a name="update-filters-for-general-resource-search"></a>Yleisen resurssihaun suodattimien päivittäminen
Kun haet resurssia, aikataulutaulukossa käytössä olevat suodattimet tulee päivittää niin, että voit hakea myös ulkoisia resursseja määrittämällä yhden tai kaikki seuraavista:
  - Työntekijätyyppi, näytetäänkö sopimustyöntekijät vai työntekijät.
  - Toimittajayritys, johon resurssi kuuluu.
  - Tiettyyn alihankintaan tai alihankintariviin kuuluvat resurssit.
    
### <a name="update-retrieve-resource-query"></a>Resurssin noutokyselyn päivittäminen
Myös hakuun käytettävä kysely on päivitettävä käyttämään näitä lisäsuodatinmääritteitä. Toimi seuraavasti päivittääksesi aikataulutaulukon määrityksen yleistä resurssihakua varten:  
1. Avaa kyseisen aikataulutaulukon **Aikataulutaulukon asetukset**.
2. Avaa **Yleiset asetukset** -välilehti ja vieritä kohtaan **Muut asetukset**.
3. Päivitä tämän osan asetusluettelossa kohta **Suodattimien asettelu** muotoon **Project Operations Liten suodattimien oletusasettelu**.
4. Päivitä kohta **Resurssin noutokysely** Muotoon **Project Operations Liten resurssin oletusnoutokysely**.

![Aikataulutaulukoiden asetusten päivittäminen yleistä resurssihakua varten](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Aikataulutaulukoiden asetusten päivittäminen tarvepohjaista resurssihakua varten
### <a name="update-filters-for-requirement-specific-resource-search"></a>Tarvekohtaisen resurssihaun suodattimien päivittäminen 
Kun haet resurssia, aikataulutaulukossa käytössä olevat suodattimet tulee päivittää niin, että voit hakea myös ulkoisia resursseja määrittämällä yhden tai kaikki seuraavista:
 - Työntekijätyyppi, näytetäänkö sopimustyöntekijät vai työntekijät.
 - Toimittajayritys, johon resurssi kuuluu.
 - Tiettyyn alihankintaan tai alihankintariviin kuuluvat resurssit.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Resurssin noutokyselyn päivittäminen tarvekohtaista resurssihakua varten 
Myös hakuun käytettävä kysely on päivitettävä käyttämään näitä lisäsuodatinmääritteitä. Toimi seuraavasti päivittääksesi aikataulutaulukon määrityksen tarvepohjaista resurssihakua varten:

1. Avaa tietyn aikataulutaulukon **Aikataulutaulukon asetukset** ja valitse sitten **Avaa oletusasetukset** avataksesi tarvekohtaisen haun asetukset.
2. Avaa **Yleiset asetukset** -välilehti ja vieritä kohtaan **Muut asetukset**.
3. Päivitä tämän osan asetusluettelossa kohta **Suodattimien asettelu** muotoon **Project Operations Liten suodattimien oletusasettelu**.
4. Päivitä kohta **Resurssin noutokysely** Muotoon **Project Operations Liten resurssin oletusnoutokysely**.
5. Avaa **Aikataulutyypit**-välilehti ja siirry kohtaan **Projekti**.
6. Päivitä **Projektin** asetuksissa **Ajoitusavustajan resurssien noutokysely** muotoon **Project Operations Liten resurssin oletusnoutokysely** ja päivitä **Ajoitusavustajan rajoitteiden noutokysely** muotoon **Project Operations Liten rajoitteiden oletusnoutokysely**.

![Aikataulutaulukoiden asetusten päivittäminen tarvepohjaista resurssihakua varten](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
