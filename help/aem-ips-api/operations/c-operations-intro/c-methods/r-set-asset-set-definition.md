---
description: Aktualisiert die Set-Definition für einen vorhandenen Asset-Set.
seo-description: Aktualisiert die Set-Definition für einen vorhandenen Asset-Set.
seo-title: setAssetSetDefinition
solution: Experience Manager
title: setAssetSetDefinition
topic: Scene7 Image Production System API
uuid: 2a2dce5d-7a01-49af-ac8b-33ae0b234ecc
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 6%

---


# setAssetSetDefinition{#setassetsetdefinition}

Aktualisiert die Set-Definition für einen vorhandenen Asset-Set.

Syntax

## Autorisierte Benutzertypen {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Input (setAssetDefinitionParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle zur Firma mit dem Asset-Set. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Asset-Set-Handle |
| ` *`setDefinition`*` | `xsd:string` | Ja | Definitionszeichenfolge. Siehe unten. |

**Output (setAssetSetDefinitionReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## setDefinition-Parameter: Info {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition-Funktionen**

Legen Sie `setDefinition` die Ersatzfunktionen inline fest. Diese werden während einer Katalogsuche oder bei der Veröffentlichung behoben. Ersatzzeichenfolgen haben das Format `${<substitution_func>}`und beinhalten Folgendes:

>[!NOTE]
>
>Handle-Literale in den Listen der Parameter müssen in Klammern stehen `([])`. Der Text außerhalb einer Ersatzzeichenfolge wird während der Auflösung in die Ausgabestrategie kopiert.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Substitutionsfunktion </th> 
   <th colname="col2" class="entry"> Gibt die </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Primär-Dateipfad. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Katalog-ID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>],[ <span class="varname"> metadata_field_handle </span>]) </span> </td> 
   <td colname="col2"> Metadatenwert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Katalog-ID. Gilt für bildbasierte Assets (Image, Angepasste Ansicht, Layer Ansicht). <p>Bei anderen Assets wird die Katalog-ID des Daumenassets zurückgegeben (sofern vorhanden). Wenn dem Asset kein Thumb-Asset zugeordnet ist, gibt die Funktion eine leere Zeichenfolge zurück. </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition-Beispiele**

Diese Medienset-Definitionszeichenfolge:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Löst zur Nachschlagezeit oder zur Veröffentlichungszeit Folgendes auf:

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Beispiele {#section-739b42eec3074cafae285ec015a2d088}

**Anforderung**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Antwort**

Keine.
