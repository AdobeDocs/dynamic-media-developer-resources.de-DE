---
description: Modifikatorzeichenfolge für die Postfix-Anforderung. Keine oder mehr Bildservierungsbefehle, durch "&"getrennt.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 4%

---


# PostModifier{#postmodifier}

Modifikatorzeichenfolge für die Postfix-Anforderung. Keine oder mehr Bildservierungsbefehle, durch &quot;&amp;&quot;getrennt.

Befehle in diesem Feld überschreiben Befehle in der HTTP-Anforderung und in `catalog::Modifier`.

`catalog::PostModifier` ist nützlich, wenn bestimmte Bilder spezielle Einstellungen erfordern, die normalerweise über die URL gesteuert werden, z. B.  `qlt=` oder  `resmode=`. `catalog::Modifier` sollte zur Einstellung der meisten IS-Befehle im Bildkatalog verwendet werden.

Makros sind in `catalog::PostModifier` zulässig, sofern sie im selben Katalog oder im Standardkatalog definiert sind. Auch benutzerspezifische Variablen können verwendet werden.

>[!NOTE]
>
>Wenn eine Anforderung mehrere Ebenen umfasst, wird nur der Inhalt von `catalog::PostModifier` der Ebene 0 angewendet. `catalog::PostModifier` von allen anderen Ebenen ignoriert.

## Eigenschaften {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Textzeichenfolge. Optional.

## Standard {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Keine.

## Verwandte Themen {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[Katalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
