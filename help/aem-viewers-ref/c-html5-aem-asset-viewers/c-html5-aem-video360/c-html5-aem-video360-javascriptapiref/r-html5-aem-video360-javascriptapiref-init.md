---
title: init
description: JavaScript API-Referenz für Video360-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

JavaScript API-Referenz für Video360-Viewer.

`init()`

Startet die Initialisierung des Video360-Viewers. Ab diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Containerelement noch nicht Teil des Webseitenlayouts ist (z. B. kann es mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden), setzt der Viewer den Initialisierungsprozess aus. Dies geschieht bis zu dem Zeitpunkt, zu dem die Webseite das Containerelement wieder in das Layout bringt. Wenn dieses Ereignis eintritt, wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. Nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
