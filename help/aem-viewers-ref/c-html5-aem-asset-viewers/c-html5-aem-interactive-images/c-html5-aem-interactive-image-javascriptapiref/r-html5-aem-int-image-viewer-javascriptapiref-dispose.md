---
title: dispose
description: JavaScript API-Referenz für Video Image Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# dispose{#dispose}

JavaScript API-Referenz für Video Image Viewer.

`dispose()`

Stellt diese Viewer-Instanz bereit, indem alle von der Viewer-Logik verwendeten Ressourcen freigegeben und alle inneren Objekte und Komponenten gelöscht werden, die vom Viewer zur Laufzeit erstellt wurden.

Der Webseitencode sollte auch die Viewer-Instanzvariable löschen, um den Viewer vollständig aus dem Webbrowser-Speicher zu entfernen.

Wenn der Webseitencode Ereignis-Listener direkt auf Viewer-SDK-Komponenten enthält, die vom Viewer verwendet werden - oder externe Verweise auf solche Komponenten gespeichert hat - müssen diese Listener explizit vom Webseitencode abgemeldet werden. Außerdem müssen solche externen Komponentenverweise gelöscht werden, bevor `dispose()` aufgerufen wird.

Greifen Sie nach dem Aufruf von `dispose()` nicht mehr auf die Viewer-API zu.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
