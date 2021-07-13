---
description: Präfix-Anfrage-Modifikatorzeichenfolge. Keine oder mehr Image Serving-Befehle, durch '&'-Zeichen getrennt.
solution: Experience Manager
title: Modifikator
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# Modifikator{#modifier}

Präfix-Anfrage-Modifikatorzeichenfolge. Keine oder mehr Image Serving-Befehle, durch &#39;&amp;&#39;-Zeichen getrennt.

Wird verwendet, um Bilder dauerhaft zu ändern und den Hauptteil von Vorlagen zu speichern.

Befehle in diesem Feld werden durch dieselben Befehle in der Anforderung oder Vorlage, von der aus dieser Datensatz referenziert wird, und durch Befehle in `catalog::PostModifier` überschrieben

Makros sind in `catalog::Modifier` zulässig, sofern sie im selben Katalog oder im Standardkatalog definiert sind. Auch benutzerdefinierte Variablen können verwendet werden.

## Eigenschaften {#section-6674388f77d644469371a17e8809c45f}

Textzeichenfolge. Optional.

## Standard {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Keine.

## Verwandte Themen {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
