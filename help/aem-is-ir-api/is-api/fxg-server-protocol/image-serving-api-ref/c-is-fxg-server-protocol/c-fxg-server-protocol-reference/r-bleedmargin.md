---
description: Legen Sie den Anschnittrand fest. Legt den in der PDF-Datei festgelegten Anschnittrand fest.
solution: Experience Manager
title: bleedmargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# bleedmargin{#bleedmargin}

Legen Sie den Anschnittrand fest. Legt den in der PDF-Datei festgelegten Anschnittrand fest.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in

Standardmäßig ist `bleedMargin` auf die vollständige Größe des Dokuments eingestellt, das durch `viewWidth` und `viewHeight` definiert wird. Die Werte *[!DNL left]*, *[!DNL bottom]* und *[!DNL right]* werden standardmäßig auf den Wert *[!DNL top]* gesetzt, falls nicht anders angegeben.
