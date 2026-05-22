---
title: CallToAction.align
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a92c4a-3757-4811-87b8-68fb367ea94d
TQID: 'https://experienceleague.adobe.com/zMB6vYFDHiSJW1Q3O-L1204O7PkWg-a-txzamKbtZwQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# CallToAction.align{#calltoaction-align}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]align=left|center|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links|Mitte|rechts</span> </p> </td> 
   <td colname="col2"> <p> Gibt die interne horizontale Ausrichtung (oder Verankerung) des Miniatur-Containers im Komponentenbereich an. </p> <p>In call-to-action hat der interne Miniatur-Container die Größe so, dass nur eine ganze Anzahl von Miniaturen angezeigt wird. Infolgedessen gibt es einen gewissen Abstand zwischen dem internen Container und den Begrenzungen der externen Komponente. </p> <p>Dieser Modifikator gibt an, wie der Container Interne Miniaturen horizontal innerhalb der Komponente positioniert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`center`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
align=left
```
