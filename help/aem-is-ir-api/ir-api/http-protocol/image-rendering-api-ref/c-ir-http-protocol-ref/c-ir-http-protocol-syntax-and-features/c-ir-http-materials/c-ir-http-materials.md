---
description: Beim Rendern von Bildern werden Materialien auf Gruppen oder Objekte in Vignetten angewendet.
solution: Experience Manager
title: Materialien
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Materialien{#materials}

Beim Rendern von Bildern werden Materialien auf Gruppen oder Objekte in Vignetten angewendet.

Ein Material besteht aus einem Satz von *Attributen*. Einige Attribute sind für bestimmte Materialien erforderlich, andere sind optional und einige werden ignoriert, wenn sie vorhanden sind. Viele Attribute haben Standardwerte. Nicht alle Materialien können auf alle Objekte aufgetragen werden (z.B. kann kein Schrankmaterial auf ein Sofa aufgetragen werden).

Alle Attribute, die innerhalb eines Materialspezifikationssegments (MSS) auftreten, aber weder oben noch in den spezifischen Materialtabellen unten aufgeführt sind, werden vom Server ignoriert.

In den folgenden Tabellen werden die grundlegenden Materialattribute Liste. IR unterstützt zusätzliche Attribute zur Steuerung von [erweiterten Rendereffekten](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Sofern nicht anders angegeben, sind alle Materialattribute optional mit geeigneten Standardwerten.

* [Feste Farben](r-ir-solid-colors.md)
* [Wiederholbare Texturen](r-ir-repeatable-textures.md)
* [Mauergrenzen](r-ir-wall-borders.md)
* [Dezimalstellen](r-ir-decals.md)
* [Möbel](r-ir-cabinets.md)
* [Fensterbeläge](r-ir-window-coverings.md)
