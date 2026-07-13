---
title: Fehler
description: Wenn eine Anfrage nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen anderen HTTP-Antwortstatus als 200 zusammen mit einer Fehlermeldung zurück.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
TQID: 'https://experienceleague.adobe.com/TSTpmfiuEppAPSUxX1ga5lfQSgWRkI2Wh1CXoalSU9A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# Fehler{#errors}

Wenn eine Anfrage nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen anderen HTTP-Antwortstatus als 200 zusammen mit einer Fehlermeldung zurück.

Der Wert für den Antwortstatus hängt vom Typ des Fehlers ab. Bei den häufigsten Fehlern ist er „403“. Fehlerantworten für Nicht-Bildanforderungstypen entsprechen dem Format, das mit `req=` angegeben wurde. (Wird derzeit möglicherweise nicht konsistent implementiert.)

Die in der Fehlermeldung enthaltene Menge an Details kann mit `attribute::ErrorDetail` konfiguriert werden.

**Fehlerbilder**

Die Bildbereitstellung kann so konfiguriert werden, dass in einem Bild gerenderte Fehlermeldungen zurückgegeben werden. Weitere Informationen finden Sie unter `attribute::ErrorImage` in der Referenz zum Bildkatalog . Wenn das Fehlerbild erfolgreich generiert wurde, ist der HTTP-Antwortstatus 200. Wenn bei der Verarbeitung des Fehlerbilds ein Fehler auftritt, wird die standardmäßige HTTP-Fehlerantwort und Textmeldung an den Client zurückgegeben.

**Siehe auch**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)

