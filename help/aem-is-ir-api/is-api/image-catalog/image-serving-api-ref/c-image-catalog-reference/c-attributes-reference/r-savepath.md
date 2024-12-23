---
description: Stammverzeichnis für saveToFile=. Relativer Pfad für den Stammordner, in den die mit req=saveToFile erstellten Bilder geschrieben werden sollen.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# SavePath{#savepath}

Stammverzeichnis für saveToFile=. Relativer Pfad für den Stammordner, in den die mit req=saveToFile erstellten Bilder geschrieben werden sollen.

`SavePath` ist ein Textzeichenfolgenwert.

## Eigenschaften {#section-343d1371e966491c92854a8df14c3c50}

Text-String Muss leer sein oder ein gültiger relativer Ordnerpfad. Immer mit dem absoluten Stammpfad kombiniert, der mit `ImageServer::SaveDirectory` konfiguriert wurde.

## Standard {#section-ae751eea97654f399c6aaee3f3252cbb}

Von `default::SavePath` geerbt, wenn nicht definiert. Das Speichern in Dateien ist deaktiviert, wenn der aufgelöste Wert leer ist.

## Verwandte Themen {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
