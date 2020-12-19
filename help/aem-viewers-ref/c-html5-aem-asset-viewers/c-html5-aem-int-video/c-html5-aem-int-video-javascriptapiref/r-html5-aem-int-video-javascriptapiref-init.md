---
description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: e6ec0730-1ddc-4026-939c-2c9f8ecee5c7
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---


# init{#init}

JavaScript-API-Referenz für den interaktiven Video-Viewer.

`init()`

Beginns der Initialisierung des interaktiven Video-Viewers. Bis zu diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Container-Element noch nicht Teil des Webseitenlayouts ist (es kann beispielsweise mit dem ihm zugewiesenen `display:none`-Stil ausgeblendet werden), setzt der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt aus, zu dem die Webseite das Container-Element wieder in das Layout einfügt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

