---
description: Ein Objekt oder Container in der Ordnerhierarchie.
solution: Experience Manager
title: Asset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 943e653a-ed30-4c75-9bad-6ef5b72f5219
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 2%

---

# Asset{#asset}

Ein Objekt oder Container in der Ordnerhierarchie.

Syntax

## Parameter {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> animatedGifInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AnimatedGifInfo</span> </td> 
   <td colname="col3"> Details zu einer animierten GIF-Datei. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Asset-Handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cabInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:CabinetInfo</span> </td> 
   <td colname="col3"> Eigenschaften für einen Kassa-Asset-Typ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> created</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum und Uhrzeit des Hochladens des Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> E-Mail-Adresse des Benutzers, der das Asset erstellt hat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cssInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:CssInfo</span> </td> 
   <td colname="col3"> Details zu einer CSS-Datei. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cuePointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excelInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Gibt den virtuellen Dateinamen zurück. Der vollständige virtuelle Dateipfad lautet <span class="codeph"> folder</span>+<span class="codeph"> fileName</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flashInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Ordner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ordner, der ein Asset enthält. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Umgang mit dem übergeordneten Ordner des Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typ:fontInfo</span> </td> 
   <td colname="col3"> Eigenschaften für ein Schrift-Asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> iccProfileInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:IccProfileInfo</span> </td> 
   <td colname="col3"> Eigenschaften für ein ICC-Profil-Asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageInfo</span> </td> 
   <td colname="col3"> Eigenschaften für ein Bild-Asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Relative URL, die eine Miniaturansicht des Assets darstellt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:JavascriptInfo</span> </td> 
   <td colname="col3"> Details zu einer JavaScript-Datei. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModified</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum und Uhrzeit der letzten Änderung des Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> E-Mail-Adresse des Benutzers, der das Asset zuletzt geändert hat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:LayerViewInfo</span> </td> 
   <td colname="col3"> Eigenschaften für ein Ebenenansichts-Asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masterVideoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:MetadataArray</span> </td> 
   <td colname="col3"> Array von Metadatenwerten, die mit dem Asset verknüpft sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Asset-Name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfSettingsInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:PdfSettingsInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines PDF-Einstellungsassets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Berechtigungen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> powerPointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Projekte</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Liste der Projektnamen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psdInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Legt eine Markierung fest, die angibt, ob ein Asset veröffentlicht werden soll oder nicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> renderSceneInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:RenderSceneInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines Rendering-Szene-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rtfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Generischer Asset-Untertyp, der Subtypwerte unterstützt (z. B. <span class="codeph"> AssetSet</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> svgInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:SvgInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines SVG-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:SwcInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines SWC-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> templateInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:TemplateInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines Vorlagen-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gibt an, ob sich ein Asset im Papierkorb oder in der Live-Umgebung befindet (Werte finden Sie unter "Papierkorb-Status"). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Asset-Typ. Werte finden Sie unter <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> Asset-Typen</a> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoCaptionInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>Eigenschaften eines Videountertitel-Assets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> <p>Eigenschaften eines Video-Assets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerPresetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ViewerPresetInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines Viewer-Vorgabe-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerSwfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ViewerSwfInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines Viewer-SWf-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vignetteInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:VignetteInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines Vignetten-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> watermarkInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:WatermarkInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines Wasserzeichen-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> windowCoveringInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:WindowCoveringInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines Fensters, das Assets abdeckt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:XmlInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines XML-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:XslInfo</span> </td> 
   <td colname="col3"> Eigenschaften eines XSL-Assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>
