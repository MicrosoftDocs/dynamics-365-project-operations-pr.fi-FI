---
title: Käytä esittelyn asennus- ja määritystietoja
description: Tässä aiheessa on tietoja esittelyn asennus- ja määritystietojen käyttöönotosta Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948837"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Ota esittelyn asennus- ja määritystietoja käyttöön Project Operations lite – kauppa proformalaskutukseen -käyttöönotossa

_**Lite-käyttöönotto – kauppa proformalaskutukseen_

1. Lataa [päätietopaketti](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Siirry kansioon *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ja suorita suoritettava tiedosto *DataMigrationUtility*.
3. Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.

![Määrityksen siirto](./media/1ConfigurationMigration.png)

4. Valitse ohjatun CMT-toiminnon sivulla 2 **Office 365** **asennustyypiksi**.
5. Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.
6. Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.

![Kirjautuminen määritykseen](./media/2ConfigurationSignin.png)

7. Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.
8. Valitse sivulla 4 puretusta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* -kansiosta zip-tiedosto *MasterAndSetupData*.

![Zip-tiedosto](./media/3ZipFile.png)

![Valitse tiedosto](./media/4SelectAFile.png)

9. Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.

![Tuo tiedot](./media/5ImportData.png)

10. Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan. Kun tuonti on valmis, sulje ohjattu CMT-toiminto. 
11. Tarkista organisaatiosi tiedot seuraavissa 20 entiteetissä:

- Valuutta
- Organisaatioyksikkö
- Ota yhteyttä
- Veroryhmä
- Asiakasryhmä
- Yksikkö
- Yksikköryhmä
- Hinnasto
- Projektin parametrin hinnasto
- Laskutustiheys
- Laskutustiheyden tiedot
- Varattavissa olevan resurssin luokka
- Tapahtumakategoria
- Kululuokka
- Roolin hinta
- Tapahtumaluokan hinta
- Ominaisuus
- Varattavissa oleva resurssi
- Varattavissa olevan resurssin luokkaliitos
- Varattavissa olevan resurssin ominaisuus

![Suorita tuonti](./media/6CompleteImport.png)
