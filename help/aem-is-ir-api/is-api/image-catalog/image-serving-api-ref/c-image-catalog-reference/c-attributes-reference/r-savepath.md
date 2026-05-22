---
description: Stammverzeichnis für saveToFile=. Relativer Pfad für den Stammordner, in den die mit req=saveToFile erstellten Bilder geschrieben werden sollen.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
TQID: 'https://experienceleague.adobe.com/CXC5-22MiZRyIjwOgOcgpRGq6kVZSZ6S-EKq8N-k7ME'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
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
