---
description: Beim Rendern von Bildern wird eine Größenbeschränkung von zwei Megapixeln für Vignetten ohne Pyramiden erzwungen.
solution: Experience Manager
title: Größenbeschränkung für Vignetten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# Größenbeschränkung für Vignetten{#vignette-size-limitation}

Beim Rendern von Bildern wird eine Größenbeschränkung von zwei Megapixeln für Vignetten ohne Pyramiden erzwungen.

Ändern Sie den Wert von `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf], wenn Ihre Anwendung Unterstützung für nicht-pyramid-Vignetten mit einem Bildbereich (Breite x Höhe) erfordert, der größer als dieser Grenzwert ist.

>[!NOTE]
>
>`attribute::MaxPix` und  `IS::MaxMessageSize` möglicherweise auch so angepasst werden müssen, dass ungewöhnlich große Antwortbildgrößen zugelassen werden. Weitere Informationen finden Sie in der Dokumentation zur Image-Serving .
