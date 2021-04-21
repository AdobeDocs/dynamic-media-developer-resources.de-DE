---
description: Wenn JavaScript™ als Antwortformat angegeben ist, werden die Antwortdaten als JavaScript™-Include-Datei analysiert.
solution: Experience Manager
title: JavaScript™-Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# JavaScript™-Eigenschaften{#javascript-properties}

Wenn JavaScript™ als Antwortformat angegeben ist, werden die Antwortdaten als JavaScript™-Include-Datei analysiert.

Eine typische Antwort auf JavaScript™-Eigenschaften weist folgende allgemeine Struktur auf:

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

Um eine JavaScript™-Eigenschaftenantwort zu analysieren, müssen alle Objekte oder Objekte, auf die in der Antwort verwiesen wird, erstellt werden, bevor die Eigenschaftendatei geladen wird. Im Folgenden finden Sie ein Beispiel für die Verwendung von `req=props` zum Abrufen der Antwortbildgröße in JavaScript™:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

