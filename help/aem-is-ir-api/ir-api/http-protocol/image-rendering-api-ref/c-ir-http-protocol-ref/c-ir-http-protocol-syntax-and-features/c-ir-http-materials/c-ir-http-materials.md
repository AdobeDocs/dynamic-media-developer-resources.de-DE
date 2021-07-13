---
description: Beim Rendern von Bildern werden Materialien auf Gruppen oder Objekte in Vignetten angewendet.
solution: Experience Manager
title: Materialien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Materialien{#materials}

Beim Rendern von Bildern werden Materialien auf Gruppen oder Objekte in Vignetten angewendet.

Ein Material besteht aus einem Satz von *Attributen*. Einige Attribute sind für bestimmte Materialien erforderlich, andere sind optional und einige werden ignoriert, wenn sie vorhanden sind. Viele Attribute haben Standardwerte. Nicht alle Materialien können auf alle Objekte aufgebracht werden (z.B. ein Schachtmaterial kann nicht auf ein Sofa aufgebracht werden).

Alle Attribute, die innerhalb eines Materialspezifikations-Segments (MSS) auftreten, aber weder oben noch in den spezifischen Materialtabellen unten aufgeführt sind, werden vom Server ignoriert.

In den folgenden Tabellen sind die grundlegenden materiellen Attribute aufgeführt. IR unterstützt zusätzliche Attribute zur Steuerung von [erweiterten Rendereffekten](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Sofern nicht anders angegeben, sind alle materiellen Attribute optional mit geeigneten Standardwerten.

* [Feste Farben](r-ir-solid-colors.md)
* [Wiederholbare Texturen](r-ir-repeatable-textures.md)
* [Mauergrenzen](r-ir-wall-borders.md)
* [Dezimalzahlen](r-ir-decals.md)
* [Möbel](r-ir-cabinets.md)
* [Fensterverkleidungen](r-ir-window-coverings.md)
