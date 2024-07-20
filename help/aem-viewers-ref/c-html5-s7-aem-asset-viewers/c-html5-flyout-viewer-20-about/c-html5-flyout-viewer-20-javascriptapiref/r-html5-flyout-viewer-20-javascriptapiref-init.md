---
title: init
description: JavaScript-API-Referenz zur Initialisierung des Flyout-Viewers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für Flyout-Viewer.

`init()`

Startet die Initialisierung des Flyout-Viewers. Ab diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Containerelement noch nicht Teil des Webseitenlayouts ist (z. B.), kann es mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden. Der Viewer setzt den Initialisierungsprozess aus. Dies geschieht bis zu dem Zeitpunkt, zu dem die Webseite das Containerelement wieder in das Layout bringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

Diese Methode sollte nur einmal während des Lebenszyklus des Viewers aufgerufen werden. Nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
