---
title: Käyttöönottotyypin määritys
description: Tässä aiheessa on tietoja Project Operationsin oikean käyttöönottotyypin valinnasta omalle yrityksellesi.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997102"
---
# <a name="determine-your-deployment-type"></a>Käyttöönottotyypin määritys

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

> [!IMPORTANT]
> Kun olet ostanut lisenssin, aloita tästä ja selvitä Dynamics 365 Project Operations -palvelun paras käyttöönottomalli käyttämällä  [ohjattua asennustyökulkua](https://aka.ms/provisionprojectoperations).
> Kun olet tehnyt ohjatun asennusvuon, sinut ohjataan oikeaan hallintaportaaliin, jotta asennus viimeistellään. Katso asennuksen viimeistelemisen tiedot.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Olemassa olevat Dynamics-asiakkaat, jotka käyttvät Dynamics 365 Project Service Automationia
Project Operations sisältää Project Service Automationin mukana toimitetut toiminnot. Näille asiakkaille julkaistaan päivityspolku vuoden 2021 1. julkaisuaallossa.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Olemassa olevat Dynamics 365 Finance-asiakkaat, jotka käyttävät Projektinhallinta ja kirjanpito -moduulia 

Nykyiset projektin hallinta- ja kirjanpitotoimintoja käyttävät Finance-asiakkaat voivat jatkoa käyttöä entiseen tapaan. Katso [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma).


## <a name="deployment-regions"></a>Käyttöönottoalueet
Lisätietoja Project Operationsin käyttöönottoa tukevien alueiden määrittämisestä on kohdassa [Dynamics 365:n ja Power Platformin maantieteellinen saatavuusraportti](https://dynamics.microsoft.com/en-us/geographic-availability/). Jos haluat nähdä tuetut alueet, valitse **Näytä raportti** ja laajenna **Dynamics 365 > Operation Apps > Dynamics 365 Project Operations**.

## <a name="deployment-types"></a>Käyttöönottotyypit
Project Operations tukee useita eri toteutusvaihtoehtoja tarpeidesi mukaan. Olitpa uusi tai nykyinen Dynamics 365 -asiakas, Project Operations voit tukea tarpeitasi.

[Käyttöönottokyselyn](https://aka.ms/provisionprojectoperations) avulla voit määrittää oikean käyttöönottotavan. Tulokset opastavat sinua kohti jotakin seuraavista käyttöönottotyypeistä:

- [Lite-käyttöönotto – kauppa proformalaskutukseen](#lite)
- [Project Operations resurssien ja ei-varastoitavien skenaarioissa](#integrated)
- [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma)

Project Operations tukee varastoitu/tuotantotilaus-skenaarioita ja ei-varastoitavia/resurssipohjaisia skenaarioita samassa ympäristössä yritystason määritysten avulla. Esimerkiksi Contoso voi käyttää varastossa olevaa/tuotantotilaus-ominaisuuksia Yhdysvaltain tuotantolaitoksellaan (Yritys = Contoso Manufacturing United States). Contoso voi käyttää ei-varastoituita tai resurssipohjaisia ominaisuuksia Contoso Robotics Arms -huoltolaitoksellaan Yhdistyneessä kuningaskunnassa (Yritys = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lite-käyttöönotto – kauppa proformalaskutukseen

Lite-käyttöönotossa on seuraavat ominaisuudet:

- Dynamics 365 Sales -sovelluksen kokemuksia laajentava projektien myyntiprosessi
- Projektin suunnittelu Microsoft Project -verkkoversion avulla
- Moniulotteinen hinnoittelu
- Yhdistetty resurssien hallinta
- Aikaseuranta
- Peruskulu
- Projektipäällikön tarkistusten ja muokkausten proformalaskutus 

#### <a name="deployment-steps"></a>Käyttöönotto-ohjeet
Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).

Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](lite-preview-subscription-sign-up.md) ja [Uuden ympäristön valmistelu](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations resurssien ja ei-varastoitavien skenaarioissa
Project Operations tarjoaa resurssien/ei-varastoitavien skenaarioille seuraavat ominaisuudet:
 
- Dynamics 365 Sales -sovellusta laajentava projektien myyntiprosessi
- Projektin suunnittelu Microsoft Project -verkkoversion avulla
- Moniulotteinen hinnoittelu
- Yhdistetty resurssien hallinta
- Aikaseuranta
- Peruskulu
- Koko kulu
- Kuittien OCR
- Proformalaskutus ja asiakkaille suunnattu laskutus 
- Projektien tuloutus

#### <a name="deployment-steps"></a>Käyttöönotto-ohjeet
Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).

Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](resource-sign-up-preview-subscription.md) ja [Uuden ympäristön valmistelu](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations varastoitavien/tuotantotilausten skenaarioissa

- Projektin suunnittelu työrakenteen avulla
- Resurssien hallinta
- Aikaseuranta
- Koko kulu
- Kuittien OCR
- Täysi laskutus
- Tuoton tunnistus
- Tuotantotilaukset
- Varastomateriaalien tuki varastojen avulla

#### <a name="deployment-steps"></a>Käyttöönotto-ohjeet
Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).

Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) ja [Uuden ympäristön valmistelu](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]