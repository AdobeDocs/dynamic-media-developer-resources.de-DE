---
title: Fokushervorhebung
description: Eingabefokushervorhebung, die um das fokussierte Element der Viewer-Benutzeroberfläche angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
TQID: 'https://experienceleague.adobe.com/E7n09sJ0qY9Aivp5OUFr5Jc6bwS5Ah3N-HdS9-H2Pgw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 0%

---

# Fokushervorhebung{#focus-highlight}

Eingabefokushervorhebung, die um das fokussierte Element der Viewer-Benutzeroberfläche angezeigt wird.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

Das Erscheinungsbild der Fokushervorhebung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer *:focus
```

**CSS-Eigenschaften der Fokushervorhebung**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Fokushervorhebung - Stil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel : Um die standardmäßige Browser-Fokushervorhebung für alle Elemente der Viewer-Benutzeroberfläche zu deaktivieren, fügen Sie die folgende CSS-Auswahl zum Stylesheet des Viewers hinzu:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
