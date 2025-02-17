---
description: Löscht Metadatenwerte für ein Asset. Funktioniert mit einem Array von gelöschten Metadaten, um Werte in einem Batch festzulegen.
solution: Experience Manager
title: deleteAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ce9b8dff-efc0-4427-9f50-10269647187f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 8%

---

# deleteAssetMetadata{#deleteassetmetadata}

Löscht Metadatenwerte für ein Asset. Funktioniert mit einem Array von gelöschten Metadaten, um Werte in einem Batch festzulegen.

Syntax

## Autorisierte Benutzertypen {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Löschzugriff auf das Asset haben.

## Parameter {#section-0eed164e278b456fbdfb7a50727a0416}

**Eingabe (deleteAssetMetadataParam)**

<table id="table_A4438E2FE5F245E5B73F46CD887BE70F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>companyHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Das Handle des Unternehmens, zu dem der Ordner gehört. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>assetHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Das Handle zum zu löschenden Asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metadataDelete </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Aus dem Asset zu löschende Metadaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>deleteArray </p> </td> 
   <td colname="col2"> <p><span class="codeph">:MetadataDeleteArray</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array von Metadaten, die aus dem Asset gelöscht werden sollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (deleteAssetMetadataParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d5657289f5234bb0a613dcf691507958}

MetadataDelete

```java
    <complexType name="MetadataDelete">
        <sequence>
            <element name="fieldHandle" type="xsd:string"/>
        </sequence>
    </complexType>
```

Beispielaufruf

```java
<ac:Request id="deleteAssetMetadata">
 <deleteAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
  <companyHandle>c|101</companyHandle>
  <assetHandle>a|202</assetHandle>
  <deleteArray>
   <items>
    <fieldHandle>m|2919|ASSET|UntypedUDFField1395788289789</fieldHandle>
   </items>
  </deleteArray>
 </deleteAssetMetadataParam>
</ac:Request>
```
