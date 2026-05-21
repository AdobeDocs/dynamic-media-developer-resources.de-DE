---
description: Wenn Text als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als Java-Eigenschaften lesbar sind.
solution: Experience Manager
title: Text (Java)-Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 100
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
