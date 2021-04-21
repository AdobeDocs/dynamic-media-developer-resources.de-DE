---
description: Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.
solution: Experience Manager
title: Begrenzung der Vignettengröße
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Begrenzung der Vignettengröße{#vignette-size-limitation}

Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.

Ändern Sie den Wert von `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf], wenn Ihre Anwendung Unterstützung für Nicht-Pyramidenvignetten mit einem Bildbereich (Breite x Höhe) erfordert, der größer als dieser Grenzwert ist.

>[!NOTE]
>
>`attribute::MaxPix` und  `IS::MaxMessageSize` ggf. auch angepasst werden müssen, um ungewöhnlich große Antwortbildgrößen zu ermöglichen. Weitere Informationen finden Sie in der Dokumentation zum Image-Server.

