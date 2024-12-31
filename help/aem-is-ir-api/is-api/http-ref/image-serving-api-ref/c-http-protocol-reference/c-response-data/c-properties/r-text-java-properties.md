---
description: Wenn Text als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als Java-Eigenschaften lesbar sind.
solution: Experience Manager
title: Text (Java)-Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Text (Java)-Eigenschaften{#text-java-properties}

Wenn Text als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als Java-Eigenschaften lesbar sind.

Eine typische Antwort mit Texteigenschaften weist diese allgemeine Struktur auf:

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* darf leer sein. Leerzeichen sind am Anfang und am Ende jeder Zeile sowie vor und nach dem Trennzeichen = optional. Zum Einschließen von Zeichenfolgenwerten können einfache oder doppelte Anführungszeichen verwendet werden, sie sind jedoch nicht erforderlich.

Zeichenfolgenwerte können JAVA-Escape-Zeichen enthalten, z. B. `\n`, `\t`, `\:` oder `\\`.
