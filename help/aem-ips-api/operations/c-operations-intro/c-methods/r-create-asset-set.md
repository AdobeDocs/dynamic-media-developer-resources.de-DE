---
description: Erstellt einen generischen Asset-Satz mit einer Definitionszeichenfolge für Rohsätze, der auf einem Image-Server veröffentlicht werden soll.
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 6%

---

# createAssetSet{#createassetset}

Erstellt einen generischen Asset-Satz mit einer Definitionszeichenfolge für Rohsätze, der auf einem Image-Server veröffentlicht werden soll.

Syntax

## Autorisierte Benutzertypen {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-3580b586296e42a5b21426085b1bb72d}

**Eingabe (createAssetSet)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle für das Unternehmen, das das Asset-Set enthalten wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Handle für den Ordner, in dem der neue Asset-Satz erstellt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Asset-Name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Eine eindeutige Kennung, die vom Client für den Asset-Set-Typ erstellt wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Die Parameter in der Definitionszeichenfolge des Sets. <p>Diese müssen in dem Format aufgelöst werden, das vom Ziel-Viewer angegeben wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Handle des Assets, das als Miniaturansicht für das neue Bildset dient. Wenn kein Wert angegeben ist, versucht IPS, das erste Bild-Asset zu verwenden, auf das vom Set verwiesen wird. </td> 
  </tr> 
 </tbody> 
</table>

**Ersatzfunktionen für setDefinition**

Sie können Ersatzfunktionen in Zeilen angeben, die während der Katalogsuche oder -veröffentlichung aufgelöst werden. Ersatzzeichenfolgen haben das Format `${<substitution_func>}`. Die verfügbaren Funktionen werden unten aufgelistet.

>[!NOTE]
>
>Die Handle-Literale in Parameterlisten müssen von Klammern umgeben sein `([])`. Sämtlicher Text, der sich außerhalb einer Ersatzzeichenfolge befindet, wird während der Auflösung wörtlich in die Ausgabezeichenfolge kopiert.

| **Substitutionsfunktion** | **Rückgabe** |
|---|---|
| `getFilePath([asset_handle>])` | Der Dateipfad der Primärquelle des Assets. |
| `getCatalogId([<asset_handle>])` | Die Katalog-ID des Assets. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Metadatenwerte für das Asset. |
| `getThumbCatalogId([<asset_handle>])` | Die Katalog-ID des Assets (nur für bildbasierte Assets). Die Katalog-ID des zugehörigen Miniatur-Assets (für andere Assets). Wenn kein verknüpftes Miniatur-Asset verfügbar ist, gibt die Funktion eine leere Zeichenfolge zurück. |

**Beispiel für Media setDefinition String**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Bei Katalogsuche oder Veröffentlichungszeit wird dies in eine Zeichenfolge ähnlich der folgenden aufgelöst:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Ausgabe (createAssetSet)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Das Handle für den Asset-Satz. |

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
