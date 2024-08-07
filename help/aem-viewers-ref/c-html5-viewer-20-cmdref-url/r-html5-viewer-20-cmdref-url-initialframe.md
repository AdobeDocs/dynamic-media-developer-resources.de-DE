---
title: initialFrame
description: Parameter, die allen Viewern gemeinsam sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# initialFrame{#initialframe}

Parameter, die allen Viewern gemeinsam sind.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Video-Bild-Viewer.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt einen nullbasierten Bildindex an, der beim Laden des Viewers angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdX</span></span> </p> </td> 
   <td colname="col2"> <p>Ein nullbasierter Index der Seite innerhalb des Streams, wenn das Gerät im Hochformat ausgerichtet ist. Bei einer Umgebung von links nach rechts bedeutet <span class="codeph"> 0</span> "linke Seite"und <span class="codeph"> 1</span> "rechte Seite". Bei einer Umgebung von rechts nach links ist sie umgekehrt: <span class="codeph"> 0</span> bedeutet "rechte Seite"und <span class="codeph"> 1</span> bedeutet "linke Seite". </p> <p>Wenn nichts angegeben ist, wird standardmäßig <span class="codeph"> 0</span> angenommen. Wird ignoriert, wenn das Gerät im Querformat ausgerichtet ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Kein Standardwert.

## Beispiel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
