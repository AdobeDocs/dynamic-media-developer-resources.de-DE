---
description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-title: dispose
solution: Experience Manager
title: dispose
topic: Dynamic media
uuid: 95046b8c-1277-4954-b13d-329994d0cb04
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# dispose{#dispose}

JavaScript-API-Referenz für den interaktiven Video-Viewer.

`dispose()`

Löscht diese Viewer-Instanz, indem alle von der Viewer-Logik verwendeten Ressourcen freigegeben und alle inneren Objekte und Komponenten gelöscht werden, die vom Viewer zur Laufzeit erstellt wurden.

Der Webseitencode sollte auch die Viewer-Instanzvariable löschen und den Viewer vollständig aus dem Webbrowser-Speicher entfernen.

Wenn der Webseitencode registrierte Ereignis-Listener direkt auf Viewer-SDK-Komponenten enthält, die vom Viewer verwendet werden, oder gespeicherte externe Verweise auf solche Komponenten enthält, müssen diese Listener explizit vom Webseitencode nicht registriert werden. Solche externen Komponentenverweise müssen vor dem Aufruf gelöscht werden `dispose()`.

Greifen Sie nach dem Aufruf nicht mehr auf die Viewer-API zu `dispose()` .

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

