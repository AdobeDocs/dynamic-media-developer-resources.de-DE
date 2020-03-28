---
description: Parameter, die allen Viewern gemein sind.
seo-description: Parameter, die allen Viewern gemein sind.
seo-title: initialFrame
solution: Experience Manager
title: initialFrame
topic: Dynamic media
uuid: 5d1c3a8a-8598-47c9-a106-36e8c6fcafb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameId</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt einen nullbasierten Frame-Index an, der vom Viewer beim Laden angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Ein nullbasierter Index der Seite innerhalb des Druckbogens, wenn das Gerät im Hochformat ausgerichtet ist. In einer Umgebung von links nach rechts bedeutet <span class="codeph"> 0</span> "linke Seite"und <span class="codeph"> 1</span> "rechte Seite". In "rechts nach links"ist es umgekehrt: <span class="codeph"> 0</span> bedeutet "rechte Seite" und <span class="codeph"> 1</span> "linke Seite". </p> <p>Wenn nicht angegeben, wird standardmäßig <span class="codeph"> 0</span> angenommen. Wird ignoriert, wenn das Gerät im Querformat ausgerichtet ist. </p> </td> 
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

