---
title: dispose
description: JavaScript API-Referenz für Video360-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# dispose{#dispose}

JavaScript API-Referenz für Video360-Viewer.

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
