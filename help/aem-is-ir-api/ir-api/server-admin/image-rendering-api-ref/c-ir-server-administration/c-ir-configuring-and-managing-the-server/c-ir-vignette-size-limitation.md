---
description: Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.
seo-description: Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.
seo-title: Begrenzung der Vignettengröße
solution: Experience Manager
title: Begrenzung der Vignettengröße
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Begrenzung der Vignettengröße{#vignette-size-limitation}

Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.

Ändern Sie den Wert von `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf], wenn Ihre Anwendung Unterstützung für Nicht-Pyramidenvignetten mit einem Bildbereich (Breite x Höhe) erfordert, der größer als dieser Grenzwert ist.

>[!NOTE]
>
>`attribute::MaxPix` und  `IS::MaxMessageSize` ggf. auch angepasst werden müssen, um ungewöhnlich große Antwortbildgrößen zu ermöglichen. Weitere Informationen finden Sie in der Dokumentation zum Image-Server.

