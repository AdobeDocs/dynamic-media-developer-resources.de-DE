---
description: Eigenschaftsdaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.
solution: Experience Manager
title: Eigenschaftsdaten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# Eigenschaftsdaten{#property-data}

Eigenschaftsdaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.

Eine Eigenschaft besteht aus einem Eigenschaftsnamen und einem Eigenschaftswert, getrennt durch = .

Mehrere Eigenschaften werden durch Trennlinien getrennt, die entweder `??` oder `<CR><LF>` sein können. Wenn die gesamte Eigenschaftendatenzeichenfolge nicht in Anführungszeichen gesetzt ist, ersetzt der Server jedes Vorkommen von `??` durch `<CR><LF>`, bevor er die Daten an den Client übermittelt. Eigenschaftsnamen können aus Buchstaben, Zahlen, &#39;.&#39;, &#39;-&#39; und &#39;_&#39; bestehen. Bei Eigenschaftsnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Eigenschaftswerte dürfen keine Trennlinien enthalten.

Siehe [Textzeichenfolge](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) für zusätzliche Regeln, die auf Eigenschaftendaten angewendet werden.
