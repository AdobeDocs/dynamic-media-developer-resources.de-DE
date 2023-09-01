---
title: Größenbeschränkung für Vignetten
description: Beim Rendern von Bildern wird eine Größenbeschränkung von zwei Megapixeln für Vignetten ohne Pyramid erzwungen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Größenbeschränkung für Vignetten{#vignette-size-limitation}

Beim Rendern von Bildern wird eine Größenbeschränkung von zwei Megapixeln für Vignetten ohne Pyramid erzwungen.

Ändern Sie den Wert von `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] , wenn Ihre Anwendung Unterstützung für Nicht-Pyramid-Vignetten mit einem Bildbereich (Breite x Höhe) erfordert, der größer als diese Grenze ist.

>[!NOTE]
>
>Attribute anpassen `attribute::MaxPix` und `IS::MaxMessageSize` um ungewöhnlich große Antwortbildgrößen zuzulassen. Weitere Informationen finden Sie in der Dokumentation zur Image-Serving .
