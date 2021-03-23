---
description: Stammpfad für saveToFile=. Relativer Pfad für den Stammordner, in den mit req=saveToFile generierte Bilder geschrieben werden sollen.
seo-description: Stammpfad für saveToFile=. Relativer Pfad für den Stammordner, in den mit req=saveToFile generierte Bilder geschrieben werden sollen.
seo-title: SavePath
solution: Experience Manager
title: SavePath
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# SavePath{#savepath}

Stammpfad für saveToFile=. Relativer Pfad für den Stammordner, in den mit req=saveToFile generierte Bilder geschrieben werden sollen.

`SavePath` ist ein Textzeichenfolgenwert.

## Eigenschaften {#section-343d1371e966491c92854a8df14c3c50}

Textzeichenfolge. Muss leer oder ein gültiger relativer Ordnerpfad sein. Immer mit dem absoluten Stammpfad kombiniert, der mit `ImageServer::SaveDirectory` konfiguriert wurde.

## Standard {#section-ae751eea97654f399c6aaee3f3252cbb}

Vererbt von `default::SavePath`, wenn nicht definiert. Das Speichern in Dateien ist deaktiviert, wenn der aufgelöste Wert leer ist.

## Verwandte Themen {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
