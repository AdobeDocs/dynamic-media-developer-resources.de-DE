---
title: init
description: JavaScript-API-Referenz für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für interaktiven Video-Viewer.

`init()`

Startet die Initialisierung des interaktiven Video-Viewers. Ab diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Containerelement noch nicht Teil des Webseitenlayouts ist - z. B. kann es mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden -, setzt der Viewer seinen Initialisierungsprozess aus. Dies geschieht bis zu dem Zeitpunkt, zu dem die Webseite das Containerelement wieder in das Layout bringt. Wenn dieses Ereignis eintritt, wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. Nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
