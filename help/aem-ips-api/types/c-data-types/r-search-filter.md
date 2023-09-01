---
title: SearchFilter
description: Filter, mit denen Sie Suchkriterien definieren können, um die Suche effizienter zu gestalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b3a26966-33c9-48ca-b0ed-d05fc0e2050f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# [!DNL SearchFilter]{#searchfilter}

Filter, mit denen Sie Suchkriterien definieren können, um die Suche effizienter zu gestalten.

Syntax

## Parameter {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Ordner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Geben Sie den Ordner an, den Sie suchen möchten. Leer lassen, um das gesamte Unternehmen zu durchsuchen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Legen Sie Folgendes fest: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>: Um den benannten Ordner und alle Unterordner zu durchsuchen. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>: Um nur den benannten Ordner zu durchsuchen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typ:StringArray</span> </td> 
   <td colname="col3">Eine Liste der Asset-Typen, die bei einer Suche zurückgegeben werden sollen. Beispiel: die <span class="codeph"> image</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typ:StringArray</span> </td> 
   <td colname="col3"> Geben Sie einen Asset-Typ an, der von einer Suche ausgeschlossen werden soll. Beispielsweise das Bild. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typ:StringArray</span> </td> 
   <td colname="col3">Eine Liste der Asset-Untertypen, die bei einer Suche zurückgegeben werden sollen. Beispiel: für eine <span class="codeph"> AssetSet</span>, können Sie nach der <span class="codeph"> MediaType</span> subtype. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Eine optionale boolesche Kennzeichnung, die angibt, ob Assets ohne Untertyp zurückgegeben werden, wenn <span class="codeph"> assetSubTypeArray</span> übergeben wird. </p> <p>Wenn "true", werden nur Assets mit einem der angegebenen Untertypen zurückgegeben. </p> <p>Wenn "false", werden auch Assets ohne Untertyp zurückgegeben. </p> <p>Der Standardwert ist „false“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Legen Sie Folgendes fest: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>: Um nur Original-Assets zurückzugeben. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>: Um generierten Inhalt zurückzugeben. Beispielsweise Bilder von einer hochgeladenen PDF. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle mit dem Projekt, das Sie suchen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Angeben: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> MarkedForPublish</span> , um nur veröffentlichte Assets zurückzugeben. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> , um nur unveröffentlichte Assets zurückzugeben. </li> 
    </ul> <p>Hinweis: Lassen Sie das Feld leer, um nach <i>all</i> veröffentlichte Statustypen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Angeben: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> Alle</span> , um Assets unabhängig vom Papierkorbsstatus zurückzugeben. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span> , um "normale"Assets zurückzugeben. </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InTrash</span> , um Assets aus dem Papierkorb zurückzugeben. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
