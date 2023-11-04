---
description: Eigenschaftendaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.
solution: Experience Manager
title: Eigenschaftendaten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# Eigenschaftendaten{#property-data}

Eigenschaftendaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.

Eine Eigenschaft besteht aus einem Eigenschaftsnamen und einem Eigenschaftswert, getrennt durch =.

Mehrere Eigenschaften werden durch Zeilentrennzeichen getrennt, die entweder `??` oder `<CR><LF>`. Wenn die gesamte Eigenschaftendatenzeichenfolge nicht in Anführungszeichen eingeschlossen ist, ersetzt der Server jedes Vorkommen von `??` mit `<CR><LF>` vor der Übermittlung der Daten an den Client. Eigenschaftsnamen können aus Buchstaben, Zahlen, &#39;.&#39;, &#39;-&#39; und &#39;_&#39; bestehen. Bei Eigenschaftsnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Eigenschaftswerte dürfen keine Zeilentrennzeichen enthalten.

Siehe [Textzeichenfolge](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) für zusätzliche Regeln, die auf Eigenschaftsdaten angewendet werden.
