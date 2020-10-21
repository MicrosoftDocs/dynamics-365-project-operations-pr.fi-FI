---
title: Käyttöönottotyypit
description: Tässä aiheessa on tietoja Project Operationsin oikean käyttöönottotyypin valinnasta omalle yrityksellesi.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948838"
---
# <a name="deployment-types"></a>Käyttöönottotyypit

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

> [!IMPORTANT]
> Kun olet ostanut käyttöoikeuden, voit määrittää Dynamics 365 Project Operationsin parhaan asennusmallin [ohjatun asennusvuon avulla](https://aka.ms/provisionprojectoperations).
> Kun olet tehnyt ohjatun asennusvuon, sinut ohjataan oikeaan hallintaportaaliin, jotta asennus viimeistellään. Asennuksen viimeistelemisen tiedot ovat alla.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Olemassa olevat Dynamics-asiakkaat, jotka käyttvät Dynamics 365 Project Service Automationia
Project Operations sisältää Project Service Automationin mukana toimitetut toiminnot. Näille asiakkaille julkaistaan tulevaisuudessa päivityspolku.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Olemassa olevat Dynamics 365 Finance-asiakkaat, jotka käyttävät Projektinhallinta ja kirjanpito -moduulia 

Finance-asiakkaat, jotka käyttävät Projektinhallinta- ja kirjanpito -toimintoa, voivat jatkaa käyttöä sellaisenaan. Katso [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma).

Project Operations tukee useita eri toteutusvaihtoehtoja tarpeidesi mukaan. Olitpa uusi tai nykyinen Dynamics 365 -asiakas, Project Operations voit tukea tarpeitasi.

[Käyttöönottokyselyn](https://aka.ms/provisionprojectoperations) avulla voit määrittää oikean käyttöönottotavan. Tulokset opastavat sinua kohti jotakin seuraavista käyttöönottotyypeistä:

- [Lite-käyttöönotto – kauppa proformalaskutukseen](#lite)
- [Project Operations resurssien ja ei-varastoitavien skenaarioissa](#integrated)
- [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma)

Project Operations tukee varastoitu/tuotantotilaus-skenaarioita ja ei-varastoitavia/resurssipohjaisia skenaarioita samassa ympäristössä yritystason määritysten avulla. Esimerkiksi Contoso voi hyödyntää Yhdysvaltain tuotantolaitoksessa (oikeushenkilö = Contoso Manufacturing United States) ja varastoitavien/tuotannon ominaisuuksia, ja ei-varastoitavien/resurssipohjaisten ominaisuuksia Yhdistyneiden kuningaskuntien Contoso Robotics Arms -palvelulaitoksessa (oikeushenkilö = Contoso Robotics United Kingdom).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Lite-käyttöönotto – kauppa proformalaskutukseen
Lite-käyttöönotossa on seuraavat ominaisuudet:

- Projektin suunnittelu Microsoft Project -verkkoversion avulla
- Moniulotteinen hinnoittelu
- Yhdistetty resurssien hallinta
- Aikaseuranta
- Peruskulu
- Laskuehdotus

### <a name="deployment-steps"></a>Käyttöönotto-ohjeet:
Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).

Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](lite-preview-subscription-sign-up.md) ja [Uuden ympäristön valmistelu](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations resurssien ja ei-varastoitavien skenaarioissa
Project Operations tarjoaa resurssien/ei-varastoitavien skenaarioille seuraavat ominaisuudet:
  
- Projektin suunnittelu Microsoft Project -verkkoversion avulla
- Moniulotteinen hinnoittelu
- Yhdistetty resurssien hallinta
- Aikaseuranta
- Peruskulu
- Koko kulu
- Kuittien OCR
- Täysi laskutus
- Tuoton kirjaaminen

### <a name="deployment-steps"></a>Käyttöönotto-ohjeet:
Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).

Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](resource-sign-up-preview-subscription.md) ja [Uuden ympäristön valmistelu](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations varastoitavien/tuotantotilausten skenaarioissa

- Projektin suunnittelu työrakenteen avulla
- Resurssienhallinta
- Aikaseuranta
- Koko kulu
- Kuittien OCR
- Täysi laskutus
- Tuoton kirjaaminen
- Tuotantotilaukset
- Materiaalien tuki

### <a name="deployment-steps"></a>Käyttöönotto-ohjeet:
Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).

Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uuden ympäristön valmistelu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



