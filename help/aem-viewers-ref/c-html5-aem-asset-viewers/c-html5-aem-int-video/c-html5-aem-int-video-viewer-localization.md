---
title: Lokalisierung von Elementen der Benutzeroberfläche
description: Bestimmte Inhalte, die der interaktive Video-Viewer anzeigt, unterliegen der Lokalisierung. Solche Inhalte enthalten QuickInfos zu Benutzeroberflächenelementen und eine Fehlermeldung, die angezeigt wird, wenn das Video nicht wiedergegeben werden kann.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d293c385-d355-4d9e-9fe9-8ef35fef60bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Lokalisierung von Elementen der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der interaktive Video-Viewer anzeigt, unterliegen der Lokalisierung. Solche Inhalte enthalten QuickInfos zu Benutzeroberflächenelementen und eine Fehlermeldung, die angezeigt wird, wenn das Video nicht wiedergegeben werden kann.

Jeder Textinhalt, der im Viewer lokalisiert werden kann, wird durch die spezielle Viewer-SDK-Kennung namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßigen Textwert für ein englisches Gebietsschema ( `"en"`), der mit dem standardmäßigen Viewer bereitgestellt wird. Darüber hinaus können benutzerdefinierte Werte für beliebig viele Gebietsschemata festgelegt werden.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet, andernfalls wird der Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als JSON-Objekt für die Lokalisierung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt ist Folgendes:

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

Im obigen Beispiel definiert das Localization-Objekt zwei Gebietsschemata (`"en"` und `"fr"`) und stellt die Lokalisierung für zwei Elemente der Benutzeroberfläche in jedem Gebietsschema bereit.

Der Web-Seiten-Code sollte das Lokalisierungsobjekt an den Viewer-Konstruktor als Wert `localizedTexts` Felds des Konfigurationsobjekts übergeben. Eine alternative Option besteht darin, das Lokalisierungsobjekt durch Aufruf `setLocalizedTexts(localizationInfo)` -Methode zu übergeben.

Die folgenden SYMBOLE werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>QuickInfo für… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.LABEL-</span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> Ausgewählter Status der Wiedergabe-Pause-Schaltfläche </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Deaktivierter Status der Wiedergabe-Pause-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY-</span> </p> </td> 
   <td colname="col2"> <p> Status der Pause-Wiedergabeschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP-</span> </p> </td> 
   <td colname="col2"> <p>Video-Scrubber. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP-</span> </p> </td> 
   <td colname="col2"> <p>Videodauer auf der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> Ausgewähltes veränderliches Volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Veränderliches Volume deaktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> Die Beschriftung des Lautstärkereglers wird über das Attribut ARIA <span class="codeph"> aria-valueText </span> angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Vollbildschaltfläche im normalen Zustand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Vollbildschaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> Ausgewählter Status der Untertitelschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p> Deaktivierte Schaltfläche für Untertitel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InteractiveSwatches.BANNER-</span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scroll up button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scroll down button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Social-Sharing-Tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP-</span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche „Link-Freigabe“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER-</span> </p> </td> 
   <td colname="col2"> <p>Dialogfeld-Kopfzeile verknüpfen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Dialogfeld „Verknüpfung“, Schaltfläche zum Schließen oben rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Beschreibung des Freigabe-Links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche Abbrechen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION-</span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche Alle auswählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Alle auswählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Facebook-Freigabeschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Twitter Freigabe-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton.TOOLTIP-</span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Schließen des Aktionsbereichs aufrufen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>Fehlermeldung, wenn keine Videowiedergabe möglich ist. </p> </td> 
  </tr> 
 </tbody> 
</table>
