---
description: JavaScript-API-Referenz für den E-Katalog-Viewer.
seo-description: JavaScript-API-Referenz für den E-Katalog-Viewer.
seo-title: dispose
solution: Experience Manager
title: dispose
topic: Dynamic media
uuid: 791c47e9-daab-4500-9cd0-e56ee6fc830e
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# dispose{#dispose}

JavaScript-API-Referenz für den E-Katalog-Viewer.

[!DNL `dispose()`]

Löscht diese Viewer-Instanz, indem alle von der Viewer-Logik verwendeten Ressourcen freigegeben und alle inneren Objekte und Komponenten gelöscht werden, die vom Viewer zur Laufzeit erstellt wurden.

Der Webseitencode sollte auch die Viewer-Instanzvariable löschen und den Viewer vollständig aus dem Webbrowser-Speicher entfernen.

Wenn der Webseitencode registrierte Ereignis-Listener direkt auf Viewer-SDK-Komponenten enthält, die vom Viewer verwendet werden, oder gespeicherte externe Verweise auf solche Komponenten, müssen diese Listener explizit vom Webseitencode nicht registriert werden. Solche externen Komponentenverweise müssen gelöscht werden, bevor [!DNL `dispose()`] aufgerufen wird.

Greifen Sie nach dem Aufruf von [!DNL `dispose()`] nicht mehr auf die Viewer-API zu.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

