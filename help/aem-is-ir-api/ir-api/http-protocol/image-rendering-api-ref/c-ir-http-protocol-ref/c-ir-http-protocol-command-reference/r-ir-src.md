---
title: src
description: Materialdatei Gibt Materialdaten an, entweder in Form einer einzelnen Materialkatalogreferenz oder als eine oder zwei Bild- oder Materialdatendateien, getrennt durch ein Komma.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# src{#src}

Materialdatei Gibt Materialdaten an, entweder in Form einer einzelnen Materialkatalogreferenz oder als eine oder zwei Bild- oder Materialdatendateien, getrennt durch ein Komma.

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&lbrace;'is&lbrace;'<span class="varname"> isReq</span>'&rbrace;'&rbrace;|&lbrace;'ir&lbrace;'<span class="varname"> irReq</span>'&rbrace;'|&lbrace;'&lbrace;lbrace;'<span class="varname"> ForeignReq</span>'&rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>Materialkatalog-ID (<span class="codeph">::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Materialkatalogeintrag (<span class="codeph">::ID</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Materialstil-Datei (<span class="filepath"> .vnc</span> oder <span class="filepath"> .vnw</span>) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Bilddatendatei </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Anfrage an Image-Serving. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Anforderung zum Rendern von Bildern. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ForeignReq</span> </p></td> 
  <td class="stentry"> <p>Anfrage an einen Fremdserver. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Name</span> </p></td> 
  <td class="stentry"> <p>Name eines eingebetteten Materials. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Index</span> </p></td> 
  <td class="stentry"> <p>Indexnummer auf Basis 0 für ein eingebettetes Material. </p></td> 
 </tr> 
</table>

Wiederholbare Textur-, Abziehbild- und Tapetenmaterialien erfordern ein einzelnes Bild, das als Datei oder eingebettete Anfrage angegeben werden kann.

Schrankmaterialien erfordern eine Schrankstildatei ( [!DNL .vnc]), die nicht als verschachtelte Anfrage angegeben werden kann. Eine Texturbilddatei ist für Ablagen optional und kann, falls angegeben, entweder eine Datei oder eine eingebettete Anfrage sein.

Fensterabdeckungsmaterialien erfordern eine Formatdatei für Fensterabdeckungen ( [!DNL .vnw]), die nicht als verschachtelte Anforderung angegeben werden kann. Eine Texturdatei ist optional und kann, falls angegeben, entweder eine Datei oder eine eingebettete Anfrage sein.

Für das Rendern von Bildern werden dieselben Regeln wie für die Bildbereitstellung zum Suchen von Materialkatalogen, Katalogeinträgen und Datendateien verwendet. Weitere Informationen finden Sie in der Beschreibung des *`object`*-Datentyps in der Dokumentation zu Image-Serving.

*`materialFile`* Ist ein Pfad relativ zu `attribute::RootPath`.

*`foreignReq`* Kann entweder eine URL sein, die relativ zu `attribute::RootUrl` ist, oder eine absolute URL, wenn `attribute::AllowDirectUrls` festgelegt ist.

Wenn *`catId`* nicht angegeben ist, wird der Sitzungskatalog verwendet.

`srcE=` und `srcN=` bieten Zugriff auf in die Vignette eingebettete Materialien.

## Unterstützte Dateiformate {#section-f2186d3eef834fc8bbecb2bc68daacad}

Das Bild-Rendering unterstützt dieselben Quellbildformate wie Dynamic Media Image Serving.

Anwendungen, für die Bilddaten in mehreren Auflösungen erforderlich sind, erzielen die besten Ergebnisse, wenn das Scene7 Pyramid TIFF (PTIFF)-Multiauflösungsformat verwendet wird. Image Serving beinhaltet das Image Converter-Dienstprogramm (IC), das PTIFF-Bilder aus jedem unterstützten Format erstellt.

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des IC-Dienstprogramms in der Dokumentation zu Image-Serving .

## Eigenschaften {#section-e68d03788d534e2184147987d51dfd0f}

Materialattribut. Erforderlich für alle Materialien außer Vollfarben (nicht zulässig für Vollfarbmaterialien). Bei allen Zeichenfolgen wird zwischen Groß- und Kleinschreibung unterschieden. *`index`* muss 0 oder größer sein.

## Standard {#section-dde549c1917540dc8f9555962202da3c}

Keine.

## Beispiel {#section-675865444f8a4d35b9fc6e58b36e3438}

Eine SMS für einen farbigen Schrank mit einer separaten wiederholbaren Textur:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Dasselbe Material könnte sich in einem Materialkatalog `'cat`&#39; im Datensatz &#39; `12-3-2`&#39; befinden:

`…&obj=cabinets&src=cat/12-3-2&…`

Eine verschachtelte Anfrage an Image Serving zum Abrufen eines Texturbilds:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Verwandte Themen {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Materialkataloge](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attribute::rootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
