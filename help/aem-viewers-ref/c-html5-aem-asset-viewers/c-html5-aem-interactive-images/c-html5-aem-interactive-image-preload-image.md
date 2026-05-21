---
title: Bild vorausfüllen
description: Bild vorladen ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und angezeigt wird, während Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen heruntergeladen werden. Der Zweck des vorausgefüllten Bildes ist es, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell zu präsentieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
TQID: 'https://experienceleague.adobe.com/GlTbkyDeUNGf4gjmEEGbh1NaQ-nOgPZLtrz9kH4eK7o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 0%

---

# Bild vorausfüllen{#preload-image}

Bild vorladen ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und angezeigt wird, während Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen heruntergeladen werden. Der Zweck des vorausgefüllten Bildes ist es, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell zu präsentieren.

Das Vorausfüllen des Bildes funktioniert gut für die gängigste Methode zum Einbetten von Viewern, die responsive Einbettung mit unbegrenzter Höhe ist. Siehe die Überschrift [Responsives Design Einbetten mit unbegrenzter Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Die Funktion weist jedoch bestimmte Einschränkungen auf, wenn andere Einbettungsmethoden oder bestimmte Konfigurationsoptionen verwendet werden. Das Vorabladen des Bildes kann in folgenden Fällen möglicherweise nicht ordnungsgemäß gerendert werden:

* Wenn der Viewer in der Größe festgelegt ist und die Größe entweder mithilfe `stagesize` Konfigurationsattributs im Datensatz der Viewer-Vorgabe definiert wird. Oder verwenden Sie die CSS-Datei des externen Viewers für das Container-Element der obersten Ebene des Viewers.
* Bei Verwendung der flexiblen Einbettungsmethode mit Breite und Höhe definierte Methode der Viewer-Einbettung. Siehe die Überschrift [Flexible Einbettung mit definierter Breite und Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Deaktivieren Sie die Funktion zum Vorabladen von Bildern mithilfe des Konfigurationsattributs &quot;`preloadImage`&quot;, wenn Sie den Viewer in einem der oben aufgeführten Betriebsmodi verwenden.

Außerdem wird das Vorabladen von Bildern nicht verwendet, auch wenn es in der Konfiguration aktiviert ist, wenn der Viewer in das DOM-Element eingebettet ist, mit `display:none` CSS-Einstellung ausgeblendet oder von der DOM-Struktur getrennt wird.
