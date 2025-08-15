---
title: Id
description: Typischerweise eine kurze und eindeutige Kennung wie eine SKU-Nummer, möglicherweise mit einer Art Suffix, z. B. wenn eine SKU mehrere Bilder oder gebietsschemaspezifische Varianten hat.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# Id{#id}

Normalerweise eine kurze und eindeutige Kennung wie eine SKU-Nummer, möglicherweise mit einer Art Suffix, z. B. wenn eine SKU mehrere Bilder oder gebietsschemaspezifische Varianten hat. Kann auch eine komplexere Zeichenfolge sein, die mehr wie ein Dateipfad aussieht, um die einfache Nachrüstung von Websites mit Bildbereitstellung zu unterstützen.

>[!NOTE]
>
>Die Bildtabellen und SVG-Tabellen werden beim Laden des Bildkatalogs in einer einzigen Tabelle zusammengeführt. Die ID-Werte müssen in beiden Tabellen eindeutig sein. Der SVG-Datensatz wird verworfen, wenn die Bildtabelle einen Datensatz mit demselben ID-Wert enthält. Statische Inhalte werden mit einer separaten Tabelle verwaltet. Statische Inhaltselemente und Bild-/SVG-Elemente können daher dieselben ID-Werte aufweisen.

## Eigenschaften {#section-874a6853f67b4b229341ca76682884ae}

Text-String Erforderlich. Datensatzkennung für das Bild/SVG oder die statische Inhaltsdatentabelle. Jeder `catalog::Id` in diesem Bildkatalog/SVG-Katalog oder in diesem statischen Inhaltskatalog muss eindeutig sein und darf keine &quot;,“-Zeichen enthalten.

## Standard {#section-a26e7d83a5ee44b5918baef82ee48e14}

Keine.

## Verwandte Themen {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
