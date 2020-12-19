---
description: Modifikatorzeichenfolge für die Präfix-Anforderung. Keine oder mehr Bildservierungsbefehle, durch "&"getrennt.
seo-description: Modifikatorzeichenfolge für die Präfix-Anforderung. Keine oder mehr Bildservierungsbefehle, durch "&"getrennt.
seo-title: Modifikator
solution: Experience Manager
title: Modifikator
topic: Scene7 Image Serving - Image Rendering API
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---


# Modifikator{#modifier}

Modifikatorzeichenfolge für die Präfix-Anforderung. Keine oder mehr Bildservierungsbefehle, durch &quot;&amp;&quot;getrennt.

Dient zum dauerhaften Ändern von Bildern und Speichern des Textkörpers der Vorlagen.

Befehle in diesem Feld werden durch dieselben Befehle in der Anforderung oder Vorlage, auf die dieser Datensatz verweist, sowie durch Befehle in `catalog::PostModifier` überschrieben

Makros sind in `catalog::Modifier` zulässig, sofern sie im selben Katalog oder im Standardkatalog definiert sind. Auch benutzerspezifische Variablen können verwendet werden.

## Eigenschaften {#section-6674388f77d644469371a17e8809c45f}

Textzeichenfolge. Optional.

## Standard {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Keine.

## Verwandte Themen {#section-7a67803d141b442180c418c1f3cff029}

[Katalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
