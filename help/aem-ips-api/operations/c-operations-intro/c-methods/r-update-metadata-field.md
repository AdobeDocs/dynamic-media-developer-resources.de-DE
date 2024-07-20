---
description: Aktualisieren von Feldmetadaten.
solution: Experience Manager
title: updateMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 67506e76-aa23-46a7-a900-03d89b4266fd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 11%

---

# updateMetadataField{#updatemetadatafield}

Aktualisieren von Feldmetadaten.

Syntax

## Autorisierte Benutzertypen {#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-69681ed1ddff437ca1c73f46fe835c96}

**Input (updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parametername </th> 
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
   <td colname="col4"> Handle des Unternehmens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handle für Metadatenfelder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Name des Metadatenfelds. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Metadatenfeldwert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ausblenden oder Anzeigen von IPS-systemspezifischen Metadaten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Eine boolesche Kennzeichnung, die anzeigt, ob das Metadatenfeld erzwungen (validiert) wird, wenn der Wert festgelegt wird. </p> <p>Wenn der Wert auf "true"gesetzt ist, wird ein Fehler ausgegeben, wenn ein illegaler Wert in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span> festgelegt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ermöglicht die Erstellung eines Satzes gemeinsamer Auflistungswerte, auf den ausgewählte Tags verweisen können. </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateMetadataFieldReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | Handle für Metadatenfelder. |

## Beispiele {#section-bb7d93ab6d914ddfa294e08983e589ee}

Diese Codebeispielaktualisierungen weisen einem Metadatenfeld einen neuen Namen und einen neuen Standardwert zu. Die Antwort gibt ein Handle an das aktualisierte Feld zurück.

**Anfrage**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**Antwort**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```
