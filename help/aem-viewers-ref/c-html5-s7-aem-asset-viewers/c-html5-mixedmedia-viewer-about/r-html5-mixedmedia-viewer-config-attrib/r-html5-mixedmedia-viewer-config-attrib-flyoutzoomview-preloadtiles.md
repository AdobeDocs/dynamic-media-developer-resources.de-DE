---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Setzen Sie dies auf <span class="codeph"> 1</span> , um das Vorausfüllen des gezoomten Bildes zu ermöglichen. </p> <p>Legen Sie <span class="codeph"> 0</span> fest, um das Zoombild nach Bedarf schrittweise zu laden. </p> <p> <p>Hinweis:  Beachten Sie, dass bei Aktivierung dieser Option die Bandbreitennutzung deutlich erhöht sein kann, da das gezoomte Bild vollständig geladen werden muss - selbst wenn der Benutzer keine Zoom-Aktion durchführt. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
