---
description: Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.
seo-description: Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.
seo-title: Begrenzung der Vignettengröße
solution: Experience Manager
title: Begrenzung der Vignettengröße
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Begrenzung der Vignettengröße{#vignette-size-limitation}

Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.

Ändern Sie den Wert von `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf], wenn Ihre Anwendung Unterstützung für Nicht-Pyramidenvignetten mit einem Bildbereich (Breite x Höhe) erfordert, der größer als dieser Grenzwert ist.

>[!NOTE]
>
>`attribute::MaxPix` und  `IS::MaxMessageSize` ggf. auch angepasst werden müssen, um ungewöhnlich große Antwortbildgrößen zu ermöglichen. Weitere Informationen finden Sie in der Dokumentation zum Image-Server.

