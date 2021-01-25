---
description: Id
solution: Experience Manager
title: ID
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 45a79636-3fa9-4f2a-98bb-a46c9b627dd4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 5%

---


# Id{#id}

In der Regel ein kurzer und eindeutiger Bezeichner, z. B. eine SKU-Nummer, möglicherweise mit einer Art Suffix, z. B. wenn eine SKU mehrere Bilder oder Gebietsschema-spezifische Varianten hat. Kann auch eine komplexere Zeichenfolge sein, die eher wie ein Dateipfad aussieht, um eine einfache Nachrüstung von Websites mit Image Serving zu unterstützen.

>[!NOTE]
>
>Die Bild- und SVG-Tabellen werden beim Laden des Bildkatalogs in einer einzigen Tabelle zusammengeführt. ID-Werte müssen in beiden Tabellen eindeutig sein. Der SVG-Datensatz wird verworfen, wenn die Bildtabelle einen Datensatz mit demselben ID-Wert enthält. Statische Inhalte werden mit einer separaten Tabelle verwaltet; statische Inhaltselemente und Bild-/SVG-Elemente können daher dieselben ID-Werte aufweisen.

## Eigenschaften {#section-874a6853f67b4b229341ca76682884ae}

Textzeichenfolge. Erforderlich. Datensatzbezeichner für die Datentabelle &quot;image/SVG&quot;oder &quot;static content&quot;. Jeder `catalog::Id`-Wert in diesem Bildkatalog/SVG-Katalog oder in diesem statischen Inhaltskatalog muss eindeutig sein und darf keine &quot;,&quot;-Zeichen enthalten.

## Standard {#section-a26e7d83a5ee44b5918baef82ee48e14}

Keine.

## Verwandte Themen {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
