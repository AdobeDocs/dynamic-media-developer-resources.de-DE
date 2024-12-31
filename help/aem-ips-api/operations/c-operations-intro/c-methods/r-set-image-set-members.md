---
description: Legt die Liste der mit einem Bildset verknüpften Assets fest.
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 8%

---

# setImageSetMembers{#setimagesetmembers}

Legt die Liste der mit einem Bildset verknüpften Assets fest.

Dieser Vorgang ignoriert den `pageReset` Parameter für `ImageSets` und `SpinSets` und erzwingt den Wert auf „true“.

## Autorisierte Benutzertypen {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Bildset-Asset und Lesezugriff auf jedes Mitglied-Asset haben.

## Parameter {#section-2f46efcd24c648aeacba738509426e46}

**Input (setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Firmengriff. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> AssetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Bildset-Handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Array von Asset-Mitgliedern, die zum Bildset gehören. </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (setImageSetMembersReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-7b87219034464aa98524178ccee27738}

In diesem Codebeispiel wird ein Member-Array verwendet, um die Member eines Bildsets festzulegen.

**Anfrage**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Antwort**

Keine.
