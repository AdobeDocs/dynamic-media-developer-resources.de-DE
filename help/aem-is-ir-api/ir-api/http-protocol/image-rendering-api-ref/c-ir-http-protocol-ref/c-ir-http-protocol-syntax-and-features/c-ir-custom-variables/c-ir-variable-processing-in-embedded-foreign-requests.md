---
title: Variablenverarbeitung in eingebetteten Fremdanforderungen
description: $var$-Verweise, die an einer beliebigen Stelle in den geschweiften Klammern einer eingebetteten Fremdanforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Variablenverarbeitung in eingebetteten Fremdanforderungen{#variable-processing-in-embedded-foreign-requests}

Alle `$var$` Verweise, die an einer beliebigen Stelle innerhalb der geschweiften Klammern einer eingebetteten Fremdanforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt.

Ermöglicht die Platzierung von eingebetteten Fremdanfragen in einer Vorlage in einem Bildkatalog.

Variablenwerte, die in fremde Anforderungen ersetzt werden sollen, müssen in der Regel doppelt kodiert werden, da keine erneute Kodierung erfolgt, bevor der Server versucht, die endgültige fremde URL zu übertragen.
