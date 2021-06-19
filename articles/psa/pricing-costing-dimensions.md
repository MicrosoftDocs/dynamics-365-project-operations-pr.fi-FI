---
title: Hinnoittelu- ja kustannusdimensioiden aloitussivu
description: Tämä aihe sisältää yleiskatsauksen hinnoitteludimensioihin.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009252"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Hinnoittelu- ja kustannusdimensioiden aloitussivu

[!include [banner](../includes/psa-now-project-operations.md)]

Seuraavat määritteet vaikuttavat dimensioihin, joita käytetään työn hinnoittelun ja kustannuslaskennan määritykseen projektipohjaisissa organisaatioissa:

- Käyttäjät, jotka tekevät töitä kokemuksensa, roolinsa tai maantieteellisen sijaintinsa mukaan
- Työ, joka on suoritettava samalla tavalla monimutkaisuuden tai vuorokauden ajan suhteen

Kun otetaan huomioon näiden töiden ja työn suorittamiseen tarvittavien henkilöiden tyypilliset määritteet, Project Service Automationissa on kahdentyyppisiä hinnoitteludimensioarvoja: 

- **Asetusjoukot** – Määritteet, jotka ovat arvojoukon kiinteitä luettelointeja.
- **Entiteettipohjaiset arvot** – Määritteet, joilla voi olla vaihteleva joukko arvoja, jotka ovat rajallisia mutta voivat muuttua ajan myötä.

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

Mieti, pitäisikö hinnoitteludimension olla taulukko vai asetusjoukko. Jos odotettavissa on muutoksia dimension arvoihin, jotka ylittävät 10 tai 12, ja tarvitset lisämääritteitä kyseisille arvoille, luo entiteetti asetusjoukon sijaan. Asetusjoukon ylläpitotoimiin, kuten arvojen lisäämiseen, tarvitaan järjestelmänvalvoja tai kehittäjä, kun taas useimmat yrityskäyttäjät pystyvät lisäämään uusia rivejä taulukkoon.

Seuraavassa esimerkissä esitetään laskutushintoja, jotka määritetään roolin ja sen resursoivan organisaatioyksikön perusteella, johon resurssi kuuluu. Kustannushinnat perustuvat yleensä työntekijän ja hänen organisaatioyksikkönsä palkkaluokkiin. Tässä esimerkissä laskutushinnan ja kustannushinnan taulukot näyttävät seuraavalta.

**Esimerkkilaskutushinnat**

| Rooli        | Organisaatioyksikkö    |Yksikkö      |Hinta      |Valuutta  |
| ------------|-------------|----------|----------:|----------|
| Kehittäjä   | Contoso US  |tunti | 200|USD     |
| Kehittäjä   | Contoso India |tunti|   112|USD     |


**Esimerkkikustannushinnat**

| Palkkaluokat     | Organisaatioyksikkö    |Yksikkö      |Hinta      |Valuutta  |
| ----------------|-------------|----------|----------:|----------|
| Oma company_Band1 | Contoso US  |tunti | 145|USD     |
| Oma company_Band2 | Contoso India |tunti|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]