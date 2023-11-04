---
title: src
description: Materialdatei. Gibt Materialdaten an, entweder in Form eines einzelnen Materialkatalogverweises oder als ein oder zwei Bild- oder Materialdatendateien, getrennt durch Kommas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 1%

---

# src{#src}

Materialdatei. Gibt Materialdaten an, entweder in Form eines einzelnen Materialkatalogverweises oder als ein oder zwei Bild- oder Materialdatendateien, getrennt durch Kommas.

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
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>Materialkatalog-ID (<span class="codeph"> attribute::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Eintrag zum Materialkatalog (<span class="codeph"> catalog::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Materialstildatei (<span class="filepath"> .vnc</span> oder <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Bilddatendatei. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Anfrage an Image Serving. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Anforderung für das Bild-Rendering. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ForeignReq</span> </p></td> 
  <td class="stentry"> <p>Anfrage an einen ausländischen Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Name eines eingebetteten Materials. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>0-basierte Indexnummer für ein eingebettetes Material. </p></td> 
 </tr> 
</table>

Wiederholbare Textur-, Decal- und Hintergrundmaterialien erfordern ein einzelnes Bild, das als Datei oder eingebettete Anforderung angegeben werden kann.

Die Kabinenmaterialien erfordern eine Kabinettsdatei ( [!DNL .vnc]), die nicht als verschachtelte Anforderung angegeben werden kann. Eine Texturbilddatei ist für Cabinets optional und kann, falls angegeben, entweder eine Datei oder eine eingebettete Anforderung sein.

Die Materialien für Fensterverkleidungen erfordern eine Stildatei für Fensterverkleidungen ( [!DNL .vnw]), die nicht als verschachtelte Anforderung angegeben werden kann. Eine Texturdatei ist optional und kann, falls angegeben, entweder eine Datei oder eine eingebettete Anforderung sein.

Beim Rendern von Bildern werden dieselben Regeln wie beim Image Serving verwendet, um nach Materialkatalogen, Katalogeinträgen und Datendateien zu suchen. Siehe Beschreibung der *`object`* Datentyp in der Image Serving-Dokumentation .

*`materialFile`* Ist ein Pfad relativ zu `attribute::RootPath`.

*`foreignReq`* Kann entweder eine URL sein, die relativ zu `attribute::RootUrl`oder eine absolute URL, wenn `attribute::AllowDirectUrls` festgelegt ist.

Wenn *`catId`* nicht angegeben ist, wird der Sitzungskatalog verwendet.

`srcE=` und `srcN=` Zugang zu den in die Vignette eingebetteten Materialien bieten.

## Unterstützte Dateiformate {#section-f2186d3eef834fc8bbecb2bc68daacad}

Das Bild-Rendering unterstützt dieselben Quellbildformate wie das Dynamic Media-Bildserving.

Anwendungen, die Bilddaten in mehreren Auflösungen erfordern, eignen sich am besten für die Verwendung des PTIFF-Multiauflösungsformats (Scene7 Pyramid TIFF). Image Serving umfasst das Dienstprogramm Image Converter (IC) , mit dem PTIFF-Bilder aus einem beliebigen unterstützten Format erstellt werden.

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Dokumentation zu Image Serving in der Beschreibung des IC-Dienstprogramms .

## Eigenschaften {#section-e68d03788d534e2184147987d51dfd0f}

Materialattribut. Erforderlich für alle Materialien mit Ausnahme der festen Farbe (nicht erlaubt für feste Farbstoffe). Bei allen Zeichenfolgen wird zwischen Groß- und Kleinschreibung unterschieden. *`index`* Muss 0 oder größer sein.

## Standard {#section-dde549c1917540dc8f9555962202da3c}

Keine.

## Beispiel {#section-675865444f8a4d35b9fc6e58b36e3438}

Ein MSS für einen gefärbten Behälter mit einer separaten wiederholbaren Textur:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Dasselbe Material kann in einem Materialkatalog enthalten sein `'cat`&#39; in record &#39; `12-3-2`&quot;:

`…&obj=cabinets&src=cat/12-3-2&…`

Eine verschachtelte Anfrage an Image Serving zum Abrufen eines Texturbilds:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Verwandte Themen {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Materialkataloge](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
