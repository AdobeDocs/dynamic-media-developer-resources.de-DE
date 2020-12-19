---
description: Erstellen oder bearbeiten Sie ein Metadatenfeld. Lassen Sie den optionalen Feldgriff aus, um ein neues Metadatenfeld zu erstellen.
seo-description: Erstellen oder bearbeiten Sie ein Metadatenfeld. Lassen Sie den optionalen Feldgriff aus, um ein neues Metadatenfeld zu erstellen.
seo-title: saveMetadataField
solution: Experience Manager
title: saveMetadataField
topic: Scene7 Image Production System API
uuid: ccd84366-732a-4caf-914d-3bc5fe499e7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 8%

---


# saveMetadataField{#savemetadatafield}

Erstellen oder bearbeiten Sie ein Metadatenfeld. Lassen Sie den optionalen Feldgriff aus, um ein neues Metadatenfeld zu erstellen.

>[!NOTE]
>
>Diese Methode ist veraltet.

## Autorisierte Benutzertypen {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-ec6827d485a143f4a059a92b18e40f4e}

**Input (saveMetadataFieldParam)**

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
   <td colname="col4"> Der Griff zur Firma. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Feldgriff. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Auswahl der Asset-Typen, aus denen Metadaten gespeichert werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Feldname. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Auswahl der Metadatenfeldtypen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Standardwert der Felder für alle Assets. </td> 
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
 </tbody> 
</table>

**Output (saveMetadataFieldReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Ja | Handhabung des neuen Metadatenfelds. |

## Beispiele {#section-4441c26d1f41466ba972b43dd5189e89}

In diesem Codebeispiel wird ein neues Metadatenfeld erstellt, das durch die Zeichenfolgenkonstanten &quot;Asset-Typ&quot;und &quot;Metadatenfeldtypen&quot;eingeschränkt wird. Wenn das `fieldHandle`-Element einen gültigen field handle-Wert hat, werden die Metadatenwerte geändert und dasselbe field-Handle erhalten, das Sie in der Anforderung angegeben haben.

**Anforderung**

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

