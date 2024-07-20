---
description: Source-Objektspezifikator. Bild-, SVG- und ICC-Profilobjekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden
solution: Experience Manager
title: Objekt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# Objekt{#object}

Source-Objektspezifikator. Bild-, SVG- und ICC-Profilobjekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>Name des Bildkatalogs ( <span class="codeph"> Attribut::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID des Bild-, SVG-, Vorlagen- oder ICC-Profildatensatzes im angegebenen, Haupt- oder Standardbildkatalog </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>Pfad und Name der relativen Bild-, Maske- oder ICC-Profildatei </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Objekt </span> </span> </p> </td> 
  <td class="stentry"> <p>kann entweder im Haupt-URL-Pfad oder in einem Befehl <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> oder <span class="codeph"> icc= </span> auftreten </p> </td> 
 </tr> 
</table>

*`rootId`* gibt einen Bildkatalog an. (Weitere Informationen finden Sie unter [Bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3).) Wenn im URL-Pfad *`rootId`* angegeben ist, wird dieser Katalog zum *Hauptkatalog* für diese Anforderung. Andernfalls wird der Standardkatalog als Hauptkatalog verwendet. In derselben Anforderung können mehrere verschiedene Bildkataloge verwendet werden.

Der Server geht zunächst davon aus, dass *`rootId`* in den Befehlen `src=`, `mask=` und `icc=` weggelassen wird, und versucht, einen Katalogeintrag im Hauptkatalog zu finden. Im Grunde versucht der Server, die gesamte *`object`* -Zeichenfolge als *`objId.`* zu verwenden

Wenn ein Katalogeintrag gefunden wird, wird er verwendet. Andernfalls versucht der Server, mit dem *`rootId`* eines Bildkatalogs abzugleichen. Wenn ein Katalog identifiziert wird, wird er nach *`objId`* gesucht. Wenn und der Eintrag gefunden wird, wird er verwendet.

Andernfalls wird *`object`* als expliziter Dateipfad angenommen. Wenn in diesem Fall `attribute::FullMatch` im Hauptkatalog festgelegt ist, wird der Katalog für dieses Objekt ignoriert und stattdessen der Standardkatalog verwendet. Wenn `attribute::FullMatch` nicht festgelegt ist, wird der Hauptkatalog für die weitere Verarbeitung verwendet.

Sowohl *`rootId`* als auch *`objId`* beachten die Groß-/Kleinschreibung. Bei *`path`* wird nur unter UNIX zwischen Groß- und Kleinschreibung unterschieden.

Wenn eine vorangestellte `/` angegeben wird, wird der Standardkatalog anstelle des Hauptkatalogs durchsucht. Dies ist in erster Linie nützlich, wenn ein expliziter Pfad &quot;`default::RootPath`&quot; anstelle der &quot;`attribute::RootPath`&quot; des Hauptkatalogs erfordert, aber auch verwendet werden kann, um Zugriff auf Einträge im Standardkatalog zu erhalten, die andernfalls durch Einträge im Hauptkatalog überschrieben würden.

Weitere Informationen dazu, wie *`path`* in einen physischen Dateipfad übersetzt wird, finden Sie unter *Verwalten von Inhalten* im *Server Configuration Guide* .

>[!NOTE]
>
>Komma &#39;,&#39;-Zeichen sind in *`object.`* nicht zulässig

## Unterstützte Bilddateiformate {#section-12c85aead78e4f759856ca9ff10637d7}

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des IC-Dienstprogramms (Image Converter) .

Anwendungen, die Bilddaten in mehreren Auflösungen erfordern, eignen sich am besten für die Verwendung des PTIF-Multiauflösungsformats (Dynamic Media Pyramid TIFF). Das IC-Dienstprogramm wird verwendet, um PTIF-Bilder aus einem beliebigen unterstützten Bildformat zu erstellen.

## Beispiele {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Zugreifen auf ein Bild und ein ICC-Profil in zwei verschiedenen Bildkatalogen**

Rufen Sie das Bild &quot;[!DNL myImage]&quot; im Bildkatalog mit der Bezeichnung &quot;[!DNL myCatalog]&quot; ab und fügen Sie das ICC-Profil &quot;[!DNL sRGB]&quot; im Bildkatalog mit der Bezeichnung &quot;[!DNL myProfiles]&quot; bei:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Verwenden eines einzelnen Bildkatalogs mit Ebenen

**Erstellen Sie ein einfaches zusammengesetztes Bild, das aus drei Ebenen besteht, die alle aus &quot;[!DNL myCatalog]&quot; abgerufen werden:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Direkter Zugriff auf Bilddateien bei Verwendung eines Katalogs zur Bereitstellung von Attributen**

Greifen Sie mithilfe der in `myImageCatalog` konfigurierten standardmäßigen jpg-Attribute auf [!DNL my/image/path/myImage.tif] zu:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Verwandte Themen {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
