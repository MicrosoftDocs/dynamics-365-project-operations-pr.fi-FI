---
title: Entiteettien, ohjausobjektien ja käyttöliittymän muutokset (Project Service Automation 3. x)
description: Tässä aiheessa kuvataan ratkaisumuutokset versiossa Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 86b51e58189a62f15a5ded039e9265733a0d9d4a7c7bf8d18ac46aadf1d2a931
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987342"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Entiteettien, ohjausobjektien ja käyttöliittymän muutokset (Project Service Automation 3. x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Version Microsoft Dynamics Project Service Automation (PSA) 3.x julkaisun myötä entiteetteihin, ohjausobjekteihin, näkymiin ja käyttöliittymään on tehty monia muutoksia. Tässä aiheessa annetaan tietoja näistä tärkeistä muutoksista.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Ylä- ja alatason suhteet entiteeteille myyntiasiakirja, myyntiasiakirjan rivi ja myyntiasiakirjan rivin tiedot
Ennen versiota 3.0 julkaistuissa Dynamics 365 Project Service Automationin (PSA:n) versioissa osa myyntiasiakirjojen, myyntiasiakirjojen rivien ja myyntiasiakirjojen rivien tietojen välisistä suhteista toteutettiin merkkijonokentillä, jotka sisälsivät niihin liittyvien entiteettien GUID-tunnuksen merkkijonomuodossa. Tämä johtui ympäristörajoituksista, jotka edellyttivät merkittävää mukautetun koodin määrää ratkaisun palvelin- ja asiakaspuolella, jotta kyseiset suhteet toimisivat samankaltaisesti kuin tyypilliset Dynamics CRM -entiteettien suhteet ja jotta merkkijonokentät toimisivat valintakenttien tavoin.

PSA 3.0 on päivitetty hyödyntämään uusia entiteettisuhteita entiteettien myyntiasiakirja ja myyntiasiakirjan rivi välillä.

Koska valintakenttiä voidaan nyt käyttää ilmaisemaan viittauksia entiteetteihin, GUID-tunnuksen merkkijonoarvon aiemmissa versiossa sisältäneitä kenttiä ei enää tarvita, joten ne ovat vanhentuneet. Myös mukautettu asiakas- ja palvelinpuolen koodi, joka käsitteli vanhojen merkkijonokenttien määrittämiä suhteita on vanhentunut.

### <a name="entity-schema-changes"></a>Entiteettien rakennemuutokset
Seuraavassa taulukossa esitetään yksi yhteen -luettelo entiteettien vanhentuneista merkkijonokentistä ja uusista valintakentistä. 

 Entiteetti |   Vanhentunut kenttä (Merkkijono) | Uusi kenttä (Valinta)
--- | --- | ---
invoicedetail (Laskurivi) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Todellinen arvo) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Projektisopimusrivin laskutusaikataulu) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Projektisopimusrivin välitavoite) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Tieto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Laskurivin tiedot) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Kirjauskansion rivi) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Projektin sopimusrivin resurssiluokka) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Projektin sopimusrivin tiedot) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Projektin sopimusrivin tapahtumaluokka) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Projektin sopimusrivin tapahtumaluokka) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Tarjousrivin laskutusaikataulu) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Tarjousrivin resurssiluokka) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Tarjousrivin välitavoite) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Tarjousrivin tiedot) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Tarjousrivin tapahtumaluokka) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Tarjousrivin tapahtumaluokka) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Tilausrivi) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Vanhentuneet mukautetut näkymät ja ohjausobjektit
Seuraavat mukautetut näkymät ja ohjausobjektit ja niihin liittyvät artefaktit ovat vanhentuneet.

- Veloitettavuus-näkymä.
- Mukautetut ruudukon ohjausobjektit tarjousrivin tietojen näyttämiseen tarjousrivin **Projektitiedot**-sivulla.
- Mukautetut ruudukon ohjausobjektit projektisopimusrivin tietojen näyttämiseen myyntitarjousrivin **Projektitiedot**-sivulla.

> [!NOTE]
> Täydellinen luettelo vanhentuneista resursseista on aiheessa [Vanhentuneet verkkoresurssit Project Service Automationin versiossa 3.x](../developer-guides/web-resources-deprecated-v3.x.md).

## <a name="unified-client-interface-app-module"></a>Unified Client -käyttöliittymän sovellusmoduuli
Unified Client -käyttöliittymän sovellusmoduulien käyttöönoton myötä PSA:n sivustokarttamerkinnät on poistettu järjestelmästä.  
Entiteettien Mahdollisuus, Tarjous, Tilaus ja Lasku lomakkeenvaihtoon liittyvät toiminnot ovat vanhentuneet, koska niitä ei enää tarvita sen ansiosta, että Unified Client -käyttöliittymän sovellusmoduulit sisältävät vain lomakkeiden PSA-versioita.  

Seuraavat verkkoresurssit ovat vanhentuneet:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Täydellinen luettelo vanhentuneista resursseista on aiheessa [Vanhentuneet verkkoresurssit Project Service Automationin versiossa 3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]