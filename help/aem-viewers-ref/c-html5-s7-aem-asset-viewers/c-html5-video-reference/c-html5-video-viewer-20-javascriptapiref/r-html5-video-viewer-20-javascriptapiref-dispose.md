---
title: dispose
description: JavaScript-API-Referenz für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# dispose{#dispose}

JavaScript-API-Referenz für Video-Viewer.

`dispose()`

Stellt diese Viewer-Instanz bereit, indem alle von der Viewer-Logik verwendeten Ressourcen freigegeben und alle inneren Objekte und Komponenten gelöscht werden, die vom Viewer zur Laufzeit erstellt wurden.

Der Webseitencode sollte auch die Viewer-Instanzvariable löschen, um den Viewer vollständig aus dem Webbrowser-Speicher zu entfernen.

Wenn im Webseitencode Ereignis-Listener direkt auf vom Viewer verwendeten Viewer-SDK-Komponenten registriert sind - oder externe Verweise auf solche Komponenten gespeichert sind - müssen Sie die Registrierung dieser Listener explizit vom Webseitencode aufheben. Außerdem müssen Sie diese externen Komponentenverweise löschen, bevor Sie `dispose()`.

Rufen Sie die Viewer-API nicht mehr auf, nachdem `dispose()` aufgerufen wird.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
