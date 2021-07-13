---
description: Id
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---

# ID{#id}

In der Regel handelt es sich um eine kurze und eindeutige Kennung, z. B. eine SKU-Nummer, die möglicherweise ein Suffix aufweist, z. B. wenn eine SKU mehrere Bilder hat oder gebietsschemaspezifische Varianten aufweist. Kann auch eine komplexere Zeichenfolge sein, die eher wie ein Dateipfad aussieht, um eine einfache Nachrüstung von Websites mit Image Serving zu unterstützen.

>[!NOTE]
>
>Die Bild- und SVG-Tabellen werden beim Laden des Bildkatalogs zu einer einzigen Tabelle zusammengeführt. ID-Werte müssen in beiden Tabellen eindeutig sein. Der SVG-Datensatz wird verworfen, wenn die Bildtabelle einen Datensatz mit demselben ID-Wert enthält. Statische Inhalte werden mit einer separaten Tabelle verwaltet; statische Inhaltselemente und Bild-/SVG-Elemente können daher dieselben ID-Werte aufweisen.

## Eigenschaften {#section-874a6853f67b4b229341ca76682884ae}

Textzeichenfolge. Erforderlich. Datensatz-ID für die Bild-/SVG- oder statische Datentabelle für Inhalte. Jeder `catalog::Id` -Wert in diesem Bildkatalog/SVG-Katalog oder in diesem statischen Inhaltskatalog muss eindeutig sein und darf keine &quot;,&quot;-Zeichen enthalten.

## Standard {#section-a26e7d83a5ee44b5918baef82ee48e14}

Keine.

## Verwandte Themen {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
