---
description: Es werden vier allgemeine Arten von Produktionsvignetten unterstützt.
solution: Experience Manager
title: Vignettenskalierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Vignettenskalierung{#vignette-scaling}

Es werden vier allgemeine Arten von Produktionsvignetten unterstützt.

* einfach aufgelöst

  Wird nur empfohlen, wenn sichergestellt ist, dass nur eine einzige Render-Bildgröße erforderlich ist.
* Multiauflösung

  Wird empfohlen, wenn alle gewünschten Render-Bildgrößen bekannt sind. Bietet eine bessere Qualität und schnelleres Rendering als Einzelauflösungs- und Pyramidenvignetten, da das Bild nach dem Rendering nicht skaliert werden muss.
* Pyramide

  Am besten geeignet. Wird empfohlen, wenn mehrere Bildgrößen erforderlich sind und die genauen Größen nicht vorab festgelegt sind und wenn der Dynamic Media Zoom-Viewer verwendet wird.
* Pyramide mit einer oder mehreren zusätzlichen Auflösungen

  Bietet hohe Qualität für bestimmte Größen und bietet dennoch Flexibilität und Zoom-Viewer-Unterstützung.

Effektiv wird jede Auflösung in der Produktionsvignette als unabhängige Ansicht mit eigener Bildbreite und -höhe gespeichert.

Die Ansichtsgröße einer Vignette mit einfacher Auflösung wird mit entweder `-width` oder `-height` oder beiden angegeben. Wenn beide Werte angegeben sind, wird die Vignette so skaliert, dass keine der Dimensionen größer als die angegebene Größe ist. Wenn keiner der Werte angegeben ist, hat die Ausgabe-Vignette dieselbe Größe wie die Eingabe-Vignette. Es wird kein Hochskalieren angewendet. Wenn die angegebene Größe größer ist als die Größe der Eingabevignette, hat die Ausgabevignette dieselbe Größe wie die Eingabevignette.

Effektiv gelten dieselben Regeln für Vignetten mit mehreren Auflösungen, wobei die erste Auflösungsebene genau wie eine Vignette mit einer einzigen Auflösung dimensioniert ist. Die zusätzlichen Auflösungen werden mit zusätzlichen kommagetrennten Werten für `-width` oder `-height` angegeben. Die Werte müssen nicht sortiert werden. Wenn `-width` mehrere Werte angibt, dürfen `-height` nur einen einzigen Wert bereitstellen und umgekehrt. Andernfalls wird ein Fehler zurückgegeben.

Eine Pyramidenvignette wird durch Angabe von `-pyramid` erstellt. Der größte Auflösungspegel einer solchen Vignette wird genau wie bei einer Vignette mit einfacher Auflösung bestimmt. Die zusätzlichen Auflösungsstufen werden automatisch bestimmt, indem jeder Pegel auf das 0,5fache des vorherigen Niveaus skaliert wird, wobei der kleinste Pegel 128x128 Pixel nicht überschreitet.

Für eine Pyramidenvignette können zusätzliche Auflösungsstufen festgelegt werden, ebenso wie für eine Vignette mit mehreren Auflösungen.
