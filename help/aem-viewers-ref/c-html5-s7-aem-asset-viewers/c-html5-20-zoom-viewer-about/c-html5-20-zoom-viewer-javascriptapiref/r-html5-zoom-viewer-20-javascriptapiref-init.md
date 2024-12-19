---
title: init
description: JavaScript-API-Referenz für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9e83b773-c059-45c6-a249-ef0ed2799a05
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für Video Viewer.

`init()`

Startet die Initialisierung des Video-Viewers. Zu diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Container-Element noch nicht Teil des Web-Seiten-Layouts ist (z. B. kann es mithilfe `display:none` Stils ausgeblendet werden), setzt der Viewer seinen Initialisierungsprozess aus. Dies geschieht bis zu dem Zeitpunkt, an dem die Web-Seite das Container-Element wieder an das Layout zurückgibt. Wenn dieser Prozess stattfindet, wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. Nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
