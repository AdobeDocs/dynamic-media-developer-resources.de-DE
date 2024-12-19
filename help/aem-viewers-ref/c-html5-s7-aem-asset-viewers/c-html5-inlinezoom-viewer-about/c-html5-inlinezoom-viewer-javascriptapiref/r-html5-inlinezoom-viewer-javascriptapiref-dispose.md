---
title: verfügen
description: JavaScript-API-Referenz für Inline-Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7e525bc1-6986-414c-acc0-e011dfd7b84b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# verfügen{#dispose}

JavaScript-API-Referenz für Inline-Zoom-Viewer.

`dispose()`

Löscht diese Viewer-Instanz, indem sie alle von der Viewer-Logik verwendeten Ressourcen freigibt und alle inneren Objekte und Komponenten löscht, die vom Viewer zur Laufzeit erstellt wurden.

Der Web-Seiten-Code sollte auch die Variable „Viewer-Instanz“ löschen, um den Viewer vollständig aus dem Speicher des Webbrowsers zu entfernen.

Wenn der Web-Seiten-Code Ereignis-Listener direkt in vom Viewer verwendeten Viewer-SDK-Komponenten registriert hat - oder wenn externe Verweise auf solche Komponenten gespeichert wurden - müssen diese Listener vom Web-Seiten-Code explizit deregistriert werden. Und diese externen Komponentenverweise müssen vor dem Aufruf von `dispose()` gelöscht werden.

Greifen Sie nach dem Aufruf von `dispose()` nicht mehr auf die Viewer-API zu.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
