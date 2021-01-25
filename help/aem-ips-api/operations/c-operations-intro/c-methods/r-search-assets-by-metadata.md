---
description: Durchsucht das Metadaten-Index-Repository nach den angegebenen Suchbegriffen. Gibt Asset-Daten wie die searchAssets-Methode zurück.
seo-description: Durchsucht das Metadaten-Index-Repository nach den angegebenen Suchbegriffen. Gibt Asset-Daten wie die searchAssets-Methode zurück.
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
topic: Dynamic Media Image Production System API
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 6%

---


# searchAssetsByMetadata{#searchassetsbymetadata}

Durchsucht das Metadaten-Index-Repository nach den angegebenen Suchbegriffen. Gibt Asset-Daten wie die searchAssets-Methode zurück.

Während `searchAssetsByMetadata` die Suche nach benutzerdefinierten Metadatenfeldern ermöglicht, werden diese Felder nicht zurückgegeben, wenn sie in `responseMetadataArray` angegeben sind. Zur Veranschaulichung dieses Punktes ist das folgende Codebeispiel dargestellt:

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

gibt einen Nullwert zurück:

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

Um dieses Problem zu umgehen, können Sie die Elemente `fieldHandles` verwenden, die von der Suche zurückgegeben werden, um `getAssets` auszuführen (siehe auch [getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). Diese Methode ruft die Werte für benutzerdefinierte Felder für die betreffenden Assets ab. Verwenden Sie das folgende Syntaxbeispiel, um nach benutzerdefinierten Metadatenfeldern zu suchen:

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## Autorisierte Benutzertypen {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**Input (searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Griff zur Firma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Filter</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Typ:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Filter, die Ihnen bei der Definition von Suchkriterien helfen. </p> <p>Siehe <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Bedingungen, die Suchkriterien definieren. Weitere Informationen finden Sie unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Zusätzliche Felder, die Sie in der Asset-Zusammenfassung für die Antwort ausgefüllt haben möchten. Die Felder müssen im normalisierten Format angegeben werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Die Anzahl der von der Antwort zurückgegebenen Assets. Der Standardwert ist 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Gibt die Seite der zurückzugebenden Ergebnisse basierend auf dem Seitenformat <span class="codeph"> recordsPerPage</span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortBy</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Sortieren nach ausgewähltem Asset-Feld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Auswahl der Sortierrichtung. Aufsteigend ist der Standardwert. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (searchAssetsByMetadataReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | Nein | Anzahl der Übereinstimmungen. |
| `*`assetArray`*` | `types:AssetArray` | Nein | Array von Assets, die von der Suche zurückgegeben werden. |

## metadataConditionArray Details {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**Elementstruktur**

`metadataConditionArray` Struktur wie folgt:

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**Werte**

`field_handle` ist der Suchschlüssel für Metadaten. Er kann Punktnotation enthalten. Mögliche Werte sind:

* `asset_id` (ohne Präfix)
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (entspricht  `modified_at` (Datum im Formular): 25. Juli 2014 22:13:45 GMT-0500 (CDT))

* `created_by`

**Zugelassene Operatoren**

Das [!DNL operator] definiert, wie der Wert verglichen wird und umfasst:

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

Das `comparison_value` ist der Begriff, nach dem gesucht werden soll.

## Beispiele {#section-53a12b9c023e4e629eddf5719c955ad4}

Dieses Codebeispiel führt eine Suche mit den folgenden Metadatenkriterien durch:

* `name` enthält  `1000801`.

* `dc.rights` field gleich  `Per Jessen Schmidt`.

**Anforderung**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Antwort**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

