---
title: Id
description: Typischerweise eine kurze und eindeutige Kennung wie eine SKU-Nummer, möglicherweise mit einer Art Suffix, z. B. wenn eine SKU mehrere Bilder oder gebietsschemaspezifische Varianten hat.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
TQID: 'https://experienceleague.adobe.com/88PPZnicSyrr3x97836bu0gZpqWV-d8t-u5y-tn7nvY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 3%

---

# Id{#id}

Typischerweise eine kurze und eindeutige Kennung wie eine SKU-Nummer, möglicherweise mit einer Art Suffix, z. B. wenn eine SKU mehrere Bilder oder gebietsschemaspezifische Varianten hat. Kann auch eine komplexere Zeichenfolge sein, die mehr wie ein Dateipfad aussieht, um die einfache Nachrüstung von Websites mit Bildbereitstellung zu unterstützen.

>[!NOTE]
>
>Die Bildtabellen und SVG-Tabellen werden beim Laden des Bildkatalogs in einer einzigen Tabelle zusammengeführt. Die ID-Werte müssen in beiden Tabellen eindeutig sein. Der SVG-Datensatz wird verworfen, wenn die Bildtabelle einen Datensatz mit demselben ID-Wert enthält. Statische Inhalte werden mit einer separaten Tabelle verwaltet. Statische Inhaltselemente und Bild-/SVG-Elemente können daher dieselben ID-Werte aufweisen.

## Eigenschaften {#section-874a6853f67b4b229341ca76682884ae}

Text-String Erforderlich. Datensatzkennung für das Bild/SVG oder die statische Inhaltsdatentabelle. Jeder `catalog::Id` in diesem Bildkatalog/SVG-Katalog oder in diesem statischen Inhaltskatalog muss eindeutig sein und darf keine &quot;,“-Zeichen enthalten.

## Standard {#section-a26e7d83a5ee44b5918baef82ee48e14}

Keine.

## Verwandte Themen {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
