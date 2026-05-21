---
description: Anschnittrand einstellen. Legt den Anschnittrand fest, der in der PDF-Datei festgelegt ist.
solution: Experience Manager
title: Anzapfung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
TQID: 'https://experienceleague.adobe.com/Lghb-4jpksjewoUjBD-SE9UqsD6AX6WFwb2sbkCobXE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 0%

---

# Anzapfung{#bleedmargin}

Anschnittrand einstellen. Legt den Anschnittrand fest, der in der PDF-Datei festgelegt ist.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in Punkten

Standardmäßig ist die `bleedMargin` auf die volle Dokumentgröße eingestellt, die durch `viewWidth` und `viewHeight` definiert wird. Die Werte *[!DNL left]*, *[!DNL bottom]* und *[!DNL right]* werden standardmäßig auf den *[!DNL top]* Wert gesetzt, wenn sie nicht angegeben werden.
