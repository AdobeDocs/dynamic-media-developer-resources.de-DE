---
description: Wenn JavaScript als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als JavaScript-Include-Datei analysiert werden.
seo-description: Wenn JavaScript als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als JavaScript-Include-Datei analysiert werden.
seo-title: JavaScript-Eigenschaften
solution: Experience Manager
title: JavaScript-Eigenschaften
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# JavaScript-Eigenschaften{#javascript-properties}

Wenn JavaScript als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als JavaScript-Include-Datei analysiert werden.

Eine typische Antwort auf JavaScript-Eigenschaften hat folgende allgemeine Struktur:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* darf leer sein. Leerzeichen sind optional am Anfang und am Ende jeder Zeile und vor und nach dem Trennzeichen =. Alle Werte sind durch einfache Anführungszeichen eingeschlossen. Einfache Anführungszeichen in Zeichenfolgen werden mit zwei aufeinander folgenden einfachen Anführungszeichen versehen.

Um eine JavaScript-Eigenschaftenantwort zu analysieren, müssen alle Objekte, auf die in der Antwort verwiesen wird, erstellt werden, bevor die Eigenschaftendatei geladen wird. Im Folgenden finden Sie ein Beispiel für die Verwendung von `req=props` zum Abrufen der Antwortbildgröße in JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

