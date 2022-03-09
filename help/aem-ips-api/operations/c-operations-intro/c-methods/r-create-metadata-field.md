---
description: Ermöglicht Administratoren das Erstellen neuer Metadatenfelder zur Koordinierung mit Content Management-Systemen oder für Vorlagenvorgänge. Beispiele für erstellte Metadatenfelder sind Suchbegriffe, Informationen zum Autor des Bildes oder Informationen zum Urheberrechtsinhaber.
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 8%

---

# createMetadataField{#createmetadatafield}

Ermöglicht Administratoren das Erstellen neuer Metadatenfelder zur Koordinierung mit Content Management-Systemen oder für Vorlagenvorgänge. Beispiele für erstellte Metadatenfelder sind Suchbegriffe, Informationen zum Autor des Bildes oder Informationen zum Urheberrechtsinhaber.

Syntax

## Autorisierte Benutzertypen {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parameter {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Eingabe (createMetadataFieldParam)**

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
   <td colname="col4"> Name des Unternehmens, zu dem das Metadatenfeld gehört. </td> 
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
   <td colname="col4">Metadatenfeldtyp. <p>Die Konstante für Metadatenfeldtypen definiert die verfügbaren Typen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Der Standardwert des zu erstellenden Metadatenfelds (z. B. <span class="codeph"> Scene7</span>). </p> <p>Standardwerte werden für Tag-Feldtypen nicht unterstützt und müssen weggelassen werden. Wenn für einen Tag-Feldtyp ein nicht leerer Standardwert angegeben ist, wird ein Fehler zurückgegeben. </p> </td> 
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
   <td colname="col4"> <p>Eine boolesche Kennzeichnung, die anzeigt, ob das Metadatenfeld erzwungen (validiert) wird, wenn der Wert festgelegt wird. </p> <p>Wenn der Wert auf "true"gesetzt ist, wird ein Fehler ausgegeben, wenn ein illegaler Wert in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ermöglicht die Erstellung eines Satzes gemeinsamer Auflistungswerte, auf den ausgewählte Tags verweisen können. </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (createMetadataFieldReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | Der Handle für das neue Metadatenfeld. |

## Beispiele {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Dieses Codebeispiel erstellt ein Metadatenfeld vom Typ Zeichenfolge namens `createMetadataField`. Die Antwort gibt den Handle an das neue Metadatenfeld zurück.

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
