---
title: Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssä ja Androidissa
description: Tässä aiheessa on yleisiä ohjeita, joiden avulla voit käyttää laajennuksia mukautettujen kenttien toteuttamiseen.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075402"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssä ja Androidissa

[!include [banner](../includes/banner.md)]

Tässä aiheessa on yleisiä ohjeita, joiden avulla voit käyttää laajennuksia mukautettujen kenttien toteuttamiseen. Käsiteltäviä aiheita ovat seuraavat:

- Tietolajit, joita mukautettu kenttäkehys tukee
- Miten näyttää vain luku- tai muokkauskentät työaikaraportin merkinnöissä ja tallentaa käyttäjän antamat arvot tietokantaan
- Vain luku -muotoisten kenttien näyttäminen työaikaraportin otsikossa
- Muiden mukautettujen liiketoimintalogiikkojen integroiminen kenttien oletusarvojen syöttämiseksi ja lisätarkistuksen tekemiseksi

## <a name="audience"></a>Yleisö

Tämä aihe on tarkoitettu sovelluskehittäjille, jotka integroivat mukautettuja kenttiä Microsoft Dynamics 365 Project Timesheet -mobiilisovellukseen, joka on saatavilla Apple iOS- ja Google Android -sovelluksiin. Oletuksena on, että lukijat tuntevat X++-kehitystyön ja projektin työaikaraportin toiminnot.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Tietosopimus – TSTimesheetCustomField X++-luokka

**TSTimesheetCustomField** -luokka on X++-tietosopimusluokka, joka edustaa tietoja mukautetusta kentästä työaikaraportin toiminnallisuuteen. Mukautettujen kenttäobjektien luettelot välitetään sekä TSTimesheetDetails-palvelusopimuksessa että TSTimesheetEntry-tietosopimuksessa mukautettujen kenttien näyttämistä varten mobiilisovelluksessa.

- **TSTimesheetDetails** - Työaikaraportin otsikkosopimus.
- **TSTimesheetEntry** - Työaikaraportin tapahtumasopimus. Näiden objektien ryhmät, joilla on samat projektitiedot ja **timesheetLineRecId** -arvo, muodostavat rivin.

### <a name="fieldbasetype-types"></a>fieldBaseType (Lajit)

**TsTimesheetCustom** -objektin **FieldBaseType** -ominaisuus määrittää sovelluksessa näkyvän kentän tyypin. Seuraavat **Tyypit** -arvot ovat tuettuja.

| Tyypin arvo | Laji              | Muistiinpanot |
|-------------|-------------------|-------|
| 0           | Merkkijono (ja Enum) | Kenttä näkyy tekstikenttänä. |
| 1           | Integer           | Arvo näkyy numerona, jossa ei ole desimaaleja. |
| 2           | Reaali              | Arvo näkyy numerona, jossa on desimaaleja.<p>Jos haluat näyttää sovelluksessa todellisen arvon valuuttana, käytä **fieldExtenededType** -ominaisuutta. **numberOfDecimals** -ominaisuuden avulla voit määrittää näytettävien desimaalien määrän.</p> |
| 3           | Päivä              | Päivämäärämuodot määräytyvät **Käyttäjän asetukset** -kohdassa **kieli ja maa/alue** -asetuksen mukaan määräytyvien käyttäjien **päivämäärä-, kellonaika- ja lukumuoto** -asetusten mukaan. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Jos **TSTimesheetCustomField** -objektissa ei ole **stringOptions** -ominaisuutta, käyttäjälle toimitetaan vapaamuotoinen tekstikenttä.

    **stringLength** -ominaisuuden avulla voidaan määrittää merkkijonon enimmäispituus, jonka käyttäjät voivat syöttää.

- Jos **TSTimesheetCustomField** -objektissa on **stringOptions** -ominaisuus, nämä luetteloelementit ovat ainoat arvot, joita käyttäjät voivat valita valintanappien avulla.

    Tässä tapauksessa merkkijonokenttä voi toimia luettelointi-arvona käyttäjämerkintää varten. Jos haluat tallentaa arvon tietokantaan valintaluettelolla, yhdistä se manuaalisesti uudelleen luettelointiarvoon, ennen kuin tallennat tietokantaan komentoketjulla (lisätietoja on kohdassa "käytä komentoa TSTimesheetEntryService-luokassa, kun haluat tallentaa tuntilomakemerkinnän sovelluksesta uudelleen tietokantaan"-osaan jäljempänä tässä aiheessa).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Tämän ominaisuuden avulla voit muotoilla reaaliarvoja valuutalle. Tämä menetelmä on käytettävissä vain, kun **fieldBaseType** -arvo on **Tosi**.

- **TSCustomFieldExtendedType:None** – Muotoilua ei käytetä.
- **TSCustomFieldExtendedType::Currency** – Muotoile arvo valuuttana.

    Kun valuutan muotoilu on aktiivinen, voit käyttää **stringValue** -kenttää ja siirtää sovelluksessa näkyvän valuuttakoodin. Arvo on vain luku -arvo.

    **realValue** -kenttä sisältää rahasummat, jotka tulisi tallentaa tietokantaan.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Tämän ominaisuuden avulla voit määrittää, missä mukautetun kentän pitäisi näkyä sovelluksessa.

- **TSCustomFieldSection::Header** – Kenttä näkyy **Sovelluksen lisätietoja** -osassa. Nämä kentät ovat aina vain luettavissa.
- **TSCustomFieldSection::Line** – Kenttä tulee näkyviin, kun kaikki valmiit rivikentät ovat työaikaraportin kentissä. Nämä kentät voivat olla joko muokattavia tai vain luku -kenttiä.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Tämä ominaisuus määrittää kentän, kun sovelluksen arvot tallennetaan tietokantaan.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Tämä ominaisuus määrittää kentän, kun sovelluksen arvot tallennetaan tietokantaan.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että käyttäjät voivat muokata tuntilomakemerkintäosan kenttää. Määrittämällä ominaisuuden arvoksi **Ei** , voit määrittää kentän vain luku -tilaan.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että tuntilomakemerkintäosan tulisi olla pakollinen.

### <a name="label-str"></a>label (str)

Tämä ominaisuus määrittää otsikon, joka näkyy sovelluksen kentän vieressä.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Merkkijonoluettelo)

Tämä ominaisuus on käytettävissä vain, jos **fieldBaseType** -arvoksi on määritetty **merkkijono**. Jos **stringOptions** on määritetty, valintanappien kautta valittavissa olevat merkkijonoarvot (radiopainikkeet) määritetään luettelon merkkijonojen avulla. Jos merkkijonoja ei ole, vapaatekstimuotoinen merkintä merkkijonokentässä sallitaan (lisätietoja on kohdassa "Käyttöketjun hallinta TSTimesheetEntryService-luokassa, kun tuntilomakemerkintä tallennetaan sovelluksesta uudelleen tietokantaan" -osaan jäljempänä tässä aiheessa).

### <a name="stringlength-int"></a>strinLength (kokonaisluku)

Tämä ominaisuus määrittää merkkijonokentän enimmäispituuden. Se on käytettävissä vain, jos **fieldBaseType** -arvoksi on määritetty **merkkijono**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (kokonaisluku)

Tämä ominaisuus määrittää todelliselle kentälle näytettävien desimaalien määrän. Se on käytettävissä vain, jos **fieldBaseType** -arvoksi on määritetty **todellinen**.

### <a name="ordersequence-int"></a>orderSequence (kokonaisluku)

Tämä ominaisuus määrittää, missä järjestyksessä mukautetut kentät näkyvät sovelluksessa, kun määritettynä on useampi kuin yksi mukautettu kenttä. Kentät, joiden luvut ovat alemmat, näytetään ensin.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

**Boolean** -tyypin kentissä tämä ominaisuus siirtää kentän totuusarvon palvelimen ja sovelluksen välille.

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** -tyypin kentissä tämä ominaisuus siirtää GUID-arvon palvelimen ja sovelluksen välille.

### <a name="int64value-int64"></a>int64Value (int64)

**Int64** -tyypin kentissä tämä ominaisuus siirtää kentän Int64-arvon palvelimen ja sovelluksen välille.

### <a name="intvalue-int"></a>intValue (int)

**Int** -tyypin kentissä tämä ominaisuus siirtää kentän Int-arvon palvelimen ja sovelluksen välille.

### <a name="realvalue-real"></a>realValue (todellinen)

**Todellinen** -tyypin kentissä tämä ominaisuus siirtää kentän Todellinen-arvon palvelimen ja sovelluksen välille.

### <a name="stringvalue-str"></a>stringValue (str)

**Merkkijono** -tyypin kentissä tämä ominaisuus siirtää kentän merkkijonoarvon palvelimen ja sovelluksen välille. Sitä käytetään myös **todellinen** -tyypin kentissä, jotka on muotoiltu valuutaksi. Näiden kenttien osalta ominaisuutta käytetään valuuttakoodin välittämiseen sovellukseen.

### <a name="datevalue-date"></a>dateValue (päivämäärä)

**Päivämäärä** -tyypin kentissä tämä ominaisuus siirtää kentän päivämääräarvon palvelimen ja sovelluksen välille.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mukautetun kentän näyttäminen ja tallentaminen tuntilomakemerkinnän osassa

Alla on kuvakaappaus tuntilomakemerkinnän luomisesta mobiilisovelluksessa. Siinä näkyy valmiit kentät ja mukautettu kenttä tuntimerkintäosassa nimeltään Test String ja luettelointiarvo Second Option jo asetettu.

![Testimerkkijonon mukautettu kenttä sovelluksessa](media/timesheet-entry.jpg)



Alla on näyttökuva, joka on käyttäjän mobiilisovelluksessa, kun valitaan jokin "testimerkkijonon" mukautetulle kentälle käytettävissä olevista luettelointivaihtoehdoista.  Kaksi vaihtoehtoa ovat ensimmäinen vaihtoehto ja toinen vaihtoehto, joka näkyy valintapainikkeina. Toinen vaihtoehto on tällä hetkellä valittuna.

![Valintanappi (radionappi) testimerkkijonon mukautetulle kentälle](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>TSTimesheetLine-taulukon laajentaminen siten, että siinä on mukautettu kenttä

Tyypillisissä skenaarioissa on todennäköistä, että tuntilomakkeen merkintäosan mukautetun kentän tiedot tallennetaan TSTimesheetLine-tauluun. Muita taulukoita voidaan kuitenkin käyttää, jos tiedot voidaan hakea annetun TSTimesheetTrans-tietueen perusteella tai jos niissä ei ole tiettyä tietuekontekstia (jos esimerkiksi kenttä on määritetty vain luku -tilaan projektiparametreissa).

Huomaa, että mukautettujen kenttien ei tarvitse olla tukitietokannan tietueita. Ne voidaan luoda dynaamisesti X++-logiikan perusteella. Tästä lähestymistavasta voi olla hyötyä vain luku -tilassa (lisätietoja on kohdassa Komentoketju TSTimesheetDetails-luokassa, buildCustomFieldListForHeader-menetelmä, joka täyttää työaikaraportin tiedot-osassa, joka on esimerkki dynaamisesti luoduista mukautettujen kenttien arvoista.)

Alla on Visual Studio -sovellusobjektipuusta otettu näyttökuva. Se näyttää TSTimesheetLine-taulukon laajennuksen, jossa TestLineString-kenttä on lisätty mukautettuna kenttänä.

![Rivimerkkijono](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän tuntilomakemerkinnän osassa

Tämä koodi määrittää sovelluksen kentän näyttöasetukset. Se esimerkiksi määrittää kenttätyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.

Seuraavassa esimerkissä näkyy aikamerkintöjen merkkijonokenttä. Tässä kentässä on kaksi vaihtoehtoa, **Ensimmäinen vaihtoehto** ja **Toinen vaihtoehto** , jotka ovat käytettävissä valintanappien kautta (radionapit). Sovelluksen kenttä liitetään **TestLineString** -kenttään, joka on lisätty TSTimesheetLine-tauluun.

Huomaa kohtien **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** ja **numberOfDecimals** käyttö. Voit myös määrittää nämä parametrit manuaalisesti.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Käytä komentoketjua TSTimesheetEntry-luokan buildCustomFieldListForEntry-menetelmässä, kun haluat syöttää tuntilomakemerkinnän arvot

**buildCustomFieldListForEntry** -menetelmällä syötetään arvoja mobiilisovelluksen tallennettujen työaikaraporttien riveille. Se vie TSTimesheetTrans-tietueen parametriksi. Tietueen kenttien avulla voit täyttää mukautetun kentän arvon sovelluksessa.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Käytä komentoketjua TSTimesheetEntryService-luokassa, kun haluat tallentaa tuntilomakemerkinnän sovelluksesta uudelleen tietokantaan

Jos haluat tallentaa mukautetun kentän tietokantaan tavalliseen käyttöön, sinun täytyy laajentaa useita menetelmiä:

- **timesheetLineNeedsUpdating** -menetelmällä määritetään, onko käyttäjä muuttanut rivitietuetta sovelluksessa, ja se on tallennettava tietokantaan. Jos tehokkuus ei ole ongelma, tätä menetelmää voidaan yksinkertaistaa niin, että se palauttaa aina **tosi** -arvon.
- **populateTimesheetLineFromEntryDuringCreate** - ja **populateTimesheetLineFromEntryDuringUpdate** -menetelmien avulla voi lisätä arvoja TSTimesheetLine tietokantatietueeseen. Seuraavassa esimerkissä määritetään, miten tietokantakentän ja syöttökentän välinen yhdistämismääritys tehdään manuaalisesti X++-koodin kautta.
- **populateTimesheetWeekFromEntry** -menetelmää voidaan myös laajentaa, jos **TSTimesheetEntry** -objektiin yhdistettävän mukautetun kentän täytyy kirjoittaa uudelleen TSTimesheetLineweek-tietokantataulukkoon.

> [!NOTE]
> Seuraavassa esimerkissä tallennetaan **firstOption** - tai **seconnOption** -arvo, jonka käyttäjä valitsee tietokantaan raakamerkkijonoarvona. Jos tietokannan kenttä on **Enum** -tyypin kenttä, arvot voidaan yhdistää manuaalisesti luettelointiarvoon ja tallentaa sitten tietokantataulukon luettelointikenttään.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mukautetun kentän näyttäminen tuntilomakeotsikon osassa

Alla on kuvakaappaus mobiilisovelluksesta, jossa käyttäjä tarkastelee tuntilomaketta. Lisätietoja-painike on valittu oikeassa yläkulmassa, jotta näkyviin tulee Näytä lisätiedot -vaihtoehto.  

![Näytä lisätietoja -komento](media/show-more.png)

Alla on kuvakaappaus mobiilisovelluksen tuntilomakkeen Lisää-osasta. Työaikaraportin otsikko-osaan on lisätty mukautettu kenttä, jonka nimi on tämän tuntilomakkeen käyttöaste (laskettu mukautettu kenttä). Mukautettu kenttä määrittää vain luku -arvon 0.667.

![Lisää-osa](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>TSTimesheetTable-taulukon laajentaminen siten, että siinä on mukautettu kenttä

Tyypillisissä skenaarioissa on todennäköistä, että otsikko-osan tiedot saadaan TSTimesheetHeader-taulusta. Muita taulukoita voidaan kuitenkin käyttää, jos tiedot voidaan hakea annetun TSTimesheetTable-tietueen perusteella tai jos niissä ei ole tiettyä tietuekontekstia (jos esimerkiksi kenttä on määritetty vain luku -tilaan projektiparametreissa).

Huomaa, että mukautettujen kenttien ei tarvitse olla tukitietokannan tietueita. Ne voidaan luoda dynaamisesti X++-logiikan perusteella. Seuraava esimerkki osoittaa tämän lähestymistavan.

Otsikko-osan kentät ovat aina vain luku -tilassa sovelluksessa.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän otsikko-osassa

Tämä koodi määrittää sovelluksen kentän näyttöasetukset. Se esimerkiksi määrittää kenttätyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.

Seuraava esimerkki näyttää lasketun arvon sovelluksen otsikko-osassa.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Käytä komentoketjua TSTimesheetDetails-luokan buildCustomFieldListForHeader-menetelmässä, kun haluat täyttää tuntilomakemerkinnän tiedot

**buildCustomFieldListForHeader** -menetelmää käytetään täyttämään tuntilomakkeen otsikkotiedot mobiilisovelluksessa. Se vie TSTimesheetTable-tietueen parametriksi. Tietueen kenttien avulla voit täyttää mukautetun kentän arvon sovelluksessa. Seuraavassa esimerkissä ei lue tietokannan arvoja. Sen sijaan se luo X++-logiikan avulla lasketun arvon, joka näkyy sovelluksessa.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Muut konfiguroitavuus-/laajennettavuus-mahdollisuudet

### <a name="adding-additional-validation-for-the-app"></a>Sovelluksen lisätarkistuksen lisääminen

Työaikaraportin toimintojen aiemmin luotu logiikka tietokantatasolla toimii silti odotetulla tavalla. Jos haluat keskeyttää Tallenna- tai Lähetä-toimintojen suorittamisen ja näyttää tietyn virhesanoman, voit lisätä **heittovirheen ("viesti käyttäjälle")** -komentolaajennuksen kautta. Seuraavassa on kolme hyödyllistä laajennusmenetelmäesimerkkiä:

- Jos TSTimesheetLine-taulun **validateWrite** palauttaa arvon **epätosi** aikaraportin rivintallennustoiminnon aikana, mobiilisovelluksessa näkyy virhesanoma.
- Jos TSTimesheetTable-taulun **validateSubmit** palauttaa arvon **epätosi** , sovelluksen tuntilomakkeen lähettämisen aikana käyttäjälle näytetään virheilmoitus.
- Logiikka, joka täyttää kentät (esimerkiksi **rivin ominaisuus** ) **Lisää** -menetelmän aikana TSTimesheetLine-taulussa, suoritetaan edelleen.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Valmiiden kenttien piilottaminen ja merkitseminen vain luku -muodossa määrityksen kautta

Projektiparametreistä voit luoda valmiita kenttiä vain luku -muodossa tai piilotettuina mobiilisovelluksessa. Määritä asetukset **projektinhallinta- ja kirjanpitoparametrit** -sivun **tuntilomake** -välilehden **mobiilituntilomakkeet** -kohdassa.

![Projektin parametrit](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Valintaan käytettävissä olevien aktiviteettien muuttaminen laajennusten kautta

Projektiin valittavissa olevat aktiviteetit täytetään **TsTimesheetProjectService** -luokan **getActivitiesForProject()** - ja **getActivityQuery()** - menetelmien kautta. Voit muuttaa tätä tapaa käyttämällä komentoketjua, joka vastaa liiketoimintaskenaariota aktiviteeteille, joita voi valita tietylle projektille.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Oletusprojektiluokan syöttäminen työaikaraportin tapahtumille

Oletusprojektiluokan syöttäminen työaikaraportin tapahtumille tapahtuu kolmella tasolla. Voit käyttää komentoketjua, kun haluat laajentaa käyttäytymistä jollakin tai kaikilla näillä tasoilla halutun käyttäytymisen saavuttamiseksi. Käytetään seuraavaa hierarkiaa:

1. Sovellus yrittää asettaa oletusluokan projektiresurssista. Tämä oletusluokka on määritetty **getCurrentUserResource** - ja **getDelegatedResourcesForCurrentUser** -menetelmille **TSTimesheetSettingsService** -luokassa.
2. Jos oletusluokkaa ei ole projektiresurssitasolla, sovellus yrittää vetää sen projektiaktiviteetista. Tämä oletusluokka määritetään **TSTimesheetProjectService** -luokan **getActivitiesForProject** -menetelmässä.
3. Jos oletuskategoriaa ei anneta projektin aktiviteettitasolla, oletusluokka otetaan projektin parametreista. Tämä oletusluokka määritetään **TSTimesheetProjectService** -luokan **getProjectDetailsbyRule** -menetelmässä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]