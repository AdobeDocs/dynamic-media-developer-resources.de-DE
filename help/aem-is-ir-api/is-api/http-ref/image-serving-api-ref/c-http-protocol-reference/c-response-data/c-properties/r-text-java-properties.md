---
description: Wenn Text als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als Java-Eigenschaften lesbar sind.
solution: Experience Manager
title: Texteigenschaften (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Texteigenschaften (Java){#text-java-properties}

Wenn Text als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als Java-Eigenschaften lesbar sind.

Eine typische Antwort mit den Texteigenschaften hat diese allgemeine Struktur:

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

*`propertyValue`* kann leer sein. Leerzeichen sind am Anfang und Ende jeder Zeile sowie vor und nach dem Trennzeichen = optional. Einfache oder doppelte Anführungszeichen können zum Umschließen von Zeichenfolgenwerten verwendet werden, sind jedoch nicht erforderlich.

Zeichenfolgenwerte können Escape-Zeichen im JAVA-Stil enthalten, z. B. `\n`, `\t`, `\:` oder `\\`.
