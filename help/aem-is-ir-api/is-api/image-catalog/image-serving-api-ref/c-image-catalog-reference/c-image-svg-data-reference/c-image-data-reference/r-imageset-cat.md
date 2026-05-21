---
description: Bildset-Daten. Bietet einen Mechanismus zum Definieren sortierter Bildsets und Steuerungsattribute, die von den Dynamic Media-Viewern verwendet werden.
solution: Experience Manager
title: Bildsatz
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
TQID: 'https://experienceleague.adobe.com/wh25AlzBQv0W-lEugybS8B-cIYYFoK8o9I2uGb52Ui4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 681
ht-degree: 1%

---

# Bildsatz{#imageset}

Bildset-Daten. Bietet einen Mechanismus zum Definieren sortierter Bildsets und Steuerungsattribute, die von den Dynamic Media-Viewern verwendet werden.

Ein Bildset besteht aus einer sortierten, durch Kommas getrennten Liste von Elementen. Jedes Element besteht aus einem oder mehreren Unterelementen (Bild-IDs, Farbfeld-IDs, Mediendateipfade, Beschriftungen usw.), die durch Semikolons, Doppelpunkte oder beides getrennt sind.

Geschweifte Klammern `{ }` und Klammern `( )` verwendet werden, um bestimmte Inhalte (z. B. Farbwerte) abzugrenzen oder verschachtelte Sets anzugeben. Auf diese Weise verwendete Klammern oder Klammern dürfen nicht kodiert werden und müssen immer als übereinstimmende Paare angezeigt werden. Andernfalls tritt ein Katalogparsing-Fehler auf.

>[!NOTE]
>
>Die folgenden Zeichen werden als Set-Trennzeichen verwendet und müssen HTTP-kodiert sein, wenn sie im Set als Teil der ID- oder Zeichenfolgenwerte erscheinen:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


Weitere Informationen zur Struktur und Verwendung von Bildsets finden Sie in der Dokumentation zu Image Serving Viewers .

Der Server gibt den Inhalt dieses Felds als Antwort auf eine `req=imageset`-Anfrage ohne Änderungen zurück.

## Standardsätze {#section-5ecc8ffee7224668b63f601383665564}

Die folgenden Set-Definitionen werden nativ von Image Serving unterstützt, und der Zugriff mit bestimmten Viewern umfasst das Server-seitige Analysieren, Validieren und Verarbeiten des Sets. Jeder Settyp kann identifiziert werden, indem der entsprechende Wert in `catalog::AssetType` angegeben wird.

**Grundlegende Farbfeldsets**

Jedes Element in einem grundlegenden Musterset besteht aus einem Verweis auf einen Bilddatensatz und einem optionalen separaten Verweis auf einen Bilddatensatz, der als Muster verwendet wird.

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`swatch`*]` |
| `*`swatch`*` | `*`swatchId`*`\|`solidColorSpecifier` |
| `*`imageId`*` | IS-Bildreferenz (Katalog/ID) |
| `*`swatchId`*` | IS-Bildreferenz (Katalog/ID) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`label`*]'}'` |
| `*`rrggbb`*` | Gepackter 6-stelliger Hex-RGB-Farbwert für einfarbige Farbfelder |
| `*`label`*` | Optionale Textbeschriftung für Volltonfarbfelder |

**Hierarchische Mustersets**

Jedes Element in einem hierarchischen Mustersatz kann aus einem grundlegenden Musterelement oder einem Verweis auf einen Mustersatzdatensatz bestehen (für solche Elemente sind Muster erforderlich).

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`*` \| `{` *`basicSwatchSetId`* &#39;;&#39; *`swatch`* `}` |
| `*`basicSwatchSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der einen grundlegenden Mustersatz definiert |

**Einfache Rotationssets**

Ein einfaches Rotationsset besteht aus einer einfachen Liste von Bild-IDs.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Zweidimensionale Rotationssets**

Jedes Element in einem zweidimensionalen Rotationsset kann aus einem einfachen Bild, einem Verweis auf ein grundlegendes Rotationsset oder einem Inline-BasisRotationsset bestehen, das durch geschweifte Klammern getrennt ist. Anstelle von geschweiften Klammern können Klammern verwendet werden.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`*` \| `{` &#39;{&#39; *`basicSpinSet`* &#39;}&#39; `}` \| `*`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | IS-Verweis (Katalog/ID) auf einen Katalogdatensatz, der ein grundlegendes Rotationsset definiert |

**Seitensätze**

Jedes Element in einem Seitensatz kann aus bis zu dreiseitigen Bildern bestehen, die durch Doppelpunkte getrennt sind.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Mediensets**

Jedes Element in einem Medienset kann aus einem Bild, einem grundlegenden Musterset, einem hierarchischen Musterset, einem einfachen Rotationsset, einem zweidimensionalen Rotationsset, einem Seitensatz oder einem Video-Asset bestehen. Jedes Medienset-Element kann auch eine optionale Farb-/Bildmuster- und Typkennung enthalten.

| `*`mediaSet`*` | `*`item`* &#42;[ , *`item`* ]` |
|---|---|
| `*`item`*` | `{ *`videoItem`*` \| *`recutItem`* \| *`imageItem`*`}}`\|*`setItem`*`}` `[` ; `[`*`ID`*`]` `[` ; `[` `] ] ]`*`reserved`* |
| `*`videoItem`*` | `*`video`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | `{ *`setId`*` \| `{` &#39;{&#39; *`inlineSet`* &#39;}&#39; `} }` ; *`swatchId`* |
| `*`ID`*` | `media type identifier` `[` img \| basic \| advanced_image \| img \| img_set \| advanced_imageset \| advanced_swatchset \| Spin \| `]` |
| `*`swatchId`*` | IS-Bild-ID |
| `*`video`*` | Pfad der Video-/Animationsdatei oder statische Katalog-ID |
| `*`neu schneiden`*` | XML-Dateipfad für Neuausschnittdefinition oder statische Katalog-ID |
| `*`imageId`*` | IS-Bild-ID |
| `*`setId`*` | IS-Verweis auf Bild-, Rotations- oder E-Katalog-Set |
| `*`inlineSet`*` | Inline-Bild, Rotation oder E-Katalog |
| `*`reserviert`*` | Reserviert für zukünftige Verwendung |

**Videosets**

Ein Videoset besteht aus einer einfachen Liste von Video-IDs, wobei jede ID auf einen Eintrag im statischen Inhaltskatalog verweist.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Eigenschaften {#section-17c731e5c46646aa90ac21f39bb693ca}

Text-String Durch Kommas getrennte Liste von `catalog::Id`, absoluten Image-Server-Dateipfaden oder Dateipfaden relativ zu `attribute::RootPath`. Dasselbe Bild kann im Set mehrmals referenziert werden. Der definierende Katalogdatensatz kann im Set an einer beliebigen Stelle angezeigt werden.

Dieses Feld ist an der Lokalisierung von Textzeichenfolgen beteiligt. Zusätzlich zu *`label`* Zeichenfolgen (Teil des *`solidColorSpecifier`*) werden alle durch Trennzeichen getrennten Felder lokalisiert, wenn sie mindestens ein Lokalisierungs-Token &quot;`^loc=…^`&quot; enthalten. Siehe [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz* für Details.

## Standard {#section-c3a60e360393478284f0f2d2da5b963b}

Keine.

## Siehe auch {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=ImageSet](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::rootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Object ID Translation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Dokumentation zu Image Serving Viewers
