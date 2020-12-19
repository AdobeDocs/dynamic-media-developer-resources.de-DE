---
description: Suchen Sie nach Assets, die auf Ihren angegebenen Kriterien basieren.
seo-description: Suchen Sie nach Assets, die auf Ihren angegebenen Kriterien basieren.
seo-title: searchAssets
solution: Experience Manager
title: searchAssets
topic: Scene7 Image Production System API
uuid: 125e9e0d-1856-4e80-9778-ca93cd04b766
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 7%

---


# searchAssets{#searchassets}

Suchen Sie nach Assets, die auf Ihren angegebenen Kriterien basieren.

Syntax

## searchAssets: Über {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` ist die primäre Methode zum Abrufen von IPS-Assets. Diese Methode wird für verschiedene Zwecke verwendet, z. B. zum Durchsuchen der Ordnerhierarchie oder zum Suchen eines bestimmten Assets anhand des Namens.

**Antwortgröße**

`searchAssets` gibt bis zu 1000 Assets in einem einzelnen Aufruf zurück. Um bis zu 10.000 Assets pro Aufruf zurückzugeben, beschränken Sie die Antwortdaten auf eine Untergruppe der Felder `totalRows`, `name`, `handle`, `type` und `subType`. Um größere Sätze zurückzugeben, richten Sie die Paging-Funktion mit dem Parameter `resultPage` ein.

**Ergebnisdateigröße mit responseFieldArray oder excludeFieldArray begrenzen**

Begrenzen Sie die Größe Ihres Datensatzes mit den Parametern `responseFieldArray` oder `excludFieldArray`. Diese Parameter helfen dabei, den Arbeitsspeicher und die Bandbreite zu reduzieren und die Reaktionszeit des Servers zu verbessern.

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
>Der Benutzer muss über Lesezugriff verfügen, um Assets zurückgeben zu können.

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
   <td colname="col4"> Das Handle zur Firma mit den Assets, die Sie suchen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Damit können Administratoren als andere Benutzer arbeiten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Damit können Administratoren als Teil einer anderen Gruppe arbeiten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Der Stammpfad für die Suche nach Assets. Wenn dieser Wert weggelassen wird, wird der Stammordner der Firma verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Auf <span class="codeph"> true</span> setzen, um Unterordner zu suchen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Auswahl des Veröffentlichungsstatus </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Auswahl des Papierkorbszustands. Der Standardwert ist <span class="codeph"> NotInPapierkorb</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> bedingungMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Auswahl der Suchübereinstimmungsmodi für die Kombination der Ergebnisse von <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> bedingungMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span> und  <span class="codeph"> metadataConditionArray</span>. Der Standardwert ist <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> <p>Hinweis:  Veralteter Parameter. Es wird empfohlen, dass Sie es nicht verwenden. </p> </p> <p>Ein String-Array mit Suchbegriffen, die übereinstimmen sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Auswahl der Suchübereinstimmungsmodi für die Kombination von <span class="codeph"> systemFieldCondition</span>-Übereinstimmungen. Der Standardwert ist <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Typen:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Das Array der Systemfeldbedingungen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Zeichenfolgenkonstanten für Suchabgleich-Modi. Der Standardwert ist <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:TagConditionArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Ein Array von Tag-Feld-Suchvorausschätzungen. </p> <p>Eigenschaften werden gemäß der Einstellung <span class="codeph"> tagMatchMode</span> kombiniert und dann mit allen Begriffen in <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span> und <span class="codeph"> metadataConditionArray</span> gemäß <span class="codeph"> ConditionMatchMode</span>-Einstellung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Suchübereinstimmungsmodi zum Kombinieren von <span class="codeph"> metadataCondition</span>-Übereinstimmungen. Der Standardwert ist <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> Typen:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Das Array der Suchbedingungen für Metadatenfelder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Asset-Typen, die in die Suche einbezogen werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Asset-Typen, die von der Suche ausgeschlossen werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Eine Liste von Subtypnamen, nach denen gefiltert werden soll. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> striktSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Wenn <span class="codeph"> true</span> und <span class="codeph"> assetSubTypeArray</span> nicht leer sind, werden nur Assets zurückgegeben, deren Untertypen in <span class="codeph"> assetSubTypeArray</span> liegen. Wenn <span class="codeph"> false</span> (Standard), werden Assets ohne definierten Untertyp zurückgegeben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Wenn "true", werden bei der Erfassung eines primären Assets generierte Nebenprodukt-Assets, wie z. B. gerippte PDF-Seitenbilder, aus den Suchergebnissen ausgeschlossen. Der Standardwert ist „false“. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> Typen:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Bedingungen zur Asset-Erstellung, die von den Suchergebnissen ausgeschlossen werden sollen. Wenn dieser Parameter vorhanden ist, setzt er die Einstellung excludeByproducts außer Kraft. </td> 
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
   <td colname="col4"> Maximale Anzahl der zurückzugebenden Ergebnisse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Gibt die Seite der zurückzugebenden Ergebnisse basierend auf dem Seitenformat <span class="codeph"> recordsPerPage</span> an. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Auswahl der Asset-Sortierfelder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Auswahl der Sortierrichtung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Enthält eine Liste von Feldern und Unterfeldern, die in die Antwort aufgenommen werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Enthält eine Liste von Feldern und Unterfeldern, die von der Antwort ausgeschlossen werden sollen. </td> 
  </tr> 
 </tbody> 
</table>

**Output (searchAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | Nein | Anzahl der Zeilen, die eine Suche zurückgibt, wenn Datensätze pro Seite nicht begrenzt sind. |
| ` *`assetArray`*` | `types:AssetArray` | Nein | Assets, die von der Suche zurückgegeben werden. |

## Beispiele {#section-725484cc09b54772a838ad2cc930b94b}

Dieses Codebeispiel sucht nach Bild-Assets, die zu einer bestimmten Firma gehören. Die Antwort wird wegen ihrer Kürze abgeschnitten.

**Anforderung**

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

