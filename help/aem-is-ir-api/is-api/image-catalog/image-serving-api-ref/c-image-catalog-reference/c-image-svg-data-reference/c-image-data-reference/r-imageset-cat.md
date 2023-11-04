---
description: Bildsatzdaten. Bietet einen Mechanismus zum Definieren sortierter Bildsätze und von den Dynamic Media-Viewern verwendete Steuerelementattribute.
solution: Experience Manager
title: Bildsatz
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---

# Bildsatz{#imageset}

Bildsatzdaten. Bietet einen Mechanismus zum Definieren sortierter Bildsätze und von den Dynamic Media-Viewern verwendete Steuerelementattribute.

Ein Bildset besteht aus einer sortierten, kommagetrennten Liste von Elementen. Jedes Element besteht aus einem oder mehreren Unterelementen (Bild-IDs, Muster-IDs, Mediendateipfade, Beschriftungen usw.), die durch Semikolons, Doppelpunkte oder beides voneinander getrennt sind.

geschweifte Klammern `{ }` und Klammern `( )` kann verwendet werden, um bestimmte Inhalte (z. B. Farbwerte) zu trennen oder verschachtelte Sets anzugeben. Auf diese Weise verwendete Klammern oder Klammern dürfen nicht codiert sein und müssen immer als übereinstimmende Paare angezeigt werden. Andernfalls tritt ein Katalogparsing-Fehler auf.

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

Der Server gibt den Inhalt dieses Felds ohne Änderung als Antwort auf eine `req=imageset` -Anfrage.

## Standardsätze {#section-5ecc8ffee7224668b63f601383665564}

Die folgenden Definitionen werden nativ vom Image Serving unterstützt. Der Zugriff auf bestimmte Viewer umfasst das serverseitige Parsen, Validieren und Verarbeiten des Sets. Jeder Set-Typ kann identifiziert werden, indem der entsprechende Wert in `catalog::AssetType`.

**Grundlegende Mustersets**

Jedes Element in einem grundlegenden Musterset besteht aus einem Verweis auf einen Bilddatensatz und einem optionalen separaten Verweis auf einen Bilddatensatz, der als Muster verwendet wird.

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`Musterabschnitt`*]` |
| `*`Musterabschnitt`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS-Bildreferenz (Katalog/ID) |
| `*`swatchId`*` | IS-Bildreferenz (Katalog/ID) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rgbb`* [ *`label`*]'}'` |
| `*`rgbb`*` | Verpackter 6-stelliger hexadezimaler RGB-Farbwert für Farbmuster mit Volltonfarbe |
| `*`label`*` | Optionale Textbeschriftung für Farbmuster mit Volltonfarbe |

**Hierarchische Mustersets**

Jedes Element in einem hierarchischen Musterset kann aus einem einfachen Musterelement oder einem Verweis auf einen Musterset-Datensatz bestehen (für solche Elemente sind Muster erforderlich).

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`Musterabschnitt`* }` |
| `*`basicSwatchSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der ein einfaches Musterset definiert |

**Einfache Rotationssets**

Ein einfaches Rotationsset besteht aus einer einfachen Liste von Bild-IDs.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Zweidimensionale Rotationssets**

Jedes Element in einem zweidimensionalen Rotationsset kann aus einem einfachen Bild, einem Verweis auf ein einfaches Rotationsset oder einem durch geschweifte Klammern getrennten einfachen Inline-Rotationsset bestehen. Klammern können anstelle von geschweiften Klammern verwendet werden.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der ein einfaches Rotationsset definiert |

**Seitensätze**

Jedes Element in einem Seitensatz kann aus bis zu dreiteiligen Bildern bestehen, die durch Doppelpunkte voneinander getrennt sind.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Mediensets**

Jedes Element in einem Medienset kann aus einem Bild, einem einfachen Musterset, einem hierarchischen Musterset, einem einfachen Rotationsset, einem zweidimensionalen Rotationsset, einem Seitensatz oder einem Video-Asset bestehen. Jedes Medienset-Element kann auch ein optionales Muster und eine Typkennung enthalten.

| `*`mediaSet`*` | `*`item`* &#42;[ , *`item`* ]` |
|---|---|
| `*`Element`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`reserviert`* ] ] ]` |
| `*`videoItem`*` | `*`Video`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
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

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Eigenschaften {#section-17c731e5c46646aa90ac21f39bb693ca}

Textzeichenfolge. Kommagetrennte Liste von `catalog::Id` Werte, absolute Image Server-Dateipfade oder Dateipfade relativ zu `attribute::RootPath`. Auf dasselbe Bild kann mehr als einmal im Set verwiesen werden. Der definierte Katalogdatensatz kann in der Gruppe an jedem beliebigen Speicherort angezeigt werden.

Dieses Feld nimmt an der Lokalisierung von Textzeichenfolgen teil. Zusätzlich zu *`label`* Zeichenfolgen (Teil der *`solidColorSpecifier`*) werden alle durch Trennzeichen getrennten Felder lokalisiert, wenn sie mindestens ein &quot; `^loc=…^`Lokalisierungstoken. Siehe Abschnitt [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) im *HTTP-Protokollreferenz* für Details.

## Standard {#section-c3a60e360393478284f0f2d2da5b963b}

Keine.

## Siehe auch {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Objekt-ID-Übersetzung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Dokumentation zu Image Serving Viewers
