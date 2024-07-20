---
title: Scene-Koordinaten
description: Über den Koordinatenraum der Szene können die Größen und Entfernungen der texturierbaren Objektflächen festgelegt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Scene-Koordinaten{#scene-coordinates}

Über den Koordinatenraum der Szene können die Größen und Entfernungen der texturierbaren Objektflächen festgelegt werden.

Da es sich bei den meisten Vignetten um reale Szenen handelt, die physische Objekte darstellen, werden die meisten Vignetten mit Zoll als Einheiten für den Koordinatenraum der Szene erstellt. Es können auch andere Einheiten wie mm oder cm verwendet werden. Das Bild-Rendering unterstützt keine Konvertierung von Einheiten.

Die folgenden Befehle akzeptieren Werte im Koordinatenraum der Szene:

* [grout=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
