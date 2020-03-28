---
description: Es werden vier allgemeine Typen von Produktionsvignetten unterstützt.
seo-description: Es werden vier allgemeine Typen von Produktionsvignetten unterstützt.
seo-title: Vignettenskalierung
solution: Experience Manager
title: Vignettenskalierung
topic: Scene7 Image Serving - Image Rendering API
uuid: 08c8f826-7dce-4bcb-9323-4892262eb578
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Vignettenskalierung{#vignette-scaling}

Es werden vier allgemeine Typen von Produktionsvignetten unterstützt.

* Einzelauflösung

   Wird nur empfohlen, wenn sichergestellt ist, dass nur eine einzige Render-Bildgröße erforderlich ist.
* Mehrere Auflösungen

   Wird empfohlen, wenn alle gewünschten Render-Bildgrößen bekannt sind. Bietet bessere Qualität und schnelleres Rendering als bei Vignetten mit einer Auflösung und Pyramide, da das Bild nach dem Rendering nicht skaliert werden muss.
* Pyramide

   Dies ist der beste Zweck, der empfohlen wird, wenn mehrere Bildgrößen benötigt werden und die genauen Größen nicht vorab bestimmt werden und wenn einer der Flash-Zoom-Viewer von Scene7 verwendet wird.
* Pyramide mit einer oder mehreren zusätzlichen Auflösungen

   Bietet hohe Qualität für bestimmte Größen und bietet gleichzeitig Flexibilität und Unterstützung für Zoom-Viewer.

Jede Auflösung wird als unabhängige Ansicht mit eigener Bildbreite und -höhe in der Produktionsvignette gespeichert.

Die Größe der Ansicht einer Vignette mit einer Auflösung wird entweder mit `-width` oder `-height` oder mit beiden angegeben. Wenn beide Werte angegeben sind, wird die Vignette so skaliert, dass keine der beiden Dimensionen größer als die angegebene Größe ist. Wenn keiner der Werte angegeben ist, hat die Ausgabevignette dieselbe Größe wie die Eingabebild-Vignette. Es wird keine Vergrößerung angewendet. Wenn die angegebene Größe die Größe der Vignette für die Eingabe überschreitet, hat die Vignette dieselbe Größe wie die Vignette für die Eingabe.

Die gleichen Regeln gelten für Vignetten mit mehreren Auflösungen, wobei die erste Auflösungsebene genau wie eine Vignette mit einer einzelnen Auflösung skaliert wird. Die zusätzlichen Auflösungen werden mit zusätzlichen kommagetrennten Werten für entweder `-width` oder `-height`angegeben. Werte müssen nicht sortiert werden. Wenn mehrere Werte `-width` angegeben sind, muss `-height` nur ein Wert angegeben werden, andernfalls wird ein Fehler zurückgegeben.

Eine Pyramidenvignette wird durch Angabe `-pyramid`erstellt. Die höchste Auflösungsstufe einer solchen Vignette wird genau wie bei einer Vignette mit nur einer Auflösung festgelegt. Die zusätzlichen Auflösungsstufen werden automatisch bestimmt, indem jede Ebene auf das 0,5-fache der vorherigen Ebene skaliert wird, wobei der kleinste Wert 128 x 128 Pixel nicht überschreiten darf.

Für eine Pyramidenvignette können zusätzliche Auflösungsstufen festgelegt werden, genau wie für eine Vignette mit mehreren Auflösungen.
