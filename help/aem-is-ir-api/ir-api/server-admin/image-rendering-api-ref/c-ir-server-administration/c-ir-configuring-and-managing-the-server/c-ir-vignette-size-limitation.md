---
title: Größenbeschränkung der Vignette
description: Das Bild-Rendering erzwingt eine Größenbegrenzung von zwei Megapixeln für Nicht-Pyramiden-Vignetten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Größenbeschränkung der Vignette{#vignette-size-limitation}

Das Bild-Rendering erzwingt eine Größenbegrenzung von zwei Megapixeln für Nicht-Pyramiden-Vignetten.

Ändern Sie den Wert von `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf], wenn Ihre Anwendung die Unterstützung für Nicht-Pyramidenvignetten mit einem Bildbereich (Breite x Höhe) erfordert, der größer als dieser Grenzwert ist.

>[!NOTE]
>
>Passen Sie die Attribute `attribute::MaxPix` und `IS::MaxMessageSize` an, um ungewöhnlich große Antwortbildgrößen zu ermöglichen. Weitere Informationen finden Sie in der Dokumentation zu Image-Serving .
