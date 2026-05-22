---
title: verfügen
description: JavaScript-API-Referenz für Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c796943e-8ea8-4a97-a1ff-09676204150a
TQID: 'https://experienceleague.adobe.com/Fi7inW4o2cQ5r3518sL7n8GWCJZeVf94Za4-2unBzRE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 3%

---

# verfügen{#dispose}

JavaScript-API-Referenz für Zoom-Viewer.

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
