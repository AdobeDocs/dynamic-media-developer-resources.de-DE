---
description: Wenn xml als Antwortformat angegeben ist, werden die Antwortdaten als XML-Dokument formatiert, das von jedem XML-Standardparser analysiert werden kann.
seo-description: Wenn xml als Antwortformat angegeben ist, werden die Antwortdaten als XML-Dokument formatiert, das von jedem XML-Standardparser analysiert werden kann.
seo-title: XML-Eigenschaften
solution: Experience Manager
title: XML-Eigenschaften
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# XML-Eigenschaften{#xml-properties}

Wenn xml als Antwortformat angegeben ist, werden die Antwortdaten als XML-Dokument formatiert, das von jedem XML-Standardparser analysiert werden kann.

Ein typisches Dokument für die Reaktion auf Eigenschaften weist folgende allgemeine Struktur auf:

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

Das `<prop-group>`-Element wird als äußerer Container und zur Gruppierung von Eigenschaften verwendet. Wenn eine Gruppe benannt ist, entspricht der Name dem Java/JavaScript-Objektnamen.

>[!NOTE]
>
>Die Zeichenkodierung kann für einige `req=`-Typen angegeben werden. Weitere Informationen finden Sie in der Beschreibung des spezifischen Befehls `req=`.

