---
description: Quellobjektspezifikator. Bild-, SVG- und ICC-Profilobjekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden
solution: Experience Manager
title: Objekt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# Objekt{#object}

Quellobjektspezifikator. Bild-, SVG- und ICC-Profilobjekte können als Bildkatalogeinträge oder relative Dateipfade angegeben werden

`*`Objekt`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>Name des Bildkatalogs ( <span class="codeph"> attribute::RootId </span>) </p> </td> 
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
  <td class="stentry"> <p>kann entweder im Haupt-URL-Pfad oder in einem <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>oder <span class="codeph"> icc= </span> command </p> </td> 
 </tr> 
</table>

*`rootId`* identifiziert einen Bildkatalog. (Siehe [Bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) für Details.) Wenn *`rootId`* im URL-Pfad angegeben ist, wird dieser Katalog zum *Hauptkatalog* für diese Anfrage. Andernfalls wird der Standardkatalog als Hauptkatalog verwendet. In derselben Anforderung können mehrere verschiedene Bildkataloge verwendet werden.

Der Server geht zunächst davon aus, dass *`rootId`* wird in `src=`, `mask=`und `icc=` -Befehle und versuchen, einen Katalogeintrag im Hauptkatalog zu finden. Tatsächlich versucht der Server, die gesamte *`object`* Zeichenfolge als *`objId.`*

Wenn ein Katalogeintrag gefunden wird, wird er verwendet. Andernfalls versucht der Server als Nächstes, die *`rootId`* eines Bildkatalogs. Wenn ein Katalog identifiziert wird, wird er nach *`objId`*. Wenn und der Eintrag gefunden wird, wird er verwendet.

Andernfalls *`object`* wird als expliziter Dateipfad angenommen. Wenn in diesem Fall `attribute::FullMatch` im Hauptkatalog festgelegt ist, wird der Katalog für dieses Objekt ignoriert und stattdessen der Standardkatalog verwendet. Wenn `attribute::FullMatch` nicht festgelegt ist, wird der Hauptkatalog für die weitere Verarbeitung verwendet.

Beide *`rootId`* und *`objId`* die Groß-/Kleinschreibung beachten. *`path`* wird nur unter UNIX zwischen Groß- und Kleinschreibung unterschieden.

Wenn ein führender `/` festgelegt ist, wird anstelle des Hauptkatalogs der Standardkatalog durchsucht. Dies ist in erster Linie nützlich, wenn ein expliziter Pfad `default::RootPath` anstelle des Hauptkatalogs `attribute::RootPath`, können aber auch verwendet werden, um Zugriff auf Einträge im Standardkatalog zu erhalten, die andernfalls durch Einträge im Hauptkatalog überschrieben würden.

Siehe *Verwalten von Inhalten* im *Handbuch zur Serverkonfiguration* für Einzelheiten zur *`path`* wird in einen physischen Dateipfad übersetzt.

>[!NOTE]
>
>Komma &#39;,&#39;-Zeichen sind in *`object.`*

## Unterstützte Bilddateiformate {#section-12c85aead78e4f759856ca9ff10637d7}

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des IC-Dienstprogramms (Image Converter) .

Anwendungen, die Bilddaten in verschiedenen Auflösungen erfordern, funktionieren am besten bei der Verwendung des PTIF-Multiauflösungsformats (Dynamic Media Pyramid TIFF). Das IC-Dienstprogramm wird verwendet, um PTIF-Bilder aus einem beliebigen unterstützten Bildformat zu erstellen.

## Beispiele {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Zugriff auf ein Bild und ein ICC-Profil in zwei verschiedenen Bildkatalogen**

Bild abrufen &#39; [!DNL myImage]&quot; im Bildkatalog identifiziert als &quot; [!DNL myCatalog]&quot; und fügen Sie das ICC-Profil bei &quot; [!DNL sRGB]&#39; befindet sich im Bildkatalog &#39; [!DNL myProfiles]&quot;:

` http:// *`Server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Verwenden eines einzelnen Bildkatalogs mit Ebenen

**Erstellen Sie ein einfaches zusammengesetztes Bild, das aus drei Ebenen besteht, die alle von abgerufen werden. [!DNL myCatalog]&quot;:**

` http:// *`Server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Direkter Zugriff auf Bilddateien bei Verwendung eines Katalogs zur Bereitstellung von Attributen**

Zugriff [!DNL my/image/path/myImage.tif], wobei die standardmäßigen jpg-Attribute verwendet werden, die in konfiguriert sind. `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Verwandte Themen {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
