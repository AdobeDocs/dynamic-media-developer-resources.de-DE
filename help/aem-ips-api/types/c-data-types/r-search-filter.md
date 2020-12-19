---
description: Filter, die Ihnen helfen, Suchkriterien zu definieren, um Suchvorgänge effizienter zu gestalten.
seo-description: Filter, die Ihnen helfen, Suchkriterien zu definieren, um Suchvorgänge effizienter zu gestalten.
seo-title: SearchFilter
solution: Experience Manager
title: SearchFilter
topic: Scene7 Image Production System API
uuid: 85a434d3-51a5-4e68-901e-70585c0e8b20
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# SearchFilter{#searchfilter}

Filter, die Ihnen helfen, Suchkriterien zu definieren, um Suchvorgänge effizienter zu gestalten.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> folder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Geben Sie den Ordner an, den Sie suchen möchten. Lassen Sie das Feld leer, um die gesamte Firma zu durchsuchen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Auf: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>: Zum Durchsuchen des benannten Ordners und aller Unterordner. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> FALSE</span>: Zum Durchsuchen des benannten Ordners. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Eine Liste von Asset-Typen, die bei einer Suche zurückgegeben werden sollen. Beispiel: <span class="codeph"> image</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> Geben Sie einen Asset-Typ an, der von einer Suche ausgeschlossen werden soll. Beispiel: Bild. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Eine Liste von Asset-Untertypen, die bei einer Suche zurückgegeben werden sollen. Beispiel: Für einen <span class="codeph">-AssetSet</span> können Sie nach dem Untertyp <span class="codeph"> MediaType</span> suchen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> striktSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Ein optionales boolesches Flag, das angibt, ob Assets ohne Subtyp zurückgegeben werden sollen, wenn <span class="codeph"> assetSubTypeArray</span> übergeben wird. </p> <p>Wenn "true", werden nur Assets mit einem der angegebenen Untertypen zurückgegeben. </p> <p>Wenn "false", werden auch Assets ohne Subtyp zurückgegeben. </p> <p>Die Standardeinstellung ist "false". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Auf: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>: So geben Sie nur Originalelemente zurück. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> FALSE</span>: So geben Sie generierten Inhalt zurück. Zum Beispiel Bilder aus einer hochgeladenen PDF. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Behandeln Sie das zu suchende Projekt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Angeben: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> "</span> MarkedForPublishing", um nur veröffentlichte Assets zurückzugeben. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> </span> NotMarkedForPublishingDamit werden nur unveröffentlichte Assets zurückgegeben. </li> 
    </ul> <p>Hinweis: Lassen Sie das Feld leer, um nach <i>allen</i> veröffentlichten Statustypen zu suchen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Angeben: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> Alles, </span> das Assets unabhängig vom Papierkorbsstatus zurückgibt. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> "</span> NotInTrashto"gibt "normale"Assets zurück. </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> In</span> Papierkorb, um Assets aus dem Papierkorb zurückzugeben. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

