---
title: createMetadataField
description: Damit können Admins Metadatenfelder erstellen, die mit Content-Management-Systemen oder für Vorlagenvorgänge koordiniert werden. Beispiele für erstellte Metadatenfelder sind Schlüsselwörter, Informationen über den Autor des Bildes oder Informationen über Urheberrechtsinhaber.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 6%

---

# createMetadataField{#createmetadatafield}

Damit können Admins Metadatenfelder erstellen, die mit Content-Management-Systemen oder für Vorlagenvorgänge koordiniert werden. Beispiele für erstellte Metadatenfelder sind Schlüsselwörter, Informationen über den Autor des Bildes oder Informationen über Urheberrechtsinhaber.

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
   <td colname="col4"> Der Name des Unternehmens, zu dem das Metadatenfeld gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Asset-Typ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Name des Metadatenfelds, das Sie erstellen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Metadaten-Feldtyp. <p>Die Konstante Metadatenfeldtypen definiert die verfügbaren Typen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Der Standardwert des zu erstellenden Metadatenfelds (z. B. <span class="codeph"> Scene7</span>). </p> <p>Standardwerte werden für Tag-Feldtypen nicht unterstützt und müssen weggelassen werden. Wenn für einen Tag-Feldtyp ein nicht leerer Standardwert angegeben ist, wird ein Fehler zurückgegeben. </p> </td> 
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
   <td colname="col4"> Damit können Sie einen Satz gemeinsam genutzter spezifischer Werte erstellen, auf die ausgewählte Tags verweisen können. </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (createMetadataFieldReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | Das Handle zum neuen Metadatenfeld. |

## Beispiele {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Dieses Codebeispiel erstellt ein Metadatenfeld vom Typ Zeichenfolge mit dem Namen `createMetadataField`. Die Antwort gibt das Handle zum neuen Metadatenfeld zurück.

**Anfrage**

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
