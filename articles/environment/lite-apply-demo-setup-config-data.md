---
title: Esittelyn asennus- ja määritystietojen käyttäminen – lite
description: Tässä artikkelissa on tietoja esittelyn asennus- ja määritystietojen käyttöönotosta Project Operationsissa.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811021"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operationsin esittelyn asennus- ja määritystietojen käyttäminen – lite 

_**Lite-käyttöönotto – kauppa proformalaskutukseen_



## <a name="prerequisites"></a>edellytykset

Ennen määrityksen aloittamista, Dataverse-ympäristön on oltava valmisteltuna Dynamics 365 Project Operationsia varten.


## <a name="instructions"></a>Ohjeet

1. Lataa [Määrityksen tietopaketti](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Siirry kansioon *ProjOpsSampleSetupData - CE only CMT* ja suorita suoritettava tiedosto *DataMigrationUtility*.
1. Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.

    ![Määrityksen siirto.](./media/1ConfigurationMigration.png)

1. Valitse ohjatun CMT-toiminnon sivulla 2 **Microsoft 365** **asennustyypiksi**.
1. Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.
1. Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.

   ![Kirjautuminen määritykseen.](./media/2ConfigurationSignin.png)

1. Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.
1. Valitse sivulla 4 zip-tiedosto *SampleSetupAndConfigData* pakkaamattomasta kansiosta *ProjOpsSampleSetupData - CE only CMT*.

   ![Zip-tiedosto.](./media/3ZipFile.png)

   ![Valitse tiedosto.](./media/4SelectAFile.png)

1. Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.

   ![Tuo tiedot.](./media/5ImportData.png)

1. Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan. Kun tuonti on valmis, sulje ohjattu CMT-toiminto. 
1. Tarkista organisaatiosi tiedot seuraavissa 18 entiteetissä:

    -   Valuutta
    -   Tili
    -   Organisaatioyksikkö
    -   Ota yhteyttä
    -   Yksikkö
    -   Yksikköryhmä
    -   Hinnasto
    -   Projektin parametrin hinnasto 
    -   Laskutustiheys
    -   Varattavissa olevan resurssin luokka
    -   Tapahtumakategoria
    -   Kululuokka
    -   Roolin hinta
    -   Tapahtumaluokan hinta
    -   Ominaisuus
    -   Varattavissa oleva resurssi
    -   Varattavissa olevan resurssin luokkaliitos
    -   Varattavissa olevan resurssin ominaisuus

    ![Suorita tuonti.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
