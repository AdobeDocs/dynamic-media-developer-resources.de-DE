---
description: Bildsatzdaten. Bietet einen Mechanismus zum Definieren sortierter Bildsätze und von den Dynamic Media-Viewern verwendete Steuerelementattribute.
solution: Experience Manager
title: Bildsatz
feature: Dynamic Media Classic,SDK/API,Bildsets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 2%

---

# Bildsatz{#imageset}

Bildsatzdaten. Bietet einen Mechanismus zum Definieren sortierter Bildsätze und von den Dynamic Media-Viewern verwendete Steuerelementattribute.

Ein Bildset besteht aus einer sortierten, kommagetrennten Liste von Elementen, wobei jedes Element aus einem oder mehreren Unterelementen (Bild-IDs, Muster-IDs, Mediendateipfade, Beschriftungen usw.) besteht, die durch Semikolons und/oder Doppelpunkte voneinander getrennt sind.

Geschachtelte Klammern `{ }` und Klammern `( )` können verwendet werden, um bestimmte Inhalte (z. B. Farbwerte) zu trennen oder verschachtelte Sets anzugeben. Auf diese Weise verwendete Klammern oder Klammern dürfen nicht codiert sein und müssen immer als übereinstimmende Paare angezeigt werden. Andernfalls tritt ein Katalogparsing-Fehler auf.

>[!NOTE]
>
>Die folgenden Zeichen werden als feste Trennzeichen verwendet und müssen HTTP-kodiert sein, wenn sie im Satz als Teil von ID- oder Zeichenfolgenwerten angezeigt werden:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Weitere Informationen zur Struktur und Verwendung von Bildsets finden Sie in der Dokumentation zu Image Serving Viewers .

Der Server gibt den Inhalt dieses Felds ohne Änderung als Antwort auf eine `req=imageset`-Anfrage zurück.

## Standardsätze {#section-5ecc8ffee7224668b63f601383665564}

Die folgenden Definitionen werden nativ vom Image Serving unterstützt. Der Zugriff auf bestimmte Viewer umfasst das serverseitige Parsen, Validieren und Verarbeiten des Sets. Jeder Set-Typ kann identifiziert werden, indem der entsprechende Wert in `catalog::AssetType` angegeben wird.

**Grundlegende Mustersets**

Jedes Element in einem grundlegenden Musterset besteht aus einem Verweis auf einen Bilddatensatz und einem optionalen separaten Verweis auf einen Bilddatensatz, der als Muster verwendet wird.

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemsSwatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIDSwatch`*]` |
| `*`Musterabschnitt`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS-Bildreferenz (Katalog/ID) |
| `*`swatchId`*` | IS-Bildreferenz (Katalog/ID) |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rggbblabel`*]'}'` |
| `*`rgbb`*` | 6-stelliger hexadezimaler RGB-Farbwert für Farbmuster mit durchgehender Farbtiefe |
| `*`label`*` | Optionale Textbeschriftung für Farbmuster mit Volltonfarbe |

**Hierarchische Mustersets**

Jedes Element in einem hierarchischen Musterset kann aus einem einfachen Musterelement oder einem Verweis auf einen Musterset-Datensatz bestehen (für solche Elemente sind Muster erforderlich).

| `*`hierarchicalSwatchSet`*` | `*``* &#42;[ ',' *`hierarchicalSwatchItemHierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*``* | { *``* ';' *`swatchItemBasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der ein einfaches Musterset definiert |

**Einfache Rotationssets**

Ein einfaches Rotationsset besteht aus einer einfachen Liste von Bild-IDs.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Zweidimensionale Rotationssets**

Jedes Element in einem zweidimensionalen Rotationsset kann aus einem einfachen Bild, einem Verweis auf ein einfaches Rotationsset oder einem durch geschweifte Klammern getrennten einfachen Inline-Rotationsset bestehen. Klammern können anstelle von geschweiften Klammern verwendet werden.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der ein einfaches Rotationsset definiert |

**Seitensätze**

Jedes Element in einem Seitensatz kann aus bis zu drei Seitenbildern bestehen, die durch Doppelpunkte voneinander getrennt sind.

| `*`pageSet`*` | `*``* &#42;[ , *`pageItemPageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageImageImageImageId`* ] ]` |

**Mediensets**

Jedes Element in einem Medienset kann aus einem Bild, einem einfachen Musterset, einem hierarchischen Musterset, einem einfachen Rotationsset, einem zweidimensionalen Rotationsset, einem Seitensatz oder einem Video-Asset bestehen. Jedes Medienset-Element kann auch ein optionales Muster und eine Typkennung enthalten.

| `*`mediaSet`*` | `*``* &#42;[ , *`item`* ]` |
|---|---|
| `*`Element`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemRecutImageItemItemItemItemIDpreserve`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS-Bild-ID |
| `*`Video`*` | Pfad der Video-/Animationsdatei oder statische Katalogkennung |
| `*`recut`*` | XML-Dateipfad der Neudefinition oder statische Katalogkennung |
| `*`imageId`*` | IS-Bild-ID |
| `*`setId`*` | IS-Verweis auf Bild-, Rotations- oder E-Katalog-Set |
| `*`inlineSet`*` | eingebettetes Bild, Rotationsset oder E-Katalog |
| `*`reserviert`*` | Reserviert für zukünftige Verwendung |

**Videosets**

Ein Videoset besteht aus einer einfachen Liste von Video-IDs, bei denen jede ID auf einen Eintrag im statischen Inhaltskatalog verweist.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Eigenschaften {#section-17c731e5c46646aa90ac21f39bb693ca}

Textzeichenfolge. Kommagetrennte Liste von `catalog::Id`-Werten, absoluten Image Server-Dateipfaden oder Dateipfaden relativ zu `attribute::RootPath`. Auf dasselbe Bild kann mehr als einmal im Set verwiesen werden. Der definierte Katalogdatensatz kann in der Gruppe an jedem beliebigen Speicherort angezeigt werden.

Dieses Feld nimmt an der Lokalisierung von Textzeichenfolgen teil. Neben den Zeichenfolgen *`label`* (Teil von *`solidColorSpecifier`*) werden alle getrennten Felder lokalisiert, wenn sie mindestens ein Lokalisierungstoken (`^loc=…^`) enthalten. Weitere Informationen finden Sie unter [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz* .

## Standard {#section-c3a60e360393478284f0f2d2da5b963b}

Keine.

## Siehe auch {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md),  [Object Id Translation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ,  [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Image Serving Viewers Documentation
