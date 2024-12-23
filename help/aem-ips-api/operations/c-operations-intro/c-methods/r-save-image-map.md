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

**Eingabe (saveImageMapParam)**

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
   <td colname="col4"> Der Handle für das Unternehmen mit der Imagemap, die Sie speichern möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> AssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle für das Bild-Asset, zu dem die Imagemap gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Der Ziehgriff zur Imagemap. Erstellt eine Imagemap, falls NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Name der Imagemap, die erstellt oder gespeichert wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ShapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Auswahl der Region. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Region </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Eine kommagetrennte Liste von Punkten, die die Region definieren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Aktion </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Der <span class="codeph"> href </span> Wert, der mit der Imagemap verknüpft ist, wie in der IPS-Schnittstelle angegeben. </p> <p>Um den <span class="codeph"> href-</span>-Wert zu erhalten, klicken Sie auf das Bild in der IPS-Oberfläche, kopieren Sie die URL, fügen Sie sie in dieses Element ein und formatieren Sie dann die IPS-URL als richtige URL. Beispielsweise wird <span class="codeph"> &amp; </span> zu <span class="codeph"> &amp;amp;</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Position </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Die Reihenfolge in der Liste der Imagemaps (die Z-Achse). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> aktiviert </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (saveImageMapReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| imageMapHandle | `xsd:string` | Ja | Der Ziehgriff auf die neue oder bearbeitete Imagemap. |

## Beispiele {#section-fdac488b640f427c8aa3d549c5032851}

Dieses Codebeispiel erstellt eine neue Imagemap für ein Asset. Es verwendet einen durch eine Zeichenfolgenkonstante der Bereichsform bestimmten Formtyp und gibt einen Ziehpunkt an die neue Imagemap zurück.

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
