---
description: Fehlerreaktionsbild. Beim Rendern von Bildern wird normalerweise ein Fehlerstatus mit einer Textmeldung zurückgegeben, wenn ein Fehler auftritt. Attribut ErrorImage ermöglicht die Konfiguration eines Bildes, das im Falle eines Fehlers zurückgegeben werden soll.
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# ErrorImage *{#errorimage}

Fehlerreaktionsbild. Beim Rendern von Bildern wird normalerweise ein Fehlerstatus mit einer Textmeldung zurückgegeben, wenn ein Fehler auftritt. attribute::ErrorImage ermöglicht die Konfiguration eines Bildes, das im Falle eines Fehlers zurückgegeben werden soll.

Wenn ein Fehler auftritt, versucht der Server zunächst, den Wert von `ImageRendering::attribute::ErrorImage`als einfachen Bilddateipfad zu interpretieren. Wenn die Datei nicht geöffnet werden kann, sendet sie den Attributwert und die Fehlerdetails an Image Serving, das wie in `ImageServing::attribute::ErrorImage` beschrieben verarbeitet. Wenn Image Serving kein gültiges Antwortbild zurückgibt, werden der standardmäßige HTTP-Fehlerstatus und die Textmeldung an den Client gesendet.

Fehlerbilder werden mit dem HTTP-Status 200 zurückgegeben.

## Eigenschaften {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Textzeichenfolge. Wenn angegeben, muss es sich entweder um einen **`ImageServing::catalog::id`**-Wert, einen relativen Pfad (zu **`ImageServing::attribute::RootPath`** oder **`ImageRendering::attribute::RootPath`**) oder einen absoluten Pfad zu einer Bilddatei handeln, auf die der Image-Server zugreifen kann.

## Standard {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Wird von `default::ErrorImage` übernommen, wenn nicht definiert. Wenn es definiert, aber leer ist, wird das Verhalten des Fehlerbilds deaktiviert, auch wenn `default::ErrorImage` definiert ist, und ein HTTP-Fehlerstatus wird zurückgegeben.

## Verwandte Themen {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
