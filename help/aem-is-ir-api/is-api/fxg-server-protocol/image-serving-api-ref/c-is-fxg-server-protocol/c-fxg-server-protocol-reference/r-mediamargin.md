---
description: Festlegen des Medienrands. Legt den Medienrand fest, der in der PDF-Datei festgelegt wird.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Festlegen des Medienrands. Legt den Medienrand fest, der in der PDF-Datei festgelegt wird.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in Punkten

Standardmäßig ist die `mediaMargin` auf die volle Dokumentgröße eingestellt, die durch `viewWidth` und `viewHeight` definiert wird. Die Werte *[!DNL left]*, *[!DNL bottom]* und *[!DNL right]* werden standardmäßig auf den *[!DNL top]* Wert gesetzt, wenn sie nicht angegeben werden.
