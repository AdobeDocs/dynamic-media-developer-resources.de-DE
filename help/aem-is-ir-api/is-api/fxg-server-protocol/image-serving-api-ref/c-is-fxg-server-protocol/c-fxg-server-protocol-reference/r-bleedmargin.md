---
description: Anschnittrand einstellen. Legt den Anschnittrand fest, der in der PDF-Datei festgelegt ist.
solution: Experience Manager
title: Anzapfung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Anzapfung{#bleedmargin}

Anschnittrand einstellen. Legt den Anschnittrand fest, der in der PDF-Datei festgelegt ist.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in Punkten

Standardmäßig ist die `bleedMargin` auf die volle Dokumentgröße eingestellt, die durch `viewWidth` und `viewHeight` definiert wird. Die Werte *[!DNL left]*, *[!DNL bottom]* und *[!DNL right]* werden standardmäßig auf den *[!DNL top]* Wert gesetzt, wenn sie nicht angegeben werden.
