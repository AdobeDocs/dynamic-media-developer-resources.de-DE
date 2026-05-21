---
title: Materialien
description: Beim Bild-Rendering werden Materialien auf Gruppen oder Objekte in Vignetten angewendet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
TQID: 'https://experienceleague.adobe.com/MNCMxRxVGLF2rsr7NsuTGLzWxM9zkR42MI9MLdaW6G8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
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
