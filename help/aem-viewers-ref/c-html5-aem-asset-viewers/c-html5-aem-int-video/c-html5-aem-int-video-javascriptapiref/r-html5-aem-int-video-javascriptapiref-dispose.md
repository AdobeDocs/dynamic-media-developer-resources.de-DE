---
description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-title: dispose
solution: Experience Manager
title: dispose
uuid: 95046b8c-1277-4954-b13d-329994d0cb04
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# dispose{#dispose}

JavaScript-API-Referenz für den interaktiven Video-Viewer.

`dispose()`

Löscht diese Viewer-Instanz, indem alle von der Viewer-Logik verwendeten Ressourcen freigegeben und alle inneren Objekte und Komponenten gelöscht werden, die vom Viewer zur Laufzeit erstellt wurden.

Der Webseitencode sollte auch die Viewer-Instanzvariable löschen und den Viewer vollständig aus dem Webbrowser-Speicher entfernen.

Wenn der Webseitencode registrierte Ereignis-Listener direkt auf Viewer-SDK-Komponenten enthält, die vom Viewer verwendet werden, oder gespeicherte externe Verweise auf solche Komponenten, müssen diese Listener explizit vom Webseitencode nicht registriert werden. Solche externen Komponentenverweise müssen gelöscht werden, bevor `dispose()` aufgerufen wird.

Greifen Sie nach dem Aufruf von `dispose()` nicht mehr auf die Viewer-API zu.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

