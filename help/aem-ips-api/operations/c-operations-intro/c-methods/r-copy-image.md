---
description: Erstellt eine Kopie eines vorhandenen Bild-Assets. Die angegebenen Image-Server-Protokollbefehle werden angewendet, um die neue Kopie zu generieren
solution: Experience Manager
title: copyImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 059ebbca-2341-444b-850a-1ec9582692ec
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 12%

---

# copyImage{#copyimage}

Erstellt eine Kopie eines vorhandenen Bild-Assets. Die angegebenen Image-Server-Protokollbefehle werden angewendet, um die neue Kopie zu generieren

Syntax

## Autorisierte Benutzertypen {#section-c9fe7abb550e495f832234f845db7d6e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-bf36fcbfda6742f5b9c6b02ea27e5b9d}

**Input (copyImageParam)**

<table id="table_F6B14D4875F2424D98B8C4899B1DD867"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Das Handle für das Unternehmen, das das Bild enthält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Das Handle für das Bild-Asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> folderHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Handle in den Ordner, in den das Bild kopiert werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> name</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Name des neuen Bildes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> urlModifier</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (copyImageParam)**

<table id="table_5E4ED83047314DFABC1BFAAC76C0EAC3"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Handle zum kopierten Bild. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-c30a4017001146e7befbbfc5ffcb7593}

Der Beispielcode kopiert ein Bild, das nach Unternehmen, Asset, Ordner-Handle und Name angegeben ist.

**Anfrage**

```java
<copyImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>Copy_macbookwin1</name>
   <urlModifier/>
</copyImageParam>
```

**Antwort**

```java
<copyImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|943|1|580</assetHandle>
</copyImageReturn>
```
