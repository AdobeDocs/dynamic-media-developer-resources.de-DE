---
description: Hervorhebung des Eingabefokus, der um das Element der fokussierten Benutzeroberfläche des Viewers angezeigt wird.
solution: Experience Manager
title: Fokushervorhebung
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog-Suche
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
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

