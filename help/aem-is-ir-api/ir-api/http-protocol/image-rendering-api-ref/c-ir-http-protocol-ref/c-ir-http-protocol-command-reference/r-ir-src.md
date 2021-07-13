---
description: Materialdatei. Gibt Materialdaten an, entweder in Form eines einzelnen Materialkatalogverweises oder als ein oder zwei Bild- oder Materialdatendateien, getrennt durch Kommas.
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 2%

---

# src{#src}

Materialdatei. Gibt Materialdaten an, entweder in Form eines einzelnen Materialkatalogverweises oder als ein oder zwei Bild- oder Materialdatendateien, getrennt durch Kommas.

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileEmbeddedReqmaterialFile`*]`

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
  <td class="stentry"> <p>Materialkatalog-ID (<span class="codeph"> Attribut::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Materialkatalogeintrag (<span class="codeph"> Katalog::Id</span>). </p></td> 
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

Kabinettmaterialien erfordern eine Kabinettstil-Datei ( [!DNL .vnc]), die nicht als verschachtelte Anforderung angegeben werden kann. Eine Texturbilddatei ist für Cabinets optional und kann, falls angegeben, entweder eine Datei oder eine eingebettete Anforderung sein.

Materialien für Fensterbeläge erfordern eine Stildatei für Fensterbeläge ( [!DNL .vnw]), die nicht als verschachtelte Anforderung angegeben werden kann. Eine Texturdatei ist optional und kann, falls angegeben, entweder eine Datei oder eine eingebettete Anforderung sein.

Beim Rendern von Bildern werden dieselben Regeln wie beim Image Serving verwendet, um nach Materialkatalogen, Katalogeinträgen und Datendateien zu suchen. Weitere Informationen finden Sie in der Beschreibung des Datentyps *`object`* in der Image Serving-Dokumentation.

*`materialFile`* ist ein Pfad relativ zu  `attribute::RootPath`.

*`foreignReq`* kann entweder eine URL relativ zu  `attribute::RootUrl`sein oder eine absolute URL, wenn festgelegt  `attribute::AllowDirectUrls` ist.

Wenn *`catId`* nicht angegeben ist, wird der Sitzungskatalog verwendet.

`srcE=` und  `srcN=` bieten Zugriff auf die in die Vignette eingebetteten Materialien.

## Unterstützte Dateiformate {#section-f2186d3eef834fc8bbecb2bc68daacad}

Das Bild-Rendering unterstützt dieselben Quellbildformate wie das Dynamic Media-Bildserving.

Anwendungen, die Bilddaten in mehreren verschiedenen Auflösungen erfordern, funktionieren am besten, wenn das Scene7 Pyramid TIFF (PTIFF)-Multiauflösungsformat verwendet wird. Image Serving umfasst das Dienstprogramm Image Converter (IC) , mit dem PTIFF-Bilder aus einem beliebigen unterstützten Format erstellt werden.

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Dokumentation zu Image Serving in der Beschreibung des IC-Dienstprogramms .

## Eigenschaften {#section-e68d03788d534e2184147987d51dfd0f}

Materialattribut. Erforderlich für alle Materialien mit Ausnahme der festen Farbe (nicht erlaubt für feste Farbstoffe). Bei allen Zeichenfolgen wird zwischen Groß- und Kleinschreibung unterschieden. *`index`* muss 0 oder größer sein.

## Standard {#section-dde549c1917540dc8f9555962202da3c}

Keine.

## Beispiel {#section-675865444f8a4d35b9fc6e58b36e3438}

MSS für einen gefärbten Schrank mit einer separaten wiederholbaren Textur:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Das gleiche Material kann in einem Materialkatalog `'cat` in Datensatz &#39; `12-3-2`&#39; gefunden werden:

`…&obj=cabinets&src=cat/12-3-2&…`

Eine verschachtelte Anfrage an Image Serving zum Abrufen eines Texturbilds:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Verwandte Themen {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Materialkataloge](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2),  [Attribut::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402),  [Attribut::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
