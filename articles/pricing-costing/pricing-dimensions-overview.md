---
title: Hinnoitteludimensioiden yleiskatsaus
description: Tässä aiheessa on tietoja hinnoitteludimensioista Dynamics 365 Project Operationsissa.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650183"
---
# <a name="pricing-dimensions-overview"></a>Hinnoitteludimensioiden yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Henkilöresursseissa hinnoittelun ja kustannusten määrittämiseen käytettävät dimensiot jaetaan kahteen luokkaan:

- Henkilöt
- Suunniteltu työ

Tämän vuoksi käytettävissä on seuraavat kaksi hinnoitteludimensioarvoa:

- **Asetusjoukot**: Dimensioita, jotka ovat arvojoukon kiinteitä luettelointeja.
- **Entiteettiperusteiset arvot**: Dimensioita, jotka voivat olla vaihtelevia arvojoukkoja.

## <a name="pricing-dimensions"></a>Hinnoitteludimensiot

Dynamics 365 Project Operationsin kanssa toimitetaan hinnoitteludimensioiden oletusjoukko. Hinnoitteludimensioita voi tarkastella siirtymällä kohtaan **Project Operations** > **Parametrit**. Varmista parametritietueen **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että roolin **msdyn_resourcecategory** ja resursoivan organisaatioyksikön **msdyn_organizationalunit** kenttien **Sovelletaan myyntiin** ja **Sovelletaan kustannuksiin** arvona on **Kyllä**. Näiden käytössä olevien kenttien avulla voit määrittää jokaisen roolin ja organisaatioyksikön hinnan ja kustannuksen.

![Näyttökuva Project Service -parametreista, joissa Sovelletaan myyntiin on korostettu](media/PS-OOB-parameters.png)

Jos sinun on määritettävä resurssiesi hintoja tai kustannuksia lisämääritteitä käyttäen, voit luoda mukautettuja kenttiä, entiteettejä ja dimensioita. Lisätietoja on seuraavissa aiheissa. 
  
  > [!NOTE]
  > Toimintosarjat on suoritettava siinä järjestyksessä, jossa ne on lueteltu.

1. [Ratkaisun luominen mukautetuille hinnoitteludimensioille](../sales/create-solution-custompd.md)
2. [Mukautettujen kenttien ja entiteettien luominen](create-custom-fields-entities-pricing-dimensions.md)
3. [Mukautettujen kenttien lisääminen hintamääritys- ja tapahtumaentiteetteihin ](add-custom-fields-price-setup-transactional-entities.md)
4. [Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi ](set-up-custom-fields-pricing-dimensions.md)
5. [Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Henkilöresurssin ajan hinnoitteleminen
Organisaation tapa hinnoitella henkilöresurssien aika on usein tärkeä strateginen näkökohta, joka vaikuttaa suoraan organisaation kannattavuuteen. Tee yhteistyötä talousryhmän ja ammattialan päälliköiden kanssa, kun organisaatiosi on valmis päättämään, miten se haluaa määrittää henkilöresurssien ajan laskutus- ja kustannushinnat.

Muita hinnoittelussa huomioitavia seikkoja ovat se, käytetäänkö sellaisia kenttiä tai entiteettejä uudelleen, jotka eivät tällä hetkellä ole hinnoitteludimensioita mutta soveltuvat organisaation hinnoitteludimensioiksi. Mahdollisia dimensioita ovat esimerkiksi kentät **Tapahtumaluokka** (**msdyn_transactioncategory**) ja **Varattavissa oleva resurssi** (**bookableresource**). 

Mieti, pitäisikö hinnoitteludimension olla taulukko vai asetusjoukko. Jos odotettavissa on muutoksia dimension arvioihin, jotka ylittävät 10 tai 12, ja tarvitset lisämääritteitä kyseisille arvoille, voit luoda entiteetin asetusjoukon sijaan. Asetusjoukon ylläpitotoimiin, kuten arvojen lisäämiseen, tarvitaan järjestelmänvalvoja tai kehittäjä, kun taas useimmat käyttäjät pystyvät lisäämään uusia rivejä taulukkoon.

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
