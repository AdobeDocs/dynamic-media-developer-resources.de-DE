---
description: Legt die Liste der mit einem Bildsatz verknüpften Assets fest.
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic, SDK/API, Bildsätze
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setImageSetMembers{#setimagesetmembers}

Legt die Liste der mit einem Bildsatz verknüpften Assets fest.

Dieser Vorgang ignoriert den Parameter `pageReset` für `ImageSets` und `SpinSets` und erzwingt den Wert auf true.

## Autorisierte Benutzertypen {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Bildsatz-Asset und Lesezugriff auf die einzelnen Member-Assets haben.

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
   <td colname="col4"> <p>Firma Handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Bildsatz-Handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Array von Asset-Mitgliedern, die zum Bildsatz gehören. </td> 
  </tr> 
 </tbody> 
</table>

**Output (setImageSetMembersReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-7b87219034464aa98524178ccee27738}

Dieses Codebeispiel verwendet ein Member-Array, um die Mitglieder eines Bildsatzes festzulegen.

**Anforderung**

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
