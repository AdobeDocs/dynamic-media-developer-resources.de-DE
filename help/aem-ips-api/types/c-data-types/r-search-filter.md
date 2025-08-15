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
   <td colname="col3"> Geben Sie den Ordner an, nach dem Sie suchen möchten. Lassen Sie das Feld leer, um das gesamte Unternehmen zu durchsuchen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3">Legen Sie auf fest: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>: Zum Durchsuchen des angegebenen Ordners und aller Unterordner. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>: Nur den angegebenen Ordner durchsuchen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3">Eine Liste der Asset-Typen, die Sie bei einer Suche zurückgeben möchten. Zum Beispiel das <span class="codeph"> Bild</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Geben Sie einen Asset-Typ an, der von einer Suche ausgeschlossen werden soll. Zum Beispiel das Bild . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3">Eine Liste der Asset-Untertypen, die bei einer Suche zurückgegeben werden sollen. Beispielsweise können Sie für ein <span class="codeph"> AssetSet</span> nach dem <span class="codeph"> MediaType</span>-Untertyp suchen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> rictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Ein optionales boolesches Flag, das angibt, ob Assets ohne Untertyp zurückgegeben werden sollen, wenn <span class="codeph"> assetSubTypeArray</span> übergeben wird. </p> <p>Wenn „true“, werden nur Assets mit einem der angegebenen Untertypen zurückgegeben. </p> <p>Bei „false“ werden auch Assets ohne Untertyp zurückgegeben. </p> <p>Der Standardwert ist „false“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3">Legen Sie auf fest: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>: Gibt nur Original-Assets zurück. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>: Gibt den generierten Inhalt zurück. Beispielsweise Bilder aus einer hochgeladenen PDF. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Verarbeiten Sie das Projekt, das Sie suchen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Geben Sie Folgendes an: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> MarkedForPublish: </span> nur veröffentlichte Assets zurückzugeben. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span>, um nur unveröffentlichte Assets zurückzugeben. </li> 
    </ul> <p>Hinweis: Lassen Sie das Feld leer, um nach <i>allen</i> veröffentlichten Statustypen zu suchen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Geben Sie Folgendes an: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> Beliebig</span> um Assets unabhängig von ihrem Papierkorb-Status zurückzugeben. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span> gibt „normale“ Assets zurück. </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InTrash</span>, um Assets aus dem Papierkorb zurückzugeben. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
