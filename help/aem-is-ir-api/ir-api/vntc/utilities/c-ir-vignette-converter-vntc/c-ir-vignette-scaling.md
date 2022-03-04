---
description: Es werden vier allgemeine Arten von Produktionsvignetten unterstützt.
solution: Experience Manager
title: Vignettenskalierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Vignettenskalierung{#vignette-scaling}

Es werden vier allgemeine Arten von Produktionsvignetten unterstützt.

* Einzelauflösung

   Wird nur empfohlen, wenn sicher ist, dass nur eine einzelne Renderbildgröße erforderlich ist.
* Mehrfachauflösung

   Wird empfohlen, wenn alle gewünschten Renderbildgrößen bekannt sind. Bietet eine bessere Qualität und schnelleres Rendering als Single-Resolution- und Pyramid-Vignetten, da das Bild nach dem Rendering nicht skaliert werden muss.
* Pyramide

   Am besten geeignet, wenn mehrere Bildgrößen erforderlich sind, die genauen Größen nicht vorab bestimmt werden und der Dynamic Media-Zoom-Viewer verwendet wird.
* Pyramid mit einer oder mehreren zusätzlichen Auflösungen

   Bietet hohe Qualität für bestimmte Größen und bietet gleichzeitig Flexibilität und Zoom-Viewer-Unterstützung.

Jede Auflösung wird tatsächlich in der Produktionsvignette als unabhängige Ansicht mit eigener Bildbreite und -höhe gespeichert.

Die Ansichtsgröße einer Vignette mit einer Auflösung wird entweder durch `-width` oder `-height` oder beides. Wenn beide Werte angegeben sind, wird die Vignette so skaliert, dass keine Dimension größer als die angegebene Größe ist. Wenn keiner der Werte angegeben ist, hat die Ausgabemignette dieselbe Größe wie die Eingabevignette. Es wird keine Vergrößerung vorgenommen. Wenn die angegebene Größe größer als die Größe der Vignette ist, hat die Vignette die gleiche Größe wie die Vignette.

Die gleichen Regeln gelten für Vignetten mit mehreren Auflösungen, wobei die erste Auflösungsebene wie eine Vignette mit nur einer Auflösung skaliert wird. Die zusätzlichen Auflösungen werden mit zusätzlichen kommagetrennten Werten für `-width` oder `-height`. Werte müssen nicht sortiert werden. Wenn `-width` gibt mehrere Werte an, dann `-height` darf nur einen einzigen Wert bereitstellen und umgekehrt. Andernfalls wird ein Fehler zurückgegeben.

Eine Pyramidenvignette wird durch Angabe von `-pyramid`. Die größte Auflösungsebene einer solchen Vignette wird genau wie bei einer Vignette mit nur einer Auflösung bestimmt. Die zusätzlichen Auflösungsebenen werden automatisch bestimmt, indem jeder Level auf das 0,5-fache der vorherigen Ebene skaliert wird, wobei der kleinste Wert 128 x 128 Pixel nicht überschreiten darf.

Wie bei einer Vignette mit mehreren Auflösungen können für eine Pyramidenvignette zusätzliche Auflösungsstufen angegeben werden.
