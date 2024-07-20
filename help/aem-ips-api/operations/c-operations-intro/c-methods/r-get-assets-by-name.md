---
description: Gibt Assets basierend auf einem Array von Asset-Namen zurück.
solution: Experience Manager
title: getAssetsByName
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e48574e3-9d16-45fb-b4c8-98b5e092e611
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 10%

---

# getAssetsByName{#getassetsbyname}

Gibt Assets basierend auf einem Array von Asset-Namen zurück.

Syntax

## Autorisierte Benutzertypen {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Gibt nur Assets zurück, auf die der Benutzer Lesezugriff hat.

## Parameter {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**Input (getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Erforderlich </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Handle für das Unternehmen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Bietet Zugriff als anderer Benutzer. Nur für Administratoren verfügbar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Wird zum Filtern nach einer bestimmten Gruppe verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Array von Asset-Namen, die abgerufen werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Asset-Typen, die für abgerufene Assets zulässig sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Asset-Typen, die für abgerufene Assets ausgeschlossen sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Array von Asset-Untertypen, die für abgerufene Assets zulässig sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Wenn <span class="codeph"> true</span> und <span class="codeph"> assetSubTypeArray</span> nicht leer sind, werden nur Assets zurückgegeben, deren Untertypen sich in <span class="codeph"> assetSubTypeArray</span> befinden. </p> <p>Wenn der Wert <span class="codeph"> false</span> ist, werden Assets ohne definierten Untertyp einbezogen. </p> <p>Der Standardwert ist <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Enthält eine Liste von Feldern und Unterfeldern, die in der Antwort enthalten sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Enthält eine Liste von Feldern und Unterfeldern, die von der Antwort ausgeschlossen sind. </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssetsByNameReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetArray | `types:AssetArray` | Nein | Array von Assets, die den Filterkriterien entsprechen. |

## Beispiele {#section-3b7447398e574c88aeaf8ca159cc78dd}

Dieses Codebeispiel gibt zwei Bildtyp-Assets zurück.

**Anfrage**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**Antwort**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```
