---
description: JavaScript-API-Referenz für Video-Viewer.
seo-description: JavaScript-API-Referenz für Video-Viewer.
seo-title: init
solution: Experience Manager
title: init
uuid: 2ee5bddc-957c-4813-9285-d64b9ac7d590
feature: Dynamic Media Classic, Viewer, SDK/API, Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---


# init{#init}

JavaScript-API-Referenz für Video-Viewer.

`init()`

Beginns der Initialisierung des Video-Viewers. Bis zu diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Container-Element noch nicht Teil des Webseitenlayouts ist, kann es mit dem ihm zugewiesenen `display:none`-Stil ausgeblendet werden. Der Viewer unterbricht den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

