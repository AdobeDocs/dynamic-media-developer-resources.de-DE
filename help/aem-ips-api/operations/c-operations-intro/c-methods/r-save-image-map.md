---
description: Erstellen Sie eine neue Imagemap oder bearbeiten Sie eine vorhandene Zuordnung.
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 8%

---

# saveImageMap{#saveimagemap}

Erstellen Sie eine neue Imagemap oder bearbeiten Sie eine vorhandene Zuordnung.

Syntax

## Autorisierte Benutzertypen {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Asset haben.

## Parameter {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Input (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col4"> Das Handle für das Unternehmen mit der Imagemap, die Sie speichern möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle des Bild-Assets, zu dem die Imagemap gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Das Handle zur Imagemap. Erstellt eine Imagemap mit NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Name der erstellten oder gespeicherten Imagemap. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Auswahl der Regionsform. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> region </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Eine kommagetrennte Liste von Punkten, die den Bereich definieren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Aktion </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Der <span class="codeph"> href </span> -Wert, der der Imagemap zugeordnet ist, wie in der IPS-Oberfläche angegeben. </p> <p>Um den Wert <span class="codeph"> href </span> zu erhalten, klicken Sie auf das Bild in der IPS-Oberfläche, kopieren Sie die URL und fügen Sie sie in dieses Element ein und formatieren Sie dann die IPS-URL als ordnungsgemäße URL. Beispiel: <span class="codeph"> &amp; </span> wird zu <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Die Reihenfolge in der Liste der Imagemaps (Z-Achse). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enabled </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| imageMapHandle | `xsd:string` | Ja | Das Handle zur neuen oder bearbeiteten Imagemap. |

## Beispiele {#section-fdac488b640f427c8aa3d549c5032851}

In diesem Codebeispiel wird eine neue Imagemap für ein Asset erstellt. Es wird ein durch eine Regions-Form-String-Konstante bestimmter Formtyp verwendet und ein Handle an die neue Imagemap zurückgegeben.

**Anfrage**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Antwort**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```
