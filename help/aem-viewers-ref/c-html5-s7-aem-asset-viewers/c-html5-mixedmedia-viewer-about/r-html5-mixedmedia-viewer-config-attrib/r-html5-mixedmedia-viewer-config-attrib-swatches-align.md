---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4f25112b-9e51-4a0e-9500-1b5ab0f4de87
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Gibt die interne Ausrichtung (Verankerung) des Farbfeldcontainers im Komponentenbereich an. In Farbfeldern wird der interne Miniaturansichtsbehälter so skaliert, dass nur eine ganze Anzahl von Farbfeldern angezeigt wird. Daher gibt es einige Abstände zwischen dem internen Container und den externen Komponentengrenzen. Dieser Befehl gibt an, wie der interne Farbfeldcontainer innerhalb der Komponente positioniert wird.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td> <p> Legt die Ausrichtung der horizontalen Farbfelder fest. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> Legt die Ausrichtung der vertikalen Farbfelder fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`center,center`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`align=left,top`
