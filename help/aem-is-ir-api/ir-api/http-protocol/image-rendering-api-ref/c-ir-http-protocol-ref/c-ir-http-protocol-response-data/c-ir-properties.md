---
title: Eigenschaften
description: 'Eigenschaftendaten werden als Antwort auf die folgenden req=-Typen zurückgegeben: imageprops und props.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
TQID: 'https://experienceleague.adobe.com/AIeKRT2-o9Z35SjXjrGECIWHFLRrdJz5JO-CkCOLj8U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# Eigenschaften{#properties}

Eigenschaftendaten werden als Antwort auf die folgenden req=-Typen zurückgegeben: imageprops und props.

Die Antwortdaten sind so formatiert, dass sie als Java™-Eigenschaften lesbar sind. Eine typische Antwort mit Texteigenschaften weist diese allgemeine Struktur auf:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` darf leer sein. Leerzeichen sind am Anfang und am Ende jeder Zeile sowie vor und nach dem Trennzeichen &quot;=&quot; optional. Zum Einschließen von Zeichenfolgenwerten können einfache oder doppelte Anführungszeichen verwendet werden, sie sind jedoch nicht erforderlich.

Zeichenfolgenwerte können JAVA-Escape-Zeichen enthalten, z. B. `\n`, `\t`, `\:` oder `\\`.

**Siehe auch**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
