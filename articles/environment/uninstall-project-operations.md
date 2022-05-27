---
title: Dynamics 365 Project Operations -ohjelman poistaminen
description: Tässä aiheessa on tietoja Dynamics 365 Project Operationsin asennuksen poistamisesta.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e2600c770477ad32cebb66f33a8ca31502a6da3d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575852"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Dynamics 365 Project Operations -ohjelman poistaminen 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Jos haluat poistaa Dynamics 365 Project Operations -asennuksen, sinulle on annettava Järjestelmänvalvojan rooli.

1. Siirry kohtaan **Asetukset** > **Ratkaisut**.

    ![Asetukset-sivu.](./media/uninstall-proj-ops-solutions.png)
  
2. Poista ratkaisut seuraavassa taulukossa mainitussa järjestyksessä. 

    | Osavaihe | Ratkaisun nimi                                    | Huomautus                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 2 | ProjectOperations_Anchor                           | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 5 | ProjectService                                     | Ei muuta huomioitavaa.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Ei muuta huomioitavaa.                                                                         |
    | 7 | ProjectServiceCore                                 | Ei muuta huomioitavaa.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 9 | FieldServiceCommon                                 | Vaaditaan kaksoiskirjoitukselle – Dynamics 365 Finance tai Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Vaaditaan kaksoiskirjoitukselle – Dynamics 365 Finance tai Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Vaaditaan Dynamics 365 Field Servicessä.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Vaaditaan Dynamics 365 Field Servicessä.                                                     |
    | 13 | msdyn_TESA                                         | Vaaditaan Dynamics 365 Field Servicessä.                                                     |
    | 14 | ResourceSchedulingControls                         | Vaaditaan Dynamics 365 Field Servicessä.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Vaaditaan Dynamics 365 Field Servicessä.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Vaaditaan Dynamics 365 Field Servicessä.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Vaaditaan Dynamics 365 Field Servicessä.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 19 | Dynamics365Notes                                   | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 21 | DualWriteCore                                      | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 23 | Dynamics365AssetManagement                         | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 26 | HCMCommon                                          | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 28 | Osapuoli                                              | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 29 | Dynamics365Company                                 | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 30 | CurrencyExchangeRates                              | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
    | 31 | AssetCommon                                        | Jos ratkaisua ei löydy, ohita tämä ratkaisu.                                                            |
