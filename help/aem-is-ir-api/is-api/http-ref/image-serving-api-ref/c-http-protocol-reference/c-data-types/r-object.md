---
description: Source-Objektbezeichner. Bild-, SVG- und ICC-Profilobjekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden
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

Source-Objektbezeichner. Bild-, SVG- und ICC-Profilobjekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>Name des Bildkatalogs (<span class="codeph">::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID des Bild-, SVG-, Vorlagen- oder ICC-Profildatensatzes im angegebenen, Haupt- oder Standardbildkatalog </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Pfad </span> </span> </p> </td> 
  <td class="stentry"> <p>Relativer Pfad und Name der Bild-, Masken- oder ICC-Profildatei </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Objekt </span> </span> </p> </td> 
  <td class="stentry"> <p>Kann entweder im Haupt-URL-Pfad oder in einem <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> oder <span class="codeph"> icc= </span> Befehl auftreten </p> </td> 
 </tr> 
</table>

*`rootId`* identifiziert einen Bildkatalog. (Weitere Informationen finden [ unter ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)Bildkatalog“.) Wenn *`rootId`* im URL-Pfad angegeben ist, wird dieser Katalog zum *Hauptkatalog* für diese Anfrage. Andernfalls wird der Standardkatalog als Hauptkatalog verwendet. In derselben Anfrage können mehrere verschiedene Bildkataloge verwendet werden.

Der Server geht zunächst davon aus, dass *`rootId`* in `src=`-, `mask=`- und `icc=`-Befehlen weggelassen wird, und versucht, einen Katalogeintrag im Hauptkatalog zu finden. Effektiv versucht der Server, die gesamte *`object`* als *`objId.`* zu verwenden

Wenn ein Katalogeintrag gefunden wird, wird er verwendet. Andernfalls versucht der Server als Nächstes, den *`rootId`* eines Bildkatalogs abzugleichen. Wenn ein Katalog identifiziert wird, wird nach *`objId`* gesucht. Wenn und Eintrag gefunden wird, wird er verwendet.

Andernfalls wird *`object`* als expliziter Dateipfad angenommen. Wenn `attribute::FullMatch` im Hauptkatalog festgelegt ist, wird der Katalog für dieses Objekt ignoriert und stattdessen der Standardkatalog verwendet. Wenn `attribute::FullMatch` nicht festgelegt ist, wird der Hauptkatalog für die weitere Verarbeitung verwendet.

Bei *`rootId`* und *`objId`* wird zwischen Groß- und Kleinschreibung unterschieden. *`path`* wird nur unter UNIX zwischen Groß- und Kleinschreibung unterschieden.

Wenn ein führender `/` angegeben ist, wird der Standardkatalog anstelle des Hauptkatalogs durchsucht. Dies ist in erster Linie dann nützlich, wenn ein expliziter Pfad `default::RootPath` anstelle des `attribute::RootPath` des Hauptkatalogs erfordert, kann aber auch verwendet werden, um Zugriff auf Einträge im Standardkatalog zu erhalten, die andernfalls durch Einträge im Hauptkatalog überschrieben würden.

Unter *Verwalten von Inhalten* im *Server-Konfigurationshandbuch* finden Sie Einzelheiten dazu, wie *`path`* in einen physischen Dateipfad übersetzt wird.

>[!NOTE]
>
>Komma &#39;,&#39; sind in *`object.`* nicht zulässig

## Unterstützte Bilddateiformate {#section-12c85aead78e4f759856ca9ff10637d7}

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des Dienstprogramms IC (Image Converter) .

Anwendungen, für die Bilddaten in mehreren Auflösungen erforderlich sind, erzielen die besten Ergebnisse, wenn das Dynamic Media Pyramid TIFF (PTIF)-Multiauflösungsformat verwendet wird. Das IC-Dienstprogramm wird verwendet, um PTIF-Bilder aus einem beliebigen unterstützten Bildformat zu erstellen.

## Beispiele {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Zugriff auf ein Bild und ein ICC-Profil in zwei verschiedenen Bildkatalogen**

Rufen Sie das Bild &#39; [!DNL myImage]&#39; im Bildkatalog ab, der als &#39; [!DNL myCatalog]&#39; identifiziert ist, und fügen Sie das ICC-Profil &#39; [!DNL sRGB]&#39; hinzu, das sich im Bildkatalog mit dem Namen &#39; [!DNL myProfiles]&#39; befindet:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Verwenden eines einzelnen Bildkatalogs mit Ebenen

**Erstellen Sie ein einfaches zusammengesetztes Bild, das aus drei Ebenen besteht, die alle von &quot;[!DNL myCatalog]&quot; abgerufen werden:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Direkter Zugriff auf Bilddateien, während weiterhin ein Katalog zur Bereitstellung von Attributen verwendet wird**

Greifen Sie auf [!DNL my/image/path/myImage.tif] zu, indem Sie die standardmäßigen JPG-Attribute verwenden, die in `myImageCatalog` konfiguriert sind:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Verwandte Themen {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
