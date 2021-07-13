---
description: Wenn JavaScript™ als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als JavaScript™-Include-Datei analysiert werden.
solution: Experience Manager
title: JavaScript™-Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# JavaScript™-Eigenschaften{#javascript-properties}

Wenn JavaScript™ als Antwortformat angegeben ist, werden die Antwortdaten so formatiert, dass sie als JavaScript™-Include-Datei analysiert werden.

Eine typische JavaScript™-Eigenschaftenantwort weist folgende allgemeine Struktur auf:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* kann leer sein. Leerzeichen sind am Anfang und Ende jeder Zeile sowie vor und nach dem Trennzeichen = optional. Alle Werte sind durch einfache Anführungszeichen eingeschlossen. Einzelne Anführungszeichen in Zeichenfolgen werden mit zwei aufeinander folgenden einfachen Anführungszeichen maskiert.

Um eine JavaScript™-Eigenschaftenantwort zu analysieren, müssen alle Objekte oder Objekte, auf die in der Antwort verwiesen wird, erstellt werden, bevor die Eigenschaftendatei geladen wird. Im Folgenden finden Sie ein Beispiel für die Verwendung von `req=props` zum Abrufen der Größe des Antwortbilds in JavaScript™:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
