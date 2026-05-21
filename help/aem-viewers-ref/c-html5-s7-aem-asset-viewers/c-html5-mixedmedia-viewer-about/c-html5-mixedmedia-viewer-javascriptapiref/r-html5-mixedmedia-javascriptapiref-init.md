---
title: init
description: JavaScript-API-Referenz für den Viewer für gemischte Medien.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
TQID: 'https://experienceleague.adobe.com/ePEFdZuRissBOT3MiTbKElPhonr9UGlR02dfN4CqUcE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für den Viewer für gemischte Medien.

`init()`

Startet die Initialisierung des Viewers für gemischte Medien. Zu diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Container-Element noch nicht Teil des Web-Seiten-Layouts ist - es kann beispielsweise mithilfe `display:none` Stils ausgeblendet werden - setzt der Viewer seinen Initialisierungsprozess aus. Sie wird ausgesetzt, bis die Web-Seite das Container-Element wieder an das Layout anpasst. Ab diesem Zeitpunkt wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. Nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
