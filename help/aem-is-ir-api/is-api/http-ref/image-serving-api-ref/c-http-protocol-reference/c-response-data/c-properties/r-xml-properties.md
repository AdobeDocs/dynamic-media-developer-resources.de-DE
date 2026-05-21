---
description: Wenn xml als Antwortformat angegeben ist, werden die Antwortdaten als XML-Dokument formatiert, das von jedem standardmäßigen XML-Parser geparst werden kann.
solution: Experience Manager
title: XML-Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
TQID: 'https://experienceleague.adobe.com/Nljy83DDIbeY6l-d6F02NlaFzyCFJny7iesxnF9mFyo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 0%

---

# XML-Eigenschaften{#xml-properties}

Wenn xml als Antwortformat angegeben ist, werden die Antwortdaten als XML-Dokument formatiert, das von jedem standardmäßigen XML-Parser geparst werden kann.

Ein typisches Eigenschaftenantwortdokument weist diese allgemeine Struktur auf:

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

Das `<prop-group>`-Element wird als äußerster Container und für die Gruppierung von Eigenschaften verwendet. Wenn eine Gruppe benannt ist, entspricht der Name dem Java-/JavaScript-Objektnamen.

>[!NOTE]
>
>Die Zeichenkodierung kann für einige `req=` angegeben werden. Weitere Informationen finden Sie in der Beschreibung `req=` spezifischen Befehls .
