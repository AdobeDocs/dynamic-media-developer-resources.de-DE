---
description: Modifikatorzeichenfolge für Postfix-Anforderungen. Keine oder mehr Image Serving-Befehle, durch '&'-Zeichen getrennt.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# PostModifier{#postmodifier}

Modifikatorzeichenfolge für Postfix-Anforderungen. Keine oder mehr Image Serving-Befehle, durch &#39;&amp;&#39;-Zeichen getrennt.

Befehle in diesem Feld überschreiben immer Befehle in der HTTP-Anforderung und in `catalog::Modifier`.

`catalog::PostModifier` ist nützlich, wenn bestimmte Bilder spezielle Einstellungen erfordern, die normalerweise über die URL gesteuert werden, z. B. `qlt=` oder `resmode=`. `catalog::Modifier` sollte zum Festlegen der meisten IS-Befehle im Bildkatalog verwendet werden.

Makros sind in `catalog::PostModifier` zulässig, sofern sie im selben Katalog oder im Standardkatalog definiert sind. Auch benutzerdefinierte Variablen können verwendet werden.

>[!NOTE]
>
>Wenn eine Anforderung mehrere Ebenen umfasst, wird nur der Inhalt von `catalog::PostModifier` der Ebene 0 angewendet. `catalog::PostModifier` aller anderen Ebenen wird ignoriert.

## Eigenschaften {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Textzeichenfolge. Optional.

## Standard {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Keine.

## Verwandte Themen {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
