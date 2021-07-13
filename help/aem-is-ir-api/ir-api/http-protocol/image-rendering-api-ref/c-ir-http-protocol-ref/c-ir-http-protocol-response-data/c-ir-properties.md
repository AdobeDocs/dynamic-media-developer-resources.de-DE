---
description: Eigenschaftsdaten werden als Reaktion auf die folgenden req=-Typen imageprops und props zurückgegeben.
solution: Experience Manager
title: Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---

# Eigenschaften{#properties}

Eigenschaftsdaten werden als Antwort auf die folgenden req=-Typen zurückgegeben: imageprops und props.

Die Antwortdaten sind so formatiert, dass sie als Java-Eigenschaften lesbar sind. Eine typische Antwort mit den Texteigenschaften hat diese allgemeine Struktur:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` kann leer sein. Leerzeichen sind am Anfang und Ende jeder Zeile sowie vor und nach dem Trennzeichen &#39;=&#39; optional. Einfache oder doppelte Anführungszeichen können zum Umschließen von Zeichenfolgenwerten verwendet werden, sind jedoch nicht erforderlich.

Zeichenfolgenwerte können Escape-Zeichen im JAVA-Stil enthalten, z. B. `\n`, `\t`, `\:`. oder `\\`.

**Verwandte Themen**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
