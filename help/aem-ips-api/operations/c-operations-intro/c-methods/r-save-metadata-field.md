---
title: saveMetadataField
description: Erstellen oder Bearbeiten eines Metadatenfelds. Lassen Sie das optionale Feld-Handle weg, um ein Metadatenfeld zu erstellen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 56a45324-5027-4375-a790-c965f682e4b9
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 8%

---

# saveMetadataField{#savemetadatafield}

Erstellen oder Bearbeiten eines Metadatenfelds. Lassen Sie das optionale Feld-Handle weg, um ein Metadatenfeld zu erstellen.

>[!NOTE]
>
>Diese Methode ist veraltet.

## Autorisierte Benutzertypen {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-ec6827d485a143f4a059a92b18e40f4e}

**Eingabe (saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
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
   <td colname="col4"> Der Griff zum Unternehmen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Feld-Handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Auswahl der Asset-Typen, aus denen Metadaten gespeichert werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Feldname. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Auswahl von Metadaten-Feldtypen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Standardwert der Felder für alle Assets. </td> 
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
 </tbody> 
</table>

**Ausgabe (saveMetadataFieldReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | Handle des neuen Metadatenfelds. |

## Beispiele {#section-4441c26d1f41466ba972b43dd5189e89}

In diesem Codebeispiel wird ein Metadatenfeld erstellt, das durch die Zeichenfolgenkonstanten Asset-Typ und Metadatenfeldtypen eingeschränkt ist. Wenn das `fieldHandle`-Element über einen gültigen Feld-Handle-Wert verfügt, werden die Metadatenwerte geändert und es wird derselbe Feld-Handle abgerufen, den Sie in der Anfrage angegeben haben.

**Anfrage**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**Antwort**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```
