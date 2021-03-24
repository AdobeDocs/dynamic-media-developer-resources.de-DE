---
description: Parameter, die allen Viewern gemein sind.
solution: Experience Manager
title: initialFrame
feature: Dynamic Media Classic,Viewer,SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# initialFrame{#initialframe}

Parameter, die allen Viewern gemein sind.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Video-Bild-Viewer.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt einen nullbasierten Frame-Index an, der vom Viewer beim Laden angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Ein nullbasierter Index der Seite innerhalb des Druckbogens, wenn das Gerät im Hochformat ausgerichtet ist. In einer Umgebung von links nach rechts bedeutet <span class="codeph"> 0</span> "linke Seite"und <span class="codeph"> 1</span> "rechte Seite". In "rechts nach links"ist es umgekehrt: <span class="codeph"> 0</span> bedeutet "rechte Seite" und <span class="codeph"> 1</span> bedeutet "linke Seite". </p> <p>Wenn nicht angegeben, wird standardmäßig <span class="codeph"> 0</span> angenommen. Wird ignoriert, wenn das Gerät im Querformat ausgerichtet ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Keine Standardeinstellung.

## Beispiel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```

