---
description: Verschiebt mehrere Assets unabhängig voneinander. Dies erfolgt mithilfe des im assetMoveArray enthaltenen AssetMove-Typs. Jedes AssetMove-Feld enthält einen Zielordner.
solution: Experience Manager
title: moveAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 8%

---

# moveAssets{#moveassets}

Verschiebt mehrere Assets unabhängig voneinander. Dies erfolgt mithilfe des im assetMoveArray enthaltenen AssetMove-Typs. Jedes AssetMove-Feld enthält einen Zielordner.

Syntax

## Autorisierte Benutzertypen {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-7d47f663474b41cc83439288ac133cc5}

**Eingabe (moveAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Ziehgriff an das Unternehmen mit zu verschiebenden Assets. |
| assetMoveArray | `types:AssetMoveArray` | Ja | Ein Array zum Verschieben von Assets. Es enthält ein Asset und einen Asset-Zielordner. |

**Ausgabe (moveAssetsReturn)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Asset-Anzahl erfolgreich verschoben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anzahl der Assets, die beim Versuch, sie zu verschieben, Warnungen erzeugt haben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anzahl der Assets, die Fehler verursacht haben, als der Vorgang versucht hat, sie zu verschieben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>, die Folgendes enthalten: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Assets, der die Warnungen ausgab. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Warn-Codes </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Grund für die Warnung. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>, die Folgendes enthalten: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Assets, das die Fehler ausgelöst hat. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Fehler-Codes. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Grund für die Fehler. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Dieses Codebeispiel verschiebt Assets an einen bestimmten Speicherort, der vom `assetMoveArray` angegeben wird. Das Array enthält das Asset-Handle und das Ordner-Handle. Die Antwort zeigt an, dass die Assets erfolgreich verschoben wurden.

**Anfrage**

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
