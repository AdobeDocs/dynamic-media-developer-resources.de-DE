---
description: Bildsatzdaten. Bietet einen Mechanismus zum Definieren sortierter Bildsätze und Steuerungsattribute, die von den Scene7-Viewern verwendet werden.
seo-description: Bildsatzdaten. Bietet einen Mechanismus zum Definieren sortierter Bildsätze und Steuerungsattribute, die von den Scene7-Viewern verwendet werden.
seo-title: Bildsatz
solution: Experience Manager
title: Bildsatz
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 2%

---


# Bildsatz{#imageset}

Bildsatzdaten. Bietet einen Mechanismus zum Definieren sortierter Bildsätze und Steuerungsattribute, die von den Scene7-Viewern verwendet werden.

Ein Bildsatz besteht aus einer sortierten, kommagetrennten Liste von Elementen, bei der jedes Element aus einem oder mehreren Unterelementen (Bild-IDs, Muster-IDs, Mediendateipfade, Beschriftungen usw.) besteht, die durch Semikolons und/oder Doppelpunkte voneinander getrennt sind.

Geschachtelte Klammern `{ }` und Klammern `( )` können verwendet werden, um bestimmten Inhalt (z. B. Farbwerte) abzugrenzen oder verschachtelte Sätze anzugeben. Auf diese Weise verwendete Klammern oder Klammern dürfen nicht verschlüsselt sein und müssen immer als übereinstimmende Paare angezeigt werden. Andernfalls tritt ein Fehler bei der Kataloganalyse auf.

>[!NOTE]
>
>Die folgenden Zeichen werden als Trennzeichen verwendet und müssen HTTP-kodiert sein, wenn sie im Satz als Teil von ID- oder Zeichenfolgenwerten angezeigt werden:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Weitere Informationen zur Struktur und Verwendung von Bildsätzen finden Sie in der Dokumentation zu Image Serving Viewers.

Der Server gibt den Inhalt dieses Felds ohne Änderung als Antwort auf eine `req=imageset`-Anforderung zurück.

## Standardsätze {#section-5ecc8ffee7224668b63f601383665564}

Die folgenden Set-Definitionen werden vom Image Serving nativ unterstützt. Der Zugriff auf bestimmte Viewer umfasst das serverseitige Analysieren, Validieren und Verarbeiten des Sets. Jeder Set-Typ kann identifiziert werden, indem der entsprechende Wert in `catalog::AssetType` angegeben wird.

**Grundlegende Mustersets**

Jedes Element in einem grundlegenden Musterset besteht aus einem Verweis auf einen Bilddatensatz und einem optionalen separaten Verweis auf einen Bilddatensatz, der als Muster verwendet wird.

| ` *`basicSwatchSet`*` | ` *``*&#42;[',' *`swatchItemsSwatchItem`*]` |
|---|---|
| ` *`swatchItem`*` | ` *``*[';' *`imageIdswatch`*]` |
| ` *`Farbfeld`*` | ` *`swatchId`*|solidColorSpecifier` |
| ` *`imageId`*` | IS-Bildreferenz (Katalog/ID) |
| ` *`swatchId`*` | IS-Bildreferenz (Katalog/ID) |
| ` *`solidColorSpecifier`*` | ` '{0x' *`rrggbblabel `* [ *``*]'}'` |
| ` *`rggbb`*` | Packung mit 6-stelligem hexadezimalen RGB-Farbwert für Farbfelder mit Volltonfarbe |
| ` *`label`*` | Optionale Textbeschriftung für Farbfelder mit Volltonfarbe |

**Hierarchische Mustersets**

Jedes Element in einem hierarchischen Musterset kann aus einem einfachen Musterset oder einem Verweis auf einen Musterset-Datensatz bestehen (für solche Elemente sind Mustersets erforderlich).

| ` *`hierarchySwatchSet`*` | ` *``* &#42;[ ',' *`hierarchySwatchItemHierarchicalSwatchItem`* ]` |
|---|---|
| ` *`hierarchySwatchItem`*` | ` *``* | { *``* ';' *`swatchItemBasicSwatchSetIdswatch`* }` |
| ` *`basicSwatchSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der ein einfaches Musterset definiert |

**Grundlegende Rotationssets**

Ein einfaches Rotationsset besteht aus einer einfachen Liste von Bild-IDs.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**zweidimensionale Rotationssets**

Jedes Element in einem zweidimensionalen Rotationsset kann aus einem einfachen Bild, einem Verweis auf ein einfaches Rotationsset oder einem durch geschweifte Klammern getrennten grundlegenden Rotationsset bestehen. Klammern können anstelle von geschweiften Klammern verwendet werden.

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| ` *`basicSpinSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der ein einfaches Rotationsset definiert |

**Seitensätze**

Jedes Element in einem Seitensatz kann aus bis zu drei mit Doppelpunkten getrennten Seitenbildern bestehen.

| ` *`pageSet`*` | ` *``* &#42;[ , *`pageItemItem`* ]` |
|---|---|
| ` *`pageItem`*` | ` *``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Mediensets**

Jedes Element in einem Mediensatz kann aus einem Bild, einem einfachen Musterset, einem hierarchischen Musterset, einem einfachen Rotationsset, einem zweidimensionalen Rotationsset, einem Seitensatz oder einem Video-Asset bestehen. Jedes Medienset-Element kann auch ein optionales Muster und eine Typkennung enthalten.

| ` *`mediaSet`*` | ` *``* &#42;[ , *`item`* ]` |
|---|---|
| ` *`Element`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemRecutItemimageItemItemIDreserved`* ] ] ]` |
| ` *`videoItem`*` | ` *``* ; *`videoswatchId`*` |
| ` *`recutItem`*` | ` *``* ; *`recutswatchId`*` |
| ` *`imageItem`*` | ` *``* ; [ *`imageIdswatchId`* ]` |
| ` *`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`swatchId`*` | IS-Bild-ID |
| ` *`video`*` | Pfad der Video-/Animationsdatei oder statische Katalog-ID |
| ` *`recut`*` | XML-Dateipfad der Neuschnittanzeige oder statische Katalog-ID |
| ` *`imageId`*` | IS-Bild-ID |
| ` *`setId`*` | IS-Verweis auf Bild-, Rotationsset- oder E-Katalog-Set |
| ` *`inlineSet`*` | Inline-Bild-, Rotationsset- oder E-Katalog-Set |
| ` *`reserviert`*` | Für zukünftige Verwendung reserviert |

**Videosets**

Ein Videoset besteht aus einer einfachen Liste von Video-IDs, bei denen jede ID auf einen Eintrag im statischen Inhaltskatalog verweist.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Eigenschaften {#section-17c731e5c46646aa90ac21f39bb693ca}

Textzeichenfolge. Kommagetrennte Liste von `catalog::Id`-Werten, absoluten Image Server-Dateipfaden oder Dateipfaden relativ zu `attribute::RootPath`. Auf dasselbe Bild kann mehr als einmal im Set verwiesen werden. Der definierte Katalogdatensatz kann an jeder beliebigen Stelle im Satz erscheinen.

Dieses Feld nimmt an der lokale Anpassung der Textzeichenfolge teil. Zusätzlich zu den Zeichenfolgen für *`label`* (Teil von *`solidColorSpecifier`*) werden alle getrennten Felder lokalisiert, wenn sie mindestens ein Token für die lokale Anpassung &quot;`^loc=…^`&quot;enthalten. Weitere Informationen finden Sie unter [Textzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz*.

## Standard {#section-c3a60e360393478284f0f2d2da5b963b}

Keine.

## Siehe auch {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md),  [Objekt-ID-Übersetzung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ,  [Textzeichenzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Image Serving Viewers-Dokumentation
