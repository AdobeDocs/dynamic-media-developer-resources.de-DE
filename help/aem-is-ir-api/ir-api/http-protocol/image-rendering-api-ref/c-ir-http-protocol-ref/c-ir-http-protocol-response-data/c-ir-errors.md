---
description: Wenn eine Anforderung nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen anderen HTTP-Antwortstatus als 200 zusammen mit einer Fehlermeldung zurück.
solution: Experience Manager
title: Fehler
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# Fehler{#errors}

Wenn eine Anforderung nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen anderen HTTP-Antwortstatus als 200 zusammen mit einer Fehlermeldung zurück.

Der Wert des Antwortstatus hängt vom Typ des Fehlers ab. für die häufigsten Fehler &quot;403&quot;. Fehlerantworten für Nicht-Bildanforderungstypen entsprechen dem Format, das mit `req=` angegeben wurde. (Kann derzeit nicht konsistent implementiert werden.)

Die in der Fehlermeldung enthaltene Detailmenge kann mit `attribute::ErrorDetail` konfiguriert werden.

**Fehlerbilder**

Image Serving kann so konfiguriert werden, dass in ein Bild gerenderte Fehlermeldungen zurückgegeben werden. Weitere Informationen finden Sie unter `attribute::ErrorImage` in der Bildkatalogreferenz. Wenn das Fehlerbild erfolgreich generiert wurde, ist der HTTP-Antwortstatus 200. Tritt bei der Verarbeitung des Fehlerbilds ein Fehler auf, werden die standardmäßige HTTP-Fehlerantwort und die Textmeldung an den Client zurückgegeben.

**Verwandte Themen**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
