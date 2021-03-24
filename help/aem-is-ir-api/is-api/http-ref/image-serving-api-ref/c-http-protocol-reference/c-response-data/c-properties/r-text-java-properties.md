---
description: Wenn Text als Antwortformat angegeben wird, werden die Antwortdaten als Java-Eigenschaften lesbar formatiert.
solution: Experience Manager
title: Eigenschaften von Text (Java)
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
