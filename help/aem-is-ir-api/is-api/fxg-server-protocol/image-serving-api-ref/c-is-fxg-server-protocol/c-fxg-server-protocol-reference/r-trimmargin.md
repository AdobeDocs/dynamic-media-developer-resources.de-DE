---
description: Legt den Trimmrand fest. Legt den in der PDF-Datei festgelegten Trimmrand fest.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

Legt den Trimmrand fest. Legt den in der PDF-Datei festgelegten Trimmrand fest.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in Punkten

Standardmäßig ist der `trimMargin` auf die volle Dokumentgröße eingestellt, die durch `viewWidth` und `viewHeight` definiert wird. Die Werte *[!DNL left]*, *[!DNL bottom]* und *[!DNL right]* werden standardmäßig auf den Wert *[!DNL top]* gesetzt, falls nicht angegeben.
