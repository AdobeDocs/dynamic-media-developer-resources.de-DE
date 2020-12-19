---
description: Quellenobjektbezeichner. Bild-, SVG- und ICC-Profil-Objekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden.
seo-description: Quellenobjektbezeichner. Bild-, SVG- und ICC-Profil-Objekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden.
seo-title: Objekt
solution: Experience Manager
title: Objekt
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 1%

---


# Objekt{#object}

Quellenobjektbezeichner. Bild-, SVG- und ICC-Profil-Objekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden.

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Name des Bildkatalogs ( <span class="codeph"> Attribut::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID des Image-, SVG-, Vorlagen- oder ICC-Profil-Datensatzes im angegebenen, Haupt- oder Standardbildkatalog </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>Pfad und Name der relativen Bild-, Maske- oder ICC-Profil-Datei </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>kann entweder im Haupt-URL-Pfad oder in einem <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> oder <span class="codeph"> icc= </span>-Befehl auftreten </p> </td> 
 </tr> 
</table>

*`rootId`* identifiziert einen Bildkatalog. (Weitere Informationen finden Sie unter [Bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3).) Wenn *`rootId`* im URL-Pfad angegeben ist, wird dieser Katalog zum *Hauptkatalog* für diese Anforderung. Andernfalls wird der Standardkatalog als Hauptkatalog verwendet. In derselben Anforderung können mehrere verschiedene Bildkataloge verwendet werden.

Der Server nimmt zunächst an, dass *`rootId`* in den Befehlen `src=`, `mask=` und `icc=` ausgelassen wird, und versucht, einen Katalogeintrag im Hauptkatalog zu finden. Im Grunde versucht der Server, die gesamte *`object`*-Zeichenfolge als *`objId.`* zu verwenden.

Wenn ein Katalogeintrag gefunden wird, wird er verwendet; Andernfalls versucht der Server, dem *`rootId`* eines Bildkatalogs zu entsprechen. Wenn ein Katalog identifiziert wird, wird er nach *`objId`* gesucht. Wenn und Eintrag gefunden wird, wird sie verwendet.

Andernfalls wird angenommen, dass *`object`* ein expliziter Dateipfad ist. Wenn `attribute::FullMatch` in diesem Fall im Hauptkatalog eingestellt ist, wird der Katalog für dieses Objekt ignoriert und stattdessen der Standardkatalog verwendet. Wenn `attribute::FullMatch` nicht eingestellt ist, wird der Hauptkatalog für die weitere Verarbeitung verwendet.

Bei *`rootId`* und *`objId`* wird die Groß-/Kleinschreibung beachtet. *`path`* ist nur unter UNIX auf die Groß- und Kleinschreibung zu achten.

Wenn ein führendes &quot;/&quot;angegeben ist, wird der Standardkatalog anstelle des Hauptkatalogs durchsucht. Dies ist vor allem dann nützlich, wenn ein expliziter Pfad `default::RootPath` anstelle des `attribute::RootPath`-Katalogs des Hauptkatalogs benötigt, kann aber auch verwendet werden, um Zugriff auf Einträge im Standardkatalog zu erhalten, die sonst durch Einträge im Hauptkatalog außer Kraft gesetzt würden.

Weitere Informationen dazu, wie *`path`* in einen physischen Dateipfad übersetzt wird, finden Sie unter *Verwalten von Inhalten* im *Serverkonfigurationshandbuch*.

>[!NOTE]
>
>Komma &#39;,&#39; Zeichen sind in *`object.`* nicht zulässig

## Unterstützte Bilddateiformate {#section-12c85aead78e4f759856ca9ff10637d7}

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des IC-Dienstprogramms (Image Converter).

Anwendungen, bei denen Bilddaten in verschiedenen Auflösungen benötigt werden, funktionieren am besten, wenn das Scene7 Pyramid TIFF (PTIF)-Format mit mehreren Auflösungen verwendet wird. Das IC-Dienstprogramm wird zum Erstellen von PTIF-Bildern aus jedem unterstützten Bildformat verwendet.

## Beispiele {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Zugriff auf ein Bild und ein ICC-Profil in zwei verschiedenen Bildkatalogen**

Rufen Sie das Bild &#39; [!DNL myImage]&#39; im Bildkatalog mit der Bezeichnung &#39; [!DNL myCatalog]&#39; ab und fügen Sie das ICC-Profil &#39; [!DNL sRGB]&#39; im Bildkatalog &#39; [!DNL myProfiles]&#39; an:

` http:// *`Server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Verwenden eines einzelnen Bildkatalogs mit Ebenen

**Erstellen Sie ein einfaches Composite-Bild, das aus drei Ebenen besteht, die alle aus &#39;  [!DNL myCatalog]&#39; abgerufen werden:**

` http:// *`Server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Direkter Zugriff auf Bilddateien, während weiterhin ein Katalog zur Bereitstellung von Attributen verwendet wird**

Greifen Sie mithilfe der standardmäßigen jpg-Attribute, die in `myImageCatalog` konfiguriert sind, auf [!DNL my/image/path/myImage.tif] zu:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Verwandte Themen {#section-b6eccefad63f441d922699c4aba58fc9}

[IC-Dienstprogramm](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
