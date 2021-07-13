---
description: JavaScript-API-Referenz für Viewer für gemischte Medien.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: e09f73a9-a961-4188-b092-f7bbcae4946d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# dispose{#dispose}

JavaScript-API-Referenz für Viewer für gemischte Medien.

`dispose()`

Stellt diese Viewer-Instanz bereit, indem alle von der Viewer-Logik verwendeten Ressourcen freigegeben und alle inneren Objekte und Komponenten gelöscht werden, die vom Viewer zur Laufzeit erstellt wurden.

Der Webseitencode sollte auch die Viewer-Instanzvariable löschen, um den Viewer vollständig aus dem Webbrowser-Speicher zu entfernen.

Wenn der Webseitencode Ereignis-Listener direkt auf Viewer-SDK-Komponenten enthält, die vom Viewer verwendet werden, oder externe Verweise auf solche Komponenten gespeichert hat, müssen diese Listener explizit vom Webseitencode abgemeldet werden. Solche externen Komponentenverweise müssen vor dem Aufruf von `dispose()` gelöscht werden.

Greifen Sie nach dem Aufruf von `dispose()` nicht mehr auf die Viewer-API zu.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
