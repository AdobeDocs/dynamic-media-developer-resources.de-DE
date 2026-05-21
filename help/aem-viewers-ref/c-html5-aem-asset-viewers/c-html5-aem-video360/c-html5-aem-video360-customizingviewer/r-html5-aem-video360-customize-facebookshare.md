---
title: Facebook-Freigabe
description: Das Facebook-Share-Tool besteht aus einer Schaltfläche, die zum Social-Sharing-Bedienfeld hinzugefügt wird. Wenn die Schaltfläche ausgewählt ist, wird der Benutzer zu einem Freigabedialogfeld weitergeleitet, das von einem Social-Media-Service bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 343cde8b-796a-420f-abb7-268b3791a684
TQID: 'https://experienceleague.adobe.com/ryqtr6b9OrkNEK8xw5tspcQmuTPQe7Rl1ELRVr0AHms'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 0%

---

# Facebook-Freigabe{#facebook-share}

Das Facebook-Share-Tool besteht aus einer Schaltfläche, die zum Social-Sharing-Bedienfeld hinzugefügt wird. Wenn die Schaltfläche ausgewählt ist, wird der Benutzer zu einem Freigabedialogfeld weitergeleitet, das von einem Social-Media-Service bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Das Erscheinungsbild der Facebook-Freigabe-Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer .s7facebookshare
```

**CSS-Eigenschaften des Facebook-Freigabe-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Bedienfeld Social-Freigabe entfernen, indem Sie `display:none` CSS-Eigenschaft für die CSS-Klasse festlegen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Beispiel** - Zum Einrichten einer Facebook-Freigabe-Schaltfläche mit einer Größe von 28 x 28 Pixel, die für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt:

```
.s7video360viewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7video360viewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7video360viewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7video360viewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
