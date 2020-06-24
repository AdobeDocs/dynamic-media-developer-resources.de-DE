---
description: Auftragstyp, um den autorisierten Export bereits hochgeladener Dateien zu ermöglichen.
seo-description: Auftragstyp, um den autorisierten Export bereits hochgeladener Dateien zu ermöglichen.
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 10%

---


# ExportJob{#exportjob}

Auftragstyp, um den autorisierten Export bereits hochgeladener Dateien zu ermöglichen.

ExportJob unterstützt die folgenden Asset-Typen nicht:

* Bildsets
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Typen:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Liste von <span class="codeph"> assetHandle</span> , die exportiert werden müssen. Siehe <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Gibt den <span class="codeph"> Exporttyp an.Mögliche Werte</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Wenn <span class="codeph"> "fmt=orig</span>"festgelegt ist, werden die Assets als Original exportiert </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Wenn <span class="codeph"> fmt=convert</span>, werden die Assets in das Format konvertiert, das in den Eingabeparametern <span class="codeph"> is_modifer</span> oder <span class="codeph"> macro</span> angegeben ist. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Gibt die URL-Zeichenfolge zum Rendern von <span class="codeph"> ImageServer</span> an, die an die ExportJob- <span class="codeph"> Konvertierungsanforderung</span> angehängt wird. </p> <p>Einzelheiten zum Senden der IS-Modifikatoren finden Sie in der <a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> IS-Dokumentation</a> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Auswahl der E-Mail-Einstellung. Mögliche Werte: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> All</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Fehler</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> Keine</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Gibt die IP-Adresse des Kunden oder Kunden an, der die Exportanforderung initiiert hat. </p> <p> <p>Hinweis:  Dieser Parameter wird derzeit nicht aktiv ausgefüllt und ist ausschließlich für die zukünftige Verwendung reserviert. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bei ExportJob-Anforderungen, bei denen `fmt=convert` und sowohl `is_modifier` als auch `macro` bereitgestellt werden, respektiert die Zieldatei das von `macro`angegebene Format. Beispiel:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

