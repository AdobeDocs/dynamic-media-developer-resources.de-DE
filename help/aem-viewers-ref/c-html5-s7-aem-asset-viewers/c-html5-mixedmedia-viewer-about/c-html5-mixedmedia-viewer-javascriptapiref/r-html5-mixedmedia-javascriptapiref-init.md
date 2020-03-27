---
description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: f16e3cfe-4b30-4497-bd65-52d2f1edf3d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

JavaScript-API-Referenz für gemischte Medien-Viewer.

`init()`

Beginn für die Initialisierung des gemischten Medien-Viewers. Bis zu diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Container-Element noch nicht Teil des Webseitenlayouts ist (z. B. mit dem ihm zugewiesenen `display:none` Stil ausgeblendet), setzt der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt aus, an dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

