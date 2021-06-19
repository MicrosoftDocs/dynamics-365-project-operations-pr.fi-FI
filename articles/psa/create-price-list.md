---
title: Hinnaston luominen
description: Hinnaston luominen Project Servicessä
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32f0cc66d1caa08bd24eb232338444df0388de3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006057"
---
# <a name="create-a-price-list-project-service"></a>Hinnaston luominen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Hinnastot sisältävät mallin jota asiakkuuspäälliköt voivat käyttää luotaessa tarjouksia ja projekteja ja projektin kustannusten määrittämisessä. Ne sisältävät roolien ja kulujen rivinimikeluettelon ja niistä veloitettava hinnan. Luomalla useita hinnastoja voit ylläpitää erilaisia hinnoittelurakenteita eri alueilla myytäviä tuotteita tai kanavia varten. On hyvä luoda vähintään yksi hinnasto jokaiselle valuutalle jossa asiakkaita on tarkoitus laskuttaa.  
  
Toimitettavan työn rahoitusta koskevien arvioiden luomiseksi varmista, että jokaisella projektilla on kustannus- ja myyntihinnaston varmuuskopio. Määritä oletusarvoinen kustannus- ja myyntihinnasto, jota käytetään yrityksesi kaikissa projekteissa.  
  
Hinnastot perustuvat rooleihin ja kululuokkiin. Ennen kuin luot hinnaston, varmista, että olet aiemmin määrittänyt roolit ja kululuokat, joita haluat käyttää hinnaston luomisen yhteydessä.  
  
1.  Siirry kohtaan **Project Service > Hinnastot**.  
  
2.  Valitse **Uusi**.  
  
3.  Kohdassa **Konteksti** valitse, onko tämä **Kustannus**, **Osto** tai **Myynti** -hinnasto.  
  
4.  Kohtaan **Nimi** kirjoita hinnaston nimi.  
  
5.  Kohdassa **Valuutta** valitse laskutuksessa tai kustannuslaskelmassa käytettävä valuutta.  
  
6.  Kohdassa **Aikayksikkö** määritä aikaväli, jota hinta koskee, esimerkiksi päivä tai tunti.  
  
7.  Täytä **Alkamispäivä**, **Päättymispäivä** ja **Kuvaus** tarpeen mukaan.  
  
8.  Valitse **Tallenna** ja luo tietue, jotta voit jatkaa muokkaamista.  
  
9. Lisää roolin hinta hinnastoon, valitse **+** kohdassa **Roolin hinnat**.  
  
10. **Roolin hinta** -ruudussa täytä tiedot ja valitse sitten **Tallenna**. Jatka roolihintojen lisäämistä tarpeen mukaan. Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.  
  
11. Lisää kululuokan hinta hinnastoon valitsemalla **+** kohdassa **Luokan hinnat**.  
  
12. **Tapahtumaluokan hinta** -ruudussa täytä tiedot ja valitse sitten **Tallenna**. Jatka luokan hintojen lisäämistä tarpeen mukaan. Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.  
  
13. Jos haluat lisätä hinnastoon hinnaston nimikkeet, valitse **+** kohdassa **Hinnaston nimikkeet**.  
  
14. **Hinnaston nimike** -ruudussa täytä tiedot ja valitse sitten **Tallenna**. Jatka hinnaston nimikkeiden lisäämistä tarpeen mukaan. Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.  
  
15. Lisää aluesuhteita hinnastoon valitsemalla **+** kohdassa **Aluesuhteet**.  
  
16. **Uusi yhteys** -valintaikkunassa täytä tiedot ja valitse sitten **Tallenna**. Jatkaa aluesuhteiden lisäämistä tarpeen mukaan. Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.  
  
### <a name="see-also"></a>Katso myös  
 [Project Service Automationin määrittäminen](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]