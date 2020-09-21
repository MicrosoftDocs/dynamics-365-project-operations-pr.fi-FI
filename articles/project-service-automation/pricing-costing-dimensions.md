---
title: Hinnoittelu- ja kustannusdimensioiden aloitussivu
description: Tämä aihe sisältää yleiskatsauksen hinnoitteludimensioihin.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751156"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Hinnoittelu- ja kustannusdimensioiden aloitussivu

Henkilöresursseissa hinnoittelun ja kustannusten määrittämiseen käytettävät dimensiot jaetaan kahteen luokkaan:

- Henkilöt
- Suunniteltu työ

Tämän vuoksi Project Service Automationissa (PSA:ssa) on käytettävissä kahdenlaisia hinnoitteludimensioarvoja: 

- **Asetusjoukot** – Dimensioita, jotka ovat arvojoukon kiinteitä luettelointeja.
- **Entiteettiperusteiset arvot** – Dimensioita, jotka voivat olla vaihtelevia arvojoukkoja.

## <a name="pricing-dimensions"></a>Hinnoitteludimensiot

PSA sisältää oletusjoukon hinnoitteludimensioita. Niitä voi tarkastella siirtymällä kohtaan **Project Service** > **Parametrit**. Varmista parametritietueen **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että roolin **msdyn_resourcecategory** ja resursoivan organisaatioyksikön **msdyn_organizationalunit** kenttien **Sovelletaan myyntiin** ja **Sovelletaan kustannuksiin** arvona on **Kyllä**. Tällöin voit määrittää jokaisen roolin ja organisaatioyksikön hinnan ja kustannuksen.

![Näyttökuva Project Service -parametreista, joissa Sovelletaan myyntiin on korostettu](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Jos olet käyttänyt valmiita roolin ja organisaatioyksikön kenttiä hinnoitteludimensioina ennen PSA;n versiota 3, muutoksia ei ole havaittavissa. Voit jatkaa Project Servicen käyttöä tavalliseen tapaan. 

Jos sinun on määritettävä resurssiesi hintoja tai kustannuksia lisämääritteitä käyttäen, voit luoda mukautettuja kenttiä, entiteettejä ja dimensioita. Lisätietoja saat seuraavista aiheista, mutta ota huomioon, että sinun on suoritettava toimenpidesarja alla näkyvässä järjestyksessä:

- [Mukautettujen kenttien ja entiteettien luominen](create-custom-fields-entities.md)
- [Mukautettujen kenttien lisääminen hinta- ja tapahtumaentiteetteihin](field-references.md)
- [Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi ](set-up-pricing-dimensions.md)
- [Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Henkilöresurssin ajan hinnoitteleminen
Organisaation tapa hinnoitella henkilöresurssien aika on usein tärkeä strateginen näkökohta, joka vaikuttaa suoraan organisaation kannattavuuteen. Tee yhteistyötä talousryhmän ja ammattialan päälliköiden kanssa, kun organisaatiosi on valmis päättämään, miten se haluaa määrittää henkilöresurssien ajan laskutus- ja kustannushinnat.

Muita hinnoittelussa huomioitavia seikkoja ovat se, käytetäänkö sellaisia kenttiä tai entiteettejä uudelleen, jotka eivät tällä hetkellä ole hinnoitteludimensioita mutta soveltuvat organisaation hinnoitteludimensioiksi. Mahdollisia dimensioita ovat esimerkiksi kentät **Tapahtumaluokka** (**msdyn_transactioncategory**) ja **Varattavissa oleva resurssi** (**bookableresource**). 

On myös päätettävä, pitäisikö hinnoitteludimension olla taulukko vai asetusjoukko. Jos odotettavissa on muutoksia dimension arvioihin, jotka ylittävät 10 tai 12, ja tarvitset lisämääritteitä kyseisille arvoille, voit luoda entiteetin asetusjoukon sijaan. Asetusjoukon ylläpitotoimiin, kuten arvojen lisäämiseen, tarvitaan järjestelmänvalvoja tai kehittäjä, kun taas useimmat käyttäjät pystyvät lisäämään uusia rivejä taulukkoon.

Seuraavassa esimerkissä esitetään laskutushintoja, jotka määritetään roolin ja sen resursoivan organisaatioyksikön perusteella, johon resurssi kuuluu. Kustannushinnat perustuvat yleensä työntekijän ja hänen organisaatioyksikkönsä palkkaluokkiin. Tässä esimerkissä laskutushinnan ja kustannushinnan taulukot näyttävät seuraavalta.

**Esimerkkilaskutushinnat**

| Rooli        | Organisaatioyksikkö    |Yksikkö      |Hinta      |Valuutta  |
| ------------|-------------|----------|----------:|----------|
| Kehittäjä   | Contoso US  |Hour | 200|USD     |
| Kehittäjä   | Contoso India |Hour|   112|USD     |


**Esimerkkikustannushinnat**

| Palkkaluokat     | Organisaatioyksikkö    |Yksikkö      |Hinta      |Valuutta  |
| ----------------|-------------|----------|----------:|----------|
| Oma company_Band1 | Contoso US  |Hour | 145|USD     |
| Oma company_Band2 | Contoso India |Hour|   67|USD     |
