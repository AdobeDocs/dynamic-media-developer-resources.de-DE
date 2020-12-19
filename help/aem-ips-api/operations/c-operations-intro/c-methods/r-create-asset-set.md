---
description: Erstellt einen generischen Asset-Satz mit einer Definitionszeichenfolge für Rohsätze, die auf einem Image-Server veröffentlicht wird.
seo-description: Erstellt einen generischen Asset-Satz mit einer Definitionszeichenfolge für Rohsätze, die auf einem Image-Server veröffentlicht wird.
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 6%

---


# createAssetSet{#createassetset}

Erstellt einen generischen Asset-Satz mit einer Definitionszeichenfolge für Rohsätze, die auf einem Image-Server veröffentlicht wird.

Syntax

## Autorisierte Benutzertypen {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-3580b586296e42a5b21426085b1bb72d}

**Input (createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle für die Firma, die den Asset-Set enthalten soll. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle für den Ordner, in dem der neue Asset-Satz erstellt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Asset-Name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Eine eindeutige ID, die vom Client für den Asset-Set-Typ erstellt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Die Parameter in der Zeichenfolge für die festgelegte Definition. <p>Diese müssen in dem vom Zielgruppe-Viewer angegebenen Format aufgelöst werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Handhabung des Assets, das als Miniaturansicht für den neuen Bildsatz fungiert. Ist dies nicht der Fall, versucht IPS, das erste Bild-Asset zu verwenden, auf das der Satz verweist. </td> 
  </tr> 
 </tbody> 
</table>

**Ersatzfunktionen für setDefinition**

Sie können Ersatzfunktionen in einer Zeile angeben, die während der Katalogsuche oder -veröffentlichung aufgelöst werden. Ersatzzeichenfolgen haben das Format `${<substitution_func>}`. Die verfügbaren Funktionen werden nachfolgend aufgelistet.

>[!NOTE]
>
>Die Handle-Literale in den Parameter-Listen müssen von Klammern `([])` umgeben sein. Der gesamte Text, der sich außerhalb einer Ersatzzeichenfolge befindet, wird während der Auflösung wörtlich in die Ausgabestrategie kopiert.

| **Substitutionsfunktion** | **Rückgabe** |
|---|---|
| `getFilePath([asset_handle>])` | Der primäre Dateipfad des Assets. |
| `getCatalogId([<asset_handle>])` | Die Katalog-ID des Assets. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Metadatenwerte für das Asset. |
| `getThumbCatalogId([<asset_handle>])` | Die Katalog-ID des Assets (nur für bildbasierte Assets). Die Katalog-ID des zugehörigen Daumenassets (für andere Assets). Wenn kein verknüpftes Thumb-Asset verfügbar ist, gibt die Funktion eine leere Zeichenfolge zurück. |

**Beispiel für einen MediensetDefinition-String**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Beim Suchen oder Veröffentlichen eines Katalogs wird diese in eine Zeichenfolge wie die folgende aufgelöst:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Output (createAssetSet)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Das Handle zum Asset-Set. |

## Beispiele {#section-fed53089de824d67ab96cd9103d384b4}

**Anforderung**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Antwort**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```

