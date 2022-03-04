---
title: Variablenverarbeitung in eingebetteten ausländischen Anforderungen
description: $var$-Referenzen, die an einer beliebigen Stelle in den geschweiften Klammern einer eingebetteten ausländischen Anforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Variablenverarbeitung in eingebetteten ausländischen Anforderungen{#variable-processing-in-embedded-foreign-requests}

Alle `$var$` Verweise, die an einer beliebigen Stelle in den geschweiften Klammern einer eingebetteten ausländischen Anforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt.

Ermöglicht die Platzierung von eingebetteten ausländischen Anforderungen in einer Vorlage in einem Bildkatalog.

Variablenwerte, die in ausländische Anforderungen ersetzt werden sollen, müssen in der Regel doppelt kodiert sein, da keine Neukodierung angewendet wird, bevor der Server versucht, die endgültige ausländische URL zu übertragen.
