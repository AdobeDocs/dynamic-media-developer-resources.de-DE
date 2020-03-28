---
description: Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.
seo-description: Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.
seo-title: Begrenzung der Vignettengröße
solution: Experience Manager
title: Begrenzung der Vignettengröße
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Begrenzung der Vignettengröße{#vignette-size-limitation}

Beim Image Rendering wird eine Größenbeschränkung von zwei Megapixeln für nicht pyramidenförmige Vignetten erzwungen.

Ändern Sie den Wert von `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf], wenn Ihre Anwendung Unterstützung für nicht-pyramidale Vignetten mit einem Bildbereich (Breite x Höhe) erfordert, der größer als dieser Grenzwert ist.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>`attribute::MaxPix` und `IS::MaxMessageSize` ggf. auch angepasst werden müssen, um ungewöhnlich große Antwortbildgrößen zu ermöglichen. Weitere Informationen finden Sie in der Dokumentation zum Image-Server.

