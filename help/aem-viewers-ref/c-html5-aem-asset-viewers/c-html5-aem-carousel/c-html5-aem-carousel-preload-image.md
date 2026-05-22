---
title: Bild vorausfüllen
description: Bild vorladen ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und angezeigt wird, während Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen heruntergeladen werden. Der Zweck des vorausgefüllten Bildes ist es, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell zu präsentieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
TQID: 'https://experienceleague.adobe.com/0Gm-U-1l0osVADyWyLCH4rJRUCuRHgUJ8XNsbDNpkgc'
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

Das Vorausfüllen des Bildes funktioniert gut für die gängigste Methode zum Einbetten von Viewern, die responsive Einbettung mit unbegrenzter Höhe ist. Siehe die Überschrift [Responsives Design Einbetten mit unbegrenzter Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Die Funktion weist jedoch bestimmte Einschränkungen auf, wenn andere Einbettungsmethoden oder bestimmte Konfigurationsoptionen verwendet werden. Das Vorabladen des Bildes kann in folgenden Fällen möglicherweise nicht ordnungsgemäß gerendert werden:

* Wenn die Größe des Viewers festgelegt ist und die Größe entweder mithilfe `stagesize` Konfigurationsattributs im Viewer-Vorgabendatensatz oder in der CSS-Datei des externen Viewers für das Viewer-Container-Element der obersten Ebene definiert wird.
* Bei Verwendung der flexiblen Einbettungsmethode mit Breite und Höhe definierte Methode der Viewer-Einbettung. Siehe die Überschrift [Flexible Einbettung mit definierter Breite und Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Wenn Sie den Viewer in einem der oben aufgeführten Betriebsmodi verwenden, deaktivieren Sie die Funktion „Bild vorab laden“ mit dem Konfigurationsattribut &quot;`preloadImage`&quot;.

Außerdem wird das Vorabladen von Bildern nicht verwendet, auch wenn es in der Konfiguration aktiviert ist, wenn der Viewer in das DOM-Element eingebettet ist, mit `display:none` CSS-Einstellung ausgeblendet oder von der DOM-Struktur getrennt wird.
