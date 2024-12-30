---
title: Eigenschaften
description: 'Eigenschaftendaten werden als Antwort auf die folgenden req=-Typen zurückgegeben: imageprops und props.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Eigenschaften{#properties}

Eigenschaftendaten werden als Antwort auf die folgenden req=-Typen zurückgegeben: imageprops und props.

Die Antwortdaten sind so formatiert, dass sie als Java™-Eigenschaften lesbar sind. Eine typische Antwort mit Texteigenschaften weist diese allgemeine Struktur auf:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

…

` *[!DNL propertyValue]*` darf leer sein. Leerzeichen sind am Anfang und am Ende jeder Zeile sowie vor und nach dem Trennzeichen &quot;=&quot; optional. Zum Einschließen von Zeichenfolgenwerten können einfache oder doppelte Anführungszeichen verwendet werden, sie sind jedoch nicht erforderlich.

Zeichenfolgenwerte können JAVA-Escape-Zeichen enthalten, z. B. `\n`, `\t`, `\:` oder `\\`.

**Siehe auch**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
