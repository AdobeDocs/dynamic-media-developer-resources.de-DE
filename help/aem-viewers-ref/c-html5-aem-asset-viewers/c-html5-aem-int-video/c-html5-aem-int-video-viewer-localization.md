---
description: Bestimmte Inhalte, die im interaktiven Video-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören QuickInfos zu Elementen in der Benutzeroberfläche und eine Fehlermeldung, die angezeigt wird, wenn das Video nicht wiedergegeben werden kann.
seo-description: Bestimmte Inhalte, die im interaktiven Video-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören QuickInfos zu Elementen in der Benutzeroberfläche und eine Fehlermeldung, die angezeigt wird, wenn das Video nicht wiedergegeben werden kann.
seo-title: lokale Anpassung der Elemente der Benutzeroberfläche
solution: Experience Manager
title: lokale Anpassung der Elemente der Benutzeroberfläche
uuid: 7c880e25-76dc-43d3-83fc-12de92afd35f
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---


# lokale Anpassung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die im interaktiven Video-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören QuickInfos zu Elementen in der Benutzeroberfläche und eine Fehlermeldung, die angezeigt wird, wenn das Video nicht wiedergegeben werden kann.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch den speziellen Viewer SDK-Bezeichner SYMBOL dargestellt. Jedes SYMBOL verfügt über einen Standardtextwert für ein englisches Gebietsschema ( `"en"`), das mit dem standardmäßigen Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für so viele Gebietsschemas wie erforderlich enthalten.

Beim Beginn des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird auf den Standardtext zurückgesetzt.

Benutzerdefinierte Daten zur lokale Anpassung können als JSON-Objekt der lokale Anpassung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches lokale Anpassung-Objekt ist Folgendes:

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

Im obigen Beispiel definiert das lokale Anpassung-Objekt zwei Gebietsschemas ( `"en"` und `"fr"`) und stellt lokale Anpassung für zwei Benutzeroberflächenelemente in jedem Gebietsschema bereit.

Der Webseitencode sollte das lokale Anpassung-Objekt an den Viewer-Konstruktor als Wert des Felds `localizedTexts` des Konfigurationsobjekts übergeben. Eine andere Option besteht darin, das Objekt &quot;lokale Anpassung&quot;durch Aufruf der Methode `setLocalizedTexts(localizationInfo)` weiterzugeben.

Die folgenden SYMBOLs werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>QuickInfo für... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Status der Schaltfläche zum Abspielen der Pause. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Deaktivierte Wiedergabe-Pause-Schaltflächenstatus </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY  </span> </p> </td> 
   <td colname="col2"> <p> Status der Schaltfläche "Pause wiedergeben". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Video-Scrubber. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Videozeit in der Steuerungsleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Ausgewähltes veränderliches Volumen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Deaktivierte veränderbare Lautstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME  </span> </p> </td> 
   <td colname="col2"> <p> Lautstärkeregler-Knopfbeschriftung durch das ARIA <span class="codeph"> aria-value-ext </span> Attribut offen gelegt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche im Vollbildmodus im Normalzustand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Status der ausgewählten Untertitel-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Deaktivieren Sie den Status der Schaltfläche "Untertitel". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InteractiveSwatches.BANNER  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Blättern Sie nach oben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Blättern Sie nach unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Social Sharing-Tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Teilen von Links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Link-Dialogfeld-Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Link-Dialogfeld oben rechts, Schaltfläche zum Schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Beschreibung des Share-Links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Alles auswählen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> Klicken Sie auf "Alle". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Freigeben"für Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Freigeben von Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Schließen des Aktionsbedienfelds </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR  </span> </p> </td> 
   <td colname="col2"> <p>Fehlermeldung, die angezeigt wird, wenn keine Videowiedergabe möglich ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

