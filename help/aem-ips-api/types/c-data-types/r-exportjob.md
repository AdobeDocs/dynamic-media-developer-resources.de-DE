---
description: Vorgangstyp, um den autorisierten Export zuvor hochgeladener Dateien zu ermöglichen.
solution: Experience Manager
title: Exportvorgang
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# [!DNL ExportJob]{#exportjob}

Vorgangstyp, um den autorisierten Export zuvor hochgeladener Dateien zu ermöglichen.

ExportJob unterstützt nicht die folgenden Asset-Typen:

* Bildsätze
* Rendersets
* Rotationssets
* Mediensets
* Sets mit mehreren Bitraten
* Videosets
* E-Kataloge
* Angebotssets

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Liste <span class="codeph"> AssetHandle</span>, die exportiert werden müssen. Siehe <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL fmt]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Gibt den Typ des <span class="codeph">-Exports an.Mögliche Werte</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Wenn <span class="codeph"> fmt=</span>ist, werden die Assets als Original exportiert </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Wenn <span class="codeph">fmt=convert</span> werden die Assets in das Format konvertiert, das in den <span class="codeph">-Eingabeparametern </span>_modifier oder <span class="codeph"> Makro angegeben </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL is_modifier]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Gibt die Rendering</span>URL-Zeichenfolge des <span class="codeph"> ImageServer an, die an die Anfrage „ExportJob <span class="codeph"> convert</span> angehängt wird. </p> <p>Einzelheiten zum Senden der <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/homeisir.html?lang=de" scope="external" format="html">-Modifikatoren finden </a> in der Dokumentation zu IIS. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL macro]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Auswahl der E-Mail-Einstellung. Mögliche Werte: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> Alle <span class="codeph"></span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Fehler</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> errorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> keine</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL clientId]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Gibt die IP-Adresse des Kunden oder Kunden an, der die Exportanfrage initiiert hat. </p> <p> <p>Hinweis: Dieser Parameter wird derzeit nicht aktiv verwendet und ist ausschließlich für die zukünftige Verwendung reserviert. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bei ExportJob-Anfragen, bei denen `fmt=convert` und sowohl `is_modifier` als auch `macro` angegeben werden, respektiert die Zieldatei das von `macro` bereitgestellte Format. Beispiel:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
