---
description: Eigenschaftsdaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.
solution: Experience Manager
title: Eigenschaftsdaten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# Eigenschaftsdaten{#property-data}

Eigenschaftsdaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.

Eine Eigenschaft besteht aus einem Eigenschaftsnamen und einem Eigenschaftswert, getrennt durch = .

Mehrere Eigenschaften werden durch Trennlinien getrennt, die entweder `??` oder `<CR><LF>` sein können. Wenn die gesamte Eigenschaftendatenzeichenfolge nicht in Anführungszeichen gesetzt ist, ersetzt der Server jedes Vorkommen von `??` durch `<CR><LF>`, bevor er die Daten an den Client übermittelt. Eigenschaftsnamen können aus Buchstaben, Zahlen, &#39;.&#39;, &#39;-&#39; und &#39;_&#39; bestehen. Bei Eigenschaftsnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Eigenschaftswerte dürfen keine Trennlinien enthalten.

Siehe [Textzeichenfolge](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) für zusätzliche Regeln, die auf Eigenschaftendaten angewendet werden.
