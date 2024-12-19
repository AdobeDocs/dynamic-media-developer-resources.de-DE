---
title: initialFrame
description: Für alle Viewer gemeinsamer Parameter.
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

Für alle Viewer gemeinsamer Parameter.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Videobild-Viewer.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt einen Null-basierten Frame-Index an, den der Viewer beim Laden anzeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageId</span></span> </p> </td> 
   <td colname="col2"> <p>Ein Index auf der Basis Null der Seite innerhalb des Spreads, wenn das Gerät im Hochformat ist. Für eine „von links nach rechts“-Umgebung bedeutet <span class="codeph"> 0</span> „linke Seite“ und <span class="codeph"> 1</span> „rechte Seite“. Bei einer Umgebung mit Rechts-nach-links-Schreibrichtung ist dies das Gegenteil: <span class="codeph"> 0 </span> „rechte Seite“ und <span class="codeph"> 1 </span> „linke Seite“. </p> <p>Wenn kein Wert angegeben ist, wird standardmäßig <span class="codeph"> 0</span> angenommen. Wird ignoriert, wenn sich das Gerät im Querformat befindet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Kein Standard.

## Beispiel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
