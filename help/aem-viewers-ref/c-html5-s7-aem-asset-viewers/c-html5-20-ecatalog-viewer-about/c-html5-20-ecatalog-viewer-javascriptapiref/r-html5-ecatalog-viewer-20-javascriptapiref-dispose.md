---
title: verfügen
description: JavaScript-API-Referenz für den E-Katalog-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 827decd9-1f6c-4ac1-8fcc-acc93cfb859d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# verfügen{#dispose}

JavaScript-API-Referenz für den E-Katalog-Viewer.

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
