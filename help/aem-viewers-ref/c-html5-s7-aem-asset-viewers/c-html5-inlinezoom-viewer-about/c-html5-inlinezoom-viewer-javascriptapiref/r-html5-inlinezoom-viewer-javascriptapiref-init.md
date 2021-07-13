---
description: JavaScript-API-Referenz für Inline-Zoom-Viewer.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewer,SDK/API,Inline-Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für Inline-Zoom-Viewer.

`init()`

Startet die Initialisierung des Viewers, damit der Viewer-Code ihn anhand seiner ID finden kann. Ab diesem Zeitpunkt muss das Container-DOM-Element erstellt werden.

Wenn das Container-Element noch nicht Teil des Web-Seiten-Layouts ist (z. B. kann es mit dem ihm zugewiesenen `display:none`-Stil ausgeblendet werden), setzt der Viewer den Initialisierungsprozess so lange aus, bis die Web-Seite das Container-Element wieder in das Layout bringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
