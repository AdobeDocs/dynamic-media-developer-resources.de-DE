---
title: ErrorImage
description: Fehlerreaktionsbild. Beim Rendern von Bildern wird normalerweise ein Fehlerstatus mit einer Textmeldung zurückgegeben, wenn ein Fehler auftritt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# ErrorImage {#errorimage}

Fehlerreaktionsbild. Beim Rendern von Bildern wird normalerweise ein Fehlerstatus mit einer Textmeldung zurückgegeben, wenn ein Fehler auftritt. Die `attribute::ErrorImage` ermöglicht die Konfiguration eines Bildes, das bei einem Fehler zurückgegeben werden soll.

Wenn ein Fehler auftritt, versucht der Server, den Wert von `ImageRendering::attribute::ErrorImage`als einfachen Bilddateipfad. Wenn die Datei nicht geöffnet werden kann, sendet sie den Attributwert und die Fehlerdetails an Image Serving, das wie unter `ImageServing::attribute::ErrorImage`. Wenn Image Serving kein gültiges Antwortbild zurückgibt, werden der standardmäßige HTTP-Fehlerstatus und die Textmeldung an den Client gesendet.

Fehlerbilder werden mit dem HTTP-Status 200 zurückgegeben.

## Eigenschaften {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Textzeichenfolge. Wenn angegeben, muss es sich um eine **`ImageServing::catalog::id`** -Wert, einen relativen Pfad (zu **`ImageServing::attribute::RootPath`** oder **`ImageRendering::attribute::RootPath`**) oder einen absoluten Pfad zu einer Bilddatei, auf die der Image-Server zugreifen kann.

## Standard {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Vererbt von `default::ErrorImage` , wenn sie nicht definiert ist. Wenn es definiert, aber leer ist, ist das Verhalten des Fehlerbilds deaktiviert, auch wenn `default::ErrorImage` definiert ist und ein HTTP-Fehlerstatus zurückgegeben wird.

## Verwandte Themen {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
