---
title: init
description: JavaScript-API-Referenz für interaktiven Bild-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 675031ab-21bb-49a5-abbc-eca8d2619e49
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für interaktiven Bild-Viewer.

`init()`

Startet die Initialisierung des interaktiven Bild-Viewers. Ab diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Containerelement noch nicht Teil des Webseitenlayouts ist - z. B. kann es mit dem ihm zugewiesenen `display:none`-Stil ausgeblendet werden -, setzt der Viewer den Initialisierungsprozess aus. Dies geschieht bis zu dem Zeitpunkt, zu dem die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion erfolgt, wird der Viewer automatisch neu geladen.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
