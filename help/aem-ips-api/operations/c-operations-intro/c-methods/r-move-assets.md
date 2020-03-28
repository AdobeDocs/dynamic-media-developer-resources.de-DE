---
description: Verschiebt mehrere Assets unabhängig voneinander. Dies erfolgt mit dem AssetMove-Typ, der im assetMoveArray enthalten ist. Jedes AssetMove-Feld enthält einen Zielordner.
seo-description: Verschiebt mehrere Assets unabhängig voneinander. Dies erfolgt mit dem AssetMove-Typ, der im assetMoveArray enthalten ist. Jedes AssetMove-Feld enthält einen Zielordner.
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Scene7 Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAssets{#moveassets}

Verschiebt mehrere Assets unabhängig voneinander. Dies erfolgt mit dem AssetMove-Typ, der im assetMoveArray enthalten ist. Jedes AssetMove-Feld enthält einen Zielordner.

Syntax

## Autorisierte Benutzertypen {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-7d47f663474b41cc83439288ac133cc5}

**Input (moveAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle zur Firma mit den zu verschiebenden Assets. |
| ` *`assetMoveArray`*` | `types:AssetMoveArray` | Ja | Ein Asset-Verschiebungsarray. Es enthält ein Asset und einen Asset-Zielordner. |

**Output (moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Asset-Anzahl erfolgreich verschoben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anzahl der Assets, die Warnungen generiert haben, wenn der Vorgang versucht hat, sie zu verschieben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anzahl der Assets, die Fehler generiert haben, wenn der Vorgang versucht hat, sie zu verschieben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaultsets, die Folgendes enthalten: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Assets, die die Warnungen ausgegeben haben. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Warnungscodes. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Grund für die Warnung. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaultsets, die Folgendes enthalten: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Assets, die die Fehler ausgegeben haben. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Fehlercodes. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Grund für die Fehler. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Dieses Codebeispiel verschiebt Assets an eine bestimmte Position, die vom `assetMoveArray`. Das Array enthält den Asset-Handle und den zugehörigen Ordner-Handle. Die Antwort zeigt an, dass die Assets erfolgreich verschoben wurden.

**Anforderung**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Antwort**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

