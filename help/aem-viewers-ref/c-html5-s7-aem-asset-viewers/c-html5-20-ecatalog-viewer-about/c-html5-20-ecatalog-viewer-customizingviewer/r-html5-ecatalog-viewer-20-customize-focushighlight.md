---
description: Hervorhebung des Eingabefokus, der um das Element der fokussierten Benutzeroberfläche des Viewers angezeigt wird.
seo-description: Hervorhebung des Eingabefokus, der um das Element der fokussierten Benutzeroberfläche des Viewers angezeigt wird.
seo-title: Fokushervorhebung
solution: Experience Manager
title: Fokushervorhebung
topic: Dynamic Media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Fokusmarkierung{#focus-highlight}

Hervorhebung des Eingabefokus, der um das Element der fokussierten Benutzeroberfläche des Viewers angezeigt wird.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

Das Erscheinungsbild der Fokushervorhebung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer *:focus
```

**CSS-Eigenschaften der Fokushervorhebung**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Umriss  </span> </p> </td> 
   <td colname="col2"> <p> Fokusmarkierungsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die standardmäßige Browserfokushervorhebung für alle Elemente der Benutzeroberfläche des Viewers zu deaktivieren, fügen Sie dem Stylesheet des Viewers den folgenden CSS-Selektor hinzu:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

