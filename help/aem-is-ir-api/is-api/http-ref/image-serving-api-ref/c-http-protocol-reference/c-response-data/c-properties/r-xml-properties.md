---
description: Wenn xml als Antwortformat angegeben ist, werden die Antwortdaten als XML-Dokument formatiert, das von jedem XML-Standardparser analysiert werden kann.
solution: Experience Manager
title: XML-Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# XML-Eigenschaften{#xml-properties}

Wenn xml als Antwortformat angegeben ist, werden die Antwortdaten als XML-Dokument formatiert, das von jedem XML-Standardparser analysiert werden kann.

Ein typisches Eigenschaftsantwort-Dokument weist folgende allgemeine Struktur auf:

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

Das Element `<prop-group>` wird als der äußere Container und für die Gruppierung von Eigenschaften verwendet. Wenn eine Gruppe benannt ist, entspricht der Name dem Java/JavaScript-Objektnamen.

>[!NOTE]
>
>Für einige `req=` -Typen kann eine Zeichenkodierung angegeben werden. Weitere Informationen finden Sie in der Beschreibung des jeweiligen `req=`Befehls.
