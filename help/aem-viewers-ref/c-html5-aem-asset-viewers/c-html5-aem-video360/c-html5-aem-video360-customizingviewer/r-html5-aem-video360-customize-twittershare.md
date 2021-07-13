---
description: Das twitter-Freigebungs-Tool besteht aus einer Schaltfläche, die dem Social-Freigabe-Bedienfeld hinzugefügt wird. Wenn auf die Schaltfläche geklickt wird, wird der Benutzer zu einem Freigabedialogfeld umgeleitet, das von einem Social-Dienst bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.
solution: Experience Manager
title: Twitter Share
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a90a4c82-b51a-4fb0-9196-44ae4ba8e0cd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Twitter Share{#twitter-share}

Das twitter-Freigebungs-Tool besteht aus einer Schaltfläche, die dem Social-Freigabe-Bedienfeld hinzugefügt wird. Wenn auf die Schaltfläche geklickt wird, wird der Benutzer zu einem Freigabedialogfeld umgeleitet, das von einem Social-Dienst bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Das Erscheinungsbild der Twitter-Freigabe-Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer .s7twittershare
```

**CSS-Eigenschaften des Twitter-Freigabe-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Social-Freigabebereich entfernen, indem Sie die CSS-Eigenschaft `display:none` in der CSS-Klasse festlegen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Beispiel** : So richten Sie eine Twitter-Freigabe-Schaltfläche mit 28 x 28 Pixel ein und zeigen für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild an:

```
.s7video360viewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7video360viewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7video360viewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7video360viewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
