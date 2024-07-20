---
title: Id
description: In der Regel eine kurze und eindeutige Kennung, z. B. eine SKU-Nummer, möglicherweise mit einer Art Suffix, z. B. wenn eine SKU mehrere Bilder hat oder gebietsschemaspezifische Varianten hat.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# Id{#id}

In der Regel eine kurze und eindeutige Kennung, z. B. eine SKU-Nummer, möglicherweise mit einer Art Suffix, z. B. wenn eine SKU mehrere Bilder hat oder gebietsschemaspezifische Varianten hat. Kann auch eine komplexere Zeichenfolge sein, die eher wie ein Dateipfad aussieht, um eine einfache Nachrüstung von Websites mit Image Serving zu unterstützen.

>[!NOTE]
>
>Die Bild- und SVG-Tabellen werden beim Laden des Bildkatalogs zu einer einzigen Tabelle zusammengeführt. ID-Werte müssen in beiden Tabellen eindeutig sein. Der SVG-Datensatz wird verworfen, wenn die Bildtabelle einen Datensatz mit demselben ID-Wert enthält. Statische Inhalte werden mit einer separaten Tabelle verwaltet. Statische Inhaltselemente und Bild-/SVG-Elemente können daher dieselben ID-Werte aufweisen.

## Eigenschaften {#section-874a6853f67b4b229341ca76682884ae}

Textzeichenfolge. Erforderlich. Datensatz-ID für die Bild-/SVG- oder statische Datentabelle für Inhalte. Jeder `catalog::Id` -Wert in diesem Bildkatalog/SVG-Katalog oder in diesem statischen Inhaltskatalog muss eindeutig sein und darf keine &quot;,&quot;-Zeichen enthalten.

## Standard {#section-a26e7d83a5ee44b5918baef82ee48e14}

Keine.

## Verwandte Themen {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
