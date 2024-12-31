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

**Eingabe (updateMetadataFieldParam)**

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
   <td colname="col4"> Firmengriff. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handle der Metadatenfelder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Name des Metadatenfelds. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Wert des Metadatenfelds. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> IPS-systemspezifische Metadaten aus- oder einblenden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforce</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Ein boolesches Flag, das angibt, ob das Metadatenfeld erzwungen (validiert) wird, wenn der Wert festgelegt wird. </p> <p>Wenn auf „true“ gesetzt, wird ein Fehler ausgelöst, wenn in <span class="codeph"> setAssetMetadata/</span><span class="codeph"> batchSetAssetMetadata</span> ein unzulässiger Wert festgelegt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ermöglicht die Erstellung eines Satzes von freigegebenen Aufzählungswerten, auf die ausgewählte Tags verweisen können. </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (updateMetadataFieldReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | Handle der Metadatenfelder. |

## Beispiele {#section-bb7d93ab6d914ddfa294e08983e589ee}

Dieses Code-Beispiel wird aktualisiert und weist einem Metadatenfeld einen neuen Namen und einen Standardwert zu. Die Antwort gibt ein -Handle zum aktualisierten Feld zurück.

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
