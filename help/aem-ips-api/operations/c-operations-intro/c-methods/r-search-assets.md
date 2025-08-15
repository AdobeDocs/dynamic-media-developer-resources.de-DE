---
description: Suche nach Assets basierend auf Ihren angegebenen Kriterien.
solution: Experience Manager
title: SearchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 6%

---

# SearchAssets{#searchassets}

Suche nach Assets basierend auf Ihren angegebenen Kriterien.

Syntax

## searchAssets: Über {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` ist die primäre Methode zum Abrufen von IPS-Assets. Diese Methode wird für verschiedene Zwecke verwendet, z. B. zum Durchsuchen der Ordnerhierarchie oder zum Suchen eines bestimmten Assets anhand des Namens.

**Antwortgröße**

`searchAssets` gibt in einem einzigen Aufruf bis zu 1.000 Assets zurück. Um bis zu 10.000 Assets pro Aufruf zurückzugeben, beschränken Sie die Antwortdaten auf eine Teilmenge der Felder `totalRows`, `name`, `handle`, `type` und `subType`. Um größere Mengen zurückzugeben, richten Sie das Paging mit dem `resultPage` Parameter ein.

**Ergebnisdateigröße mit responseFieldArray oder excludeFieldArray begrenzen**

Begrenzen Sie die Größe Ihres Datensatzes mit den `responseFieldArray`- oder `excludFieldArray`. Diese Parameter tragen dazu bei, die Speichernutzung und Bandbreite zu reduzieren und die Reaktionszeiten des Servers zu verbessern.

## Autorisierte Benutzertypen {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss über Lesezugriff verfügen, um Assets zurückzugeben.

## Parameter {#section-49aabc0600764f55a8b7017d86ded44f}

**Eingabe (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Erforderlich? </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle für das Unternehmen mit den Assets, die Sie suchen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ermöglicht es Administratoren, als ein anderer Benutzer zu arbeiten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ermöglicht es Administratoren, als Teil einer anderen Gruppe zu arbeiten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Ordner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Der Stammpfad für die Suche nach Assets. Wenn ausgelassen, wird der Stammordner des Unternehmens verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Auf "<span class="codeph"> true“ </span>, um Unterordner zu durchsuchen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Auswahl des Veröffentlichungsstatus. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Auswahl des Papierkorb-Status. Der Standardwert ist <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Auswahl der Such-Match-Modi zum Kombinieren der Ergebnisse <span class="codeph"> KeywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span> und <span class="codeph"> metadataConditionArray</span>. Die Standardeinstellung ist <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> SchlüsselwortArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> <p>Hinweis: Veralteter Parameter. Es wird empfohlen, es nicht zu verwenden. </p> </p> <p>Ein Zeichenfolgen-Array von abzugleichenden Schlüsselwörtern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Auswahl der Such-Übereinstimmungsmodi zum Kombinieren <span class="codeph"> systemFieldCondition</span> Übereinstimmungen. Die Standardeinstellung ist <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Das Array von Systemfeldbedingungen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Suche Übereinstimmungsmodi Zeichenfolgenkonstanten. Der Standardwert lautet <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> TagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:TagConditionArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Ein Array von Tag-Feld-Sucheigenschaften. </p> <p>Prädikate werden gemäß der Einstellung <span class="codeph"> tagMatchMode</span> kombiniert und dann mit beliebigen Begriffen in <span class="codeph"> SchlüsselwortArray</span>, <span class="codeph"> systemFieldConditionArray</span> und <span class="codeph"> metadataConditionArray</span> gemäß der Einstellung <span class="codeph"> conditionMatchMode</span> kombiniert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Suchen Sie nach Übereinstimmungsmodi zum Kombinieren <span class="codeph"> Übereinstimmungen mit </span>. Die Standardeinstellung ist <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph">:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Das Array von Suchbedingungen für Metadatenfelder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Asset-Typen, die bei der Suche einbezogen werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Asset-Typen, die von der Suche ausgeschlossen werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Eine Liste mit Namen von Untertypen, nach denen gefiltert werden soll. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Wenn <span class="codeph"> „true</span> und <span class="codeph"> assetSubTypeArray</span> nicht leer ist, werden nur Assets zurückgegeben, deren Untertypen sich in <span class="codeph"> assetSubTypeArray</span> befinden. Wenn „false<span class="codeph"> (Standard)“ </span>, werden Assets ohne definierten Untertyp zurückgegeben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Wenn „true“, werden während der Aufnahme eines primären Assets generierte Nebenprodukt-Assets, wie z. B. ausgelöste PDF-Seitenbilder, aus den Suchergebnissen ausgeschlossen. Der Standardwert ist „false“. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph">:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Bedingungen zur Erzeugung von Nebenprodukt-Assets, die aus Suchergebnissen ausgeschlossen werden sollen. Wenn vorhanden, überschreibt dieser Parameter die Einstellung excludeByproducts . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Handle eines Projekts, das die zu suchenden Assets enthält. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Maximale Anzahl an zurückzugebenden Ergebnissen </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Gibt die zurückzugebende Ergebnisseite basierend auf der Seitengröße <span class="codeph"> recordsPerPage </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Auswahl von Asset-Sortierfeldern. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Auswahl der Sortierrichtung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Enthält eine Liste von Feldern und Unterfeldern , die in die Antwort aufgenommen werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Enthält eine Liste der Felder und Unterfelder zum Ausschluss aus der Antwort. </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (searchAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| totalRows | `xsd:int` | Nein | Anzahl der Zeilen, die eine Suche zurückgibt, wenn Datensätze pro Seite nicht begrenzt sind. |
| assetArray | `types:AssetArray` | Nein | Assets, das die Suche zurückgibt. |

## Beispiele {#section-725484cc09b54772a838ad2cc930b94b}

In diesem Code-Beispiel wird nach Bild-Assets gesucht, die zu einem bestimmten Unternehmen gehören. Die Antwort wird zur Vereinfachung gekürzt.

**Anfrage**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**Antwort**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```
