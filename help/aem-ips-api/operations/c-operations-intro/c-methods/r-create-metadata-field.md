---
description: Ermöglicht Administratoren das Erstellen neuer Metadatenfelder zur Koordinierung mit Content-Management- oder Vorlagensystemen. Beispiele für erstellte Metadatenfelder sind Suchbegriffe, Informationen zum Autor des Bildes oder Copyright-Inhaberinformationen.
seo-description: Ermöglicht Administratoren das Erstellen neuer Metadatenfelder zur Koordinierung mit Content-Management- oder Vorlagensystemen. Beispiele für erstellte Metadatenfelder sind Suchbegriffe, Informationen zum Autor des Bildes oder Copyright-Inhaberinformationen.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Scene7 Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 7%

---


# createMetadataField{#createmetadatafield}

Ermöglicht Administratoren das Erstellen neuer Metadatenfelder zur Koordinierung mit Content-Management- oder Vorlagensystemen. Beispiele für erstellte Metadatenfelder sind Suchbegriffe, Informationen zum Autor des Bildes oder Copyright-Inhaberinformationen.

Syntax

## Autorisierte Benutzertypen {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parameter {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Input (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Name der Firma, zu der das Metadatenfeld gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Asset-Typ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Name des Metadatenfelds, das Sie erstellen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Metadatenfeldtyp. <p>Die Metadatenfeldtypen-Konstante definiert die verfügbaren Typen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Der Standardwert des zu erstellenden Metadatenfelds (z. B. <span class="codeph"> Scene7</span>). </p> <p>Standardwerte werden für Tag-Feldtypen nicht unterstützt und müssen weggelassen werden. Wenn für einen Tag-Feldtyp eine nicht leere Standardeinstellung angegeben ist, wird ein Fehler zurückgegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> IPS-systemspezifische Metadaten ausblenden oder verfügbar machen </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Ein boolesches Flag, das angibt, ob das Metadatenfeld beim Festlegen des Werts erzwungen (validiert) wird. </p> <p>Wenn "true"festgelegt ist, wird ein Fehler ausgegeben, wenn unter <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span> ein unzulässiger Wert festgelegt wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ermöglicht die Erstellung eines Satzes von freigegebenen nummerierten Werten, auf die ausgewählte Tags verweisen können. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createMetadataFieldReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Ja | Das Handle zum neuen Metadatenfeld. |

## Beispiele {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

In diesem Codebeispiel wird ein Metadatenfeld vom Typ Zeichenfolge mit dem Namen `createMetadataField` erstellt. Die Antwort gibt den Handle an das neue Metadatenfeld zurück.

**Anforderung**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Antwort**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

