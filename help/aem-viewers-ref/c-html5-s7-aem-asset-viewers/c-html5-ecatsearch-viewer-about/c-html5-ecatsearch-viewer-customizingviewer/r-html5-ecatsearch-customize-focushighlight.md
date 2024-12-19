---
title: Fokushervorhebung
description: Eingabefokushervorhebung, die um das fokussierte Element der Viewer-Benutzeroberfläche angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '74'
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
