---
description: Bestimmte Inhalte, die der Flyout-Viewer anzeigt, unterliegen der lokale Anpassung. Dieser Inhalt enthält QuickInfos zu Elementen der Benutzeroberfläche und Informationsmeldungen, die von der Flyout-Zoom-Ansicht beim Laden angezeigt werden.
solution: Experience Manager
title: lokale Anpassung der Elemente der Benutzeroberfläche
feature: Dynamic Media Classic, Viewer, SDK/API, Flyout
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# lokale Anpassung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der Flyout-Viewer anzeigt, unterliegen der lokale Anpassung. Dieser Inhalt enthält QuickInfos zu Elementen der Benutzeroberfläche und Informationsmeldungen, die von der Flyout-Zoom-Ansicht beim Laden angezeigt werden.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch einen speziellen Viewer SDK-Bezeichner namens SYMBOL dargestellt. Jedem SYMBOL ist ein Standardtextwert für das englische Gebietsschema ( `"en"`) zugeordnet, das mit dem vordefinierten Viewer bereitgestellt wird. Es können auch benutzerdefinierte Werte für so viele Gebietsschemas wie nötig festgelegt werden.

Beim Beginn des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für das Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird auf den Standardtext zurückgesetzt.

Benutzerdefinierte Daten zur lokale Anpassung können als JSON-Objekt der lokale Anpassung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches lokale Anpassung-Objekt ist Folgendes:

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

Im obigen Beispiel definiert das lokale Anpassung-Objekt zwei Gebietsschemas ( `"en"` und `"fr"`) und stellt lokale Anpassung für zwei Benutzeroberflächenelemente in jedem Gebietsschema bereit.

Der Webseitencode sollte das lokale Anpassung-Objekt als Wert des Felds `localizedTexts` des Konfigurationsobjekts an den Viewer-Konstruktor übergeben. Eine andere Option besteht darin, das Objekt &quot;lokale Anpassung&quot;durch Aufruf der `setLocalizedTexts(localizationInfo)`-Methode zu übergeben.

Die folgenden SYMBOLs werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptkomponente Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p>Informationsmeldung für Desktop-Systeme. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p>Informationsmeldung für Touch-Geräte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für die Schaltfläche "Nach links blättern". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für die Schaltfläche mit einem Bildlauf nach rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für die Schaltfläche "Nach oben". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für die Schaltfläche "Nach unten". </p> </td> 
  </tr> 
 </tbody> 
</table>

