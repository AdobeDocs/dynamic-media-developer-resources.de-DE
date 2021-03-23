---
description: Wenn Text als Antwortformat angegeben wird, werden die Antwortdaten als Java-Eigenschaften lesbar formatiert.
seo-description: Wenn Text als Antwortformat angegeben wird, werden die Antwortdaten als Java-Eigenschaften lesbar formatiert.
seo-title: Eigenschaften von Text (Java)
solution: Experience Manager
title: Eigenschaften von Text (Java)
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# Texteigenschaften (Java){#text-java-properties}

Wenn Text als Antwortformat angegeben wird, werden die Antwortdaten als Java-Eigenschaften lesbar formatiert.

Eine typische Antwort auf Texteigenschaften hat folgende allgemeine Struktur:

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

*`propertyValue`* darf leer sein. Leerzeichen sind optional am Anfang und am Ende jeder Zeile und vor und nach dem Trennzeichen =. Ein- oder Dublette-Anführungszeichen können zum Umschließen von Zeichenfolgenwerten verwendet werden, sind jedoch nicht erforderlich.

Zeichenfolgenwerte können Escape-Zeichen im JAVA-Stil enthalten, z. B. `\n`, `\t`, `\:` oder `\\`.
