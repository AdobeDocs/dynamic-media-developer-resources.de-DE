---
title: Fokushervorhebung
description: Hervorhebung des Fokus der Eingabe, die um das fokussierte Element der Benutzeroberfläche des Viewers herum angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# Fokushervorhebung{#focus-highlight}

Hervorhebung des Fokus der Eingabe, die um das fokussierte Element der Benutzeroberfläche des Viewers herum angezeigt wird.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

Das Erscheinungsbild der Fokushervorhebung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer *:focus
```

**CSS-Eigenschaften der Fokusmarkierung**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> entwurf </span> </p> </td> 
   <td colname="col2"> <p> Fokusmarkierungsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die standardmäßige Browserfokushervorhebung für alle Elemente der Viewer-Benutzeroberfläche zu deaktivieren, fügen Sie den folgenden CSS-Selektor zum Stylesheet des Viewers hinzu:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
