---
description: Aktualisiert die Satzdefinition für einen vorhandenen Asset-Satz.
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 5%

---

# setAssetSetDefinition{#setassetsetdefinition}

Aktualisiert die Satzdefinition für einen vorhandenen Asset-Satz.

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
| companyHandle | `xsd:string` | Ja | Das -Handle an die Firma mit dem Asset-Set. |
| assetHandle | `xsd:string` | Ja | Asset-Handle |
| setDefinition | `xsd:string` | Ja | Definitionszeichenfolge. Siehe unten. |

**Ausgabe (setAssetSetDefinitionReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## setDefinition-Parameter: Info {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition-Funktionen**

Geben Sie `setDefinition` Substitutionsfunktionen inline an. Diese werden bei einer Katalogsuche oder bei der Veröffentlichung aufgelöst. Ersatzzeichenfolgen haben das Format `${<substitution_func>}` und umfassen Folgendes:

>[!NOTE]
>
>Handler-Literale in den Parameterlisten müssen von Klammern `([])` umgeben sein. Der Text außerhalb einer Ersatzzeichenfolge wird während der Auflösung in die Ausgabezeichenfolge kopiert.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Substitutionsfunktion </th> 
   <th colname="col2" class="entry"> Gibt den des Assets zurück. </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Primärer Dateipfad. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogD([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Katalog-ID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>],[ <span class="varname"> metadata_field_handle </span>]) </span> </td> 
   <td colname="col2"> Metadatenwert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Katalog-ID. Gilt für bildbasierte Assets (Bild, angepasste Ansicht, Ebenenansicht). <p>Für andere Assets gibt die Katalog-ID des Miniatur-Assets zurück (falls vorhanden). Wenn dem Asset kein Miniatur-Asset zugeordnet ist, gibt die Funktion eine leere Zeichenfolge zurück. </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition-Beispiele**

Diese Zeichenfolge für die Mediensatzdefinition:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Wird bei der Suche oder Veröffentlichung wie folgt aufgelöst:

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Beispiele {#section-739b42eec3074cafae285ec015a2d088}

**Anfrage**

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
