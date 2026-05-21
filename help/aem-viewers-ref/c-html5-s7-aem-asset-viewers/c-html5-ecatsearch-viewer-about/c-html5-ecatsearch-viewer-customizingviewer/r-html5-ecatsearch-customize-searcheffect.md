---
title: Sucheffekt
description: Der Viewer zeigt Suchergebnisbereiche über der Hauptansicht an, um die im Katalog gefundenen Wörter oder Phrasen hervorzuheben.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
TQID: 'https://experienceleague.adobe.com/h30DfEeB69i1gbnfOvnKphglRkXgcvOTG8L-eTZv2GU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 1%

---

# Sucheffekt{#search-effect}

Der Viewer zeigt Suchergebnisbereiche über der Hauptansicht an, um die im Katalog gefundenen Wörter oder Phrasen hervorzuheben.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild von Suchergebnisbereichen wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrund der Suchergebnisregion. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie Suchergebnisbereiche mit einer halbtransparenten, gelben Füllung ein:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
