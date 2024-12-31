---
description: Durchsucht das Metadaten-Index-Repository nach den angegebenen Suchbegriffen. Gibt Asset-Daten wie die searchAssets-Methode zurück.
solution: Experience Manager
title: searchAssetsByMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: a0e01edb-c52b-436d-a166-e24cc6861c49
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 5%

---

# searchAssetsByMetadata{#searchassetsbymetadata}

Durchsucht das Metadaten-Index-Repository nach den angegebenen Suchbegriffen. Gibt Asset-Daten wie die searchAssets-Methode zurück.

`searchAssetsByMetadata` können Sie zwar nach benutzerdefinierten Metadatenfeldern suchen, diese Felder werden jedoch nicht zurückgegeben, wenn sie im `responseMetadataArray` angegeben sind. Um diesen Punkt zu veranschaulichen, führen Sie folgendes Codebeispiel aus:

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

Gibt einen Nullwert zurück:

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

Um dieses Problem zu umgehen, können Sie die `fieldHandles` der Assets verwenden, die von der Suche zurückgegeben werden, um `getAssets` auszuführen (siehe auch [getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). Diese Methode ruft die Werte der benutzerdefinierten Felder für die betreffenden Assets ab. Verwenden Sie das folgende Syntaxbeispiel, um nach benutzerdefinierten Metadatenfeldern zu suchen:

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

**Eingabe (searchAssetsByMetadataParam)**

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
   <td colname="col4"> <p>Der Griff zum Unternehmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Filter</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Filter, mit denen Sie Suchkriterien definieren können. </p> <p>Siehe <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Bedingungen, die Suchkriterien definieren. Weitere Informationen finden Sie unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ResponseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Zusätzliche Felder, die mit der Antwort in der Asset-Zusammenfassung ausgefüllt werden sollen. Die Felder müssen im normalisierten Format angegeben werden. </p> </td> 
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
   <td colname="col4"> <p>Gibt die zurückzugebende Ergebnisseite basierend auf der Seitengröße <span class="codeph"> recordsPerPage </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortBy</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Sortieren nach ausgewähltem Asset-Feld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Auswahl der Sortierrichtung. Aufsteigend ist Standard. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (searchAssetsByMetadataReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| totalRows | `xsd:int` | Nein | Anzahl Übereinstimmungen. |
| assetArray | `types:AssetArray` | Nein | Array von Assets, die von der Suche zurückgegeben werden. |

## metadataConditionArray-Details {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**Artikelstruktur**

`metadataConditionArray` Struktur sieht wie folgt aus:

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**Werte**

`field_handle` ist der Metadaten-Suchschlüssel. Sie kann Punktnotation enthalten. Mögliche Werte sind:

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
* `created_at` (wie `modified_at` (Datum im Formular: Fr. Jul 25 2014 22:13:45 GMT-0500 (CDT)))

* `created_by`

**Zulässige Benutzer**

Die [!DNL operator] definiert, wie der Wert verglichen und einbezogen wird:

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

Der `comparison_value` ist der Begriff, nach dem gesucht werden soll.

## Beispiele {#section-53a12b9c023e4e629eddf5719c955ad4}

Dieses Codebeispiel führt eine Suche mit den folgenden Metadatenkriterien durch:

* `name` Feld enthält `1000801`.

* `dc.rights` Feld ist gleich `Per Jessen Schmidt`.

**Anfrage**

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
