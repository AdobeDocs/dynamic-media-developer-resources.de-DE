---
title: Materialien
description: Beim Bild-Rendering werden Materialien auf Gruppen oder Objekte in Vignetten angewendet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Materialien{#materials}

Beim Bild-Rendering werden Materialien auf Gruppen oder Objekte in Vignetten angewendet.

Ein Material besteht aus einer Reihe von *Attributen*. Einige Attribute sind für bestimmte Materialien erforderlich, andere sind optional und einige werden ignoriert, falls vorhanden. Viele Attribute haben Standardwerte. Nicht alle Materialien können auf alle Objekte angewendet werden (beispielsweise kann ein Schrankmaterial nicht auf ein Sofa angewendet werden).

Alle Attribute, die innerhalb eines Materialspezifikationssegments (MSS) auftreten, aber oben oder in den spezifischen Materialtabellen unten nicht aufgeführt sind, werden vom Server ignoriert.

In der folgenden Tabelle sind die grundlegenden Materialattribute aufgeführt. IR unterstützt zusätzliche Attribute zur Steuerung [erweiterter Render-Effekte](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Sofern nicht anders angegeben, sind alle Materialattribute optional und mit geeigneten Standardwerten versehen.

* [Volltonfarben](r-ir-solid-colors.md)
* [Wiederholbare Texturen](r-ir-repeatable-textures.md)
* [Wandränder](r-ir-wall-borders.md)
* [Abziehbilder](r-ir-decals.md)
* [Schränke](r-ir-cabinets.md)
* [Fensterverkleidungen](r-ir-window-coverings.md)
