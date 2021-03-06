---
title: Fehler
description: Wenn eine Anfrage nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen HTTP-Antwortstatus mit einem anderen Status als 200 zusammen mit einer Fehlermeldung zurück.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# Fehler{#errors}

Wenn eine Anfrage nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen HTTP-Antwortstatus mit einem anderen Status als 200 zusammen mit einer Fehlermeldung zurück.

Der Antwortstatus hängt vom Fehlertyp ab. für die häufigsten Fehler &quot;403&quot;. Fehlerantworten für Nicht-Bildanforderungstypen entsprechen dem Format, das mit `req=`. (Möglicherweise ist die Implementierung derzeit nicht konsistent.)

Die in der Fehlermeldung enthaltene Detailmenge kann mit `attribute::ErrorDetail`.

**Fehlerbilder**

Image Serving kann so konfiguriert werden, dass in einem Bild gerenderte Fehlermeldungen zurückgegeben werden. Siehe `attribute::ErrorImage` in der Bildkatalogreferenz für Details. Wenn das Fehlerbild erfolgreich generiert wurde, lautet der HTTP-Antwortstatus 200. Tritt bei der Verarbeitung des Fehlerbilds ein Fehler auf, werden die standardmäßige HTTP-Fehlerantwort und die Textmeldung an den Client zurückgegeben.

**Verwandte Themen**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
