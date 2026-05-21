---
title: Variablenverarbeitung in eingebetteten Fremdanforderungen
description: $var$-Verweise, die an einer beliebigen Stelle in den geschweiften Klammern einer eingebetteten Fremdanforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# Variablenverarbeitung in eingebetteten Fremdanforderungen{#variable-processing-in-embedded-foreign-requests}

Alle `$var$` Verweise, die an einer beliebigen Stelle innerhalb der geschweiften Klammern einer eingebetteten Fremdanforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt.

Ermöglicht die Platzierung von eingebetteten Fremdanfragen in einer Vorlage in einem Bildkatalog.

Variablenwerte, die in fremde Anforderungen ersetzt werden sollen, müssen in der Regel doppelt kodiert werden, da keine erneute Kodierung erfolgt, bevor der Server versucht, die endgültige fremde URL zu übertragen.
