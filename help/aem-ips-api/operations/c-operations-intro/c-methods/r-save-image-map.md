---
description: Erstellen Sie eine neue Imagemap oder bearbeiten Sie eine vorhandene Map.
seo-description: Erstellen Sie eine neue Imagemap oder bearbeiten Sie eine vorhandene Map.
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
topic: Scene7 Image Production System API
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageMap{#saveimagemap}

Erstellen Sie eine neue Imagemap oder bearbeiten Sie eine vorhandene Map.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Griff zur Firma mit der Imagemap, die Sie speichern möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle des Bild-Assets, zu dem die Imagemap gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Der Griff zur Imagemap. Erstellt eine Imagemap mit NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Name der Imagemap, die erstellt oder gespeichert wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> formType </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Auswahl der Regionsform. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Region </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Eine kommagetrennte Liste von Punkten, die den Bereich definieren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Maßnahmen </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Der <span class="codeph"> href- </span> Wert, der mit der Imagemap wie in der IPS-Schnittstelle angegeben verknüpft ist. </p> <p>Um den <span class="codeph"> href- </span> Wert abzurufen, klicken Sie auf das Bild in der IPS-Oberfläche, kopieren Sie die URL in dieses Element und formatieren Sie dann die IPS-URL als geeignete URL. Beispiel: <span class="codeph"> &amp; </span> wird <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Position </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Die Reihenfolge in der Liste der Imagemaps (Z-Achse). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> aktiviert </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Ja | Der Griff zur neuen oder bearbeiteten Imagemap. |

## Beispiele {#section-fdac488b640f427c8aa3d549c5032851}

In diesem Codebeispiel wird eine neue Imagemap für ein Asset erstellt. Es wird ein durch eine Regions-Form-String-Konstante definierter Formtyp verwendet und gibt einen Griff an die neue Imagemap zurück.

**Anforderung**

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

