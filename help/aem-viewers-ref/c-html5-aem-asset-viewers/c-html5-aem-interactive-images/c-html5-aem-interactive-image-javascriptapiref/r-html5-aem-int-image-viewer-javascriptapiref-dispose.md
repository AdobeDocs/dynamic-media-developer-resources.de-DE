---
description: JavaScript-API-Referenz für Video-Bild-Viewer.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# dispose{#dispose}

JavaScript-API-Referenz für Video-Bild-Viewer.

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
