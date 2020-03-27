---
description: JavaScript-API-Referenz für Video-Viewer.
seo-description: JavaScript-API-Referenz für Video-Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 74d660a1-95b3-4009-92f3-228cbe6aedc7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

JavaScript-API-Referenz für Video-Viewer.

`init()`

Beginns der Initialisierung des Video-Viewers. Bis zu diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Container-Element noch nicht Teil des Webseitenlayouts ist (z. B. kann es mithilfe des ihm zugewiesenen `display:none` Stils ausgeblendet werden), setzt der Viewer den Initialisierungsprozess so lange aus, bis die Webseite das Container-Element wieder in das Layout zurückbringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

