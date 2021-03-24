---
description: Eigenschaftsdaten werden als Antwort auf die folgenden req=-Typen imageprops und props zurückgegeben.
solution: Experience Manager
title: Eigenschaften
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---


# Eigenschaften{#properties}

Eigenschaftendaten werden als Antwort auf die folgenden Typen von req= zurückgegeben: imageprops und props.

Die Antwortdaten sind so formatiert, dass sie als Java-Eigenschaften lesbar sind. Eine typische Antwort auf Texteigenschaften hat folgende allgemeine Struktur:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` darf leer sein. Leerzeichen sind optional am Anfang und am Ende jeder Zeile und vor und nach dem Trennzeichen &#39;=&#39;. Ein- oder Dublette-Anführungszeichen können zum Umschließen von Zeichenfolgenwerten verwendet werden, sind jedoch nicht erforderlich.

Zeichenfolgenwerte können Escape-Zeichen im JAVA-Stil enthalten, z. B. `\n`, `\t`, `\:`. oder `\\`.

**Verwandte Themen**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
