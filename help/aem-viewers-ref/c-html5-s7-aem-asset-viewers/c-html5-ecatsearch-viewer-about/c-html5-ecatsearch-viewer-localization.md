---
description: Bestimmte Inhalte, die der E-Katalog-Viewer anzeigt, unterliegen der lokale Anpassung, einschließlich Zoom-Schaltflächen, Schaltflächen zum Ändern der Seite, Miniaturansicht, Schaltfläche im Vollbildmodus, Schaltfläche zum Schließen und Schaltflächen für die Bildlaufleiste.
seo-description: Bestimmte Inhalte, die der E-Katalog-Viewer anzeigt, unterliegen der lokale Anpassung, einschließlich Zoom-Schaltflächen, Schaltflächen zum Ändern der Seite, Miniaturansicht, Schaltfläche im Vollbildmodus, Schaltfläche zum Schließen und Schaltflächen für die Bildlaufleiste.
seo-title: Lokale Anpassung der Elemente der Benutzeroberfläche
solution: Experience Manager
title: Lokale Anpassung der Elemente der Benutzeroberfläche
topic: Dynamic media
uuid: 836cb874-2ce6-4737-9c10-f41af003a285
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---


# Lokale Anpassung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der E-Katalog-Viewer anzeigt, unterliegen der lokale Anpassung, einschließlich Zoom-Schaltflächen, Schaltflächen zum Ändern der Seite, Miniaturansicht, Schaltfläche im Vollbildmodus, Schaltfläche zum Schließen und Schaltflächen für die Bildlaufleiste.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch einen speziellen Viewer SDK-Bezeichner namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen Standardtextwert für das englische Gebietsschema ( `"en"`), das mit dem standardmäßigen Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für so viele Gebietsschemas wie erforderlich enthalten.

Beim Beginn des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jede unterstützte SYMBOL im Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird auf den Standardtext zurückgesetzt.

Benutzerdefinierte Daten zur lokale Anpassung können als JSON-Objekt der lokale Anpassung an den Viewer übergeben werden. Ein solches Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für eine solche lokale Anpassung:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

Im obigen Beispiel definiert das lokale Anpassung-Objekt zwei Gebietsschemas ( `"en"` und `"fr"`) und stellt lokale Anpassung für zwei Benutzeroberflächenelemente in jedem Gebietsschema bereit.

Der Webseitencode sollte ein solches lokale Anpassung-Objekt als Wert des Felds `localizedTexts` des Konfigurationsobjekts an den Viewer-Konstruktor übergeben. Eine andere Option besteht darin, das Objekt &quot;lokale Anpassung&quot;durch Aufruf der Methode `setLocalizedTexts(localizationInfo)` weiterzugeben.

Die folgenden SYMBOLs werden unterstützt (vorausgesetzt, containerId ist die ID des Viewer-Containers):

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
   <td colname="col2"> <p>ARIA-Beschriftung für das Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptkomponente Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schließen-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Vergrößern" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Verkleinern" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Zurücksetzen des Zooms </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Blättern Sie nach oben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Blättern Sie nach unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_rightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Große Schaltfläche für die nächste Seite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_leftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Große Schaltfläche für vorherige Seite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_lastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Letzte Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Letzte Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_firstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Erste Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Erste Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarRightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Nächste Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Vorherige Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Miniaturansichten"im Miniaturansichtsmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Miniaturansichten"im normalen Modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schließen-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Schließen des Infofelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Social Sharing-Tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Weitergeben per E-Mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Kopfzeile des E-Mail-Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>E-Mail-Dialogfeld oben rechts, Schaltfläche zum Schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS  </span> </p> </td> 
   <td colname="col2"> <p>Fehlermeldung angezeigt, wenn die E-Mail-Adresse fehlerhaft ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Eingabefeld "An". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HINZUFÜGEN  </span> </p> </td> 
   <td colname="col2"> <p>hinzufügen Schaltfläche "Weitere E-Mail-Adresse". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HINZUFÜGEN  </span> </p> </td> 
   <td colname="col2"> <p>hinzufügen Schaltfläche "Weitere E-Mail-Adresse". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.VON  </span> </p> </td> 
   <td colname="col2"> <p>Aus dem Eingabefeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE  </span> </p> </td> 
   <td colname="col2"> <p>Meldungseingabefeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "E-Mail-Adresse entfernen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Alles auswählen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Klicken Sie auf "Alle". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche zum Schließen, die nach dem Senden des Formulars unten im Dialogfeld angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Schließen-Schaltfläche, die nach dem Senden des Formulars im unteren Bereich des Dialogfelds angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche zum Senden des Formulars. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Senden des Formulars. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS  </span> </p> </td> 
   <td colname="col2"> <p>Bestätigungsmeldung angezeigt, wenn die E-Mail erfolgreich gesendet wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE  </span> </p> </td> 
   <td colname="col2"> <p>Fehlermeldung, die angezeigt wird, wenn die E-Mail nicht erfolgreich gesendet wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Freigabe einbetten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Dialogfeldüberschrift einbetten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Dialogfeld "Einbetten"oben rechts, Schaltfläche "Schließen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Beschreibung des Einbettungscode-Textes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Kombinationsfeld "Einbettungsgröße". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>Text für den letzten Eintrag "benutzerdefinierte Größe"im Kombinationsfeld "Einbettungsgröße". </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Drucken-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> print.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Drucken Sie die Kopfzeile des Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Drucken-Dialogfeld oben rechts neben Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für den Abschnitt "Druckseiten auswählen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "Aktuelle Seiten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "Bereich verteilen von". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die numerische Auswahl "bis". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "Alle Seiten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für den Abschnitt "Seitenverarbeitung". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "1 Seite pro Blatt". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "2 Seiten pro Blatt". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> print.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p> Schaltfläche "Abbrechen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "An Druckausgabe senden" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> Schaltfläche "An Druck senden". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesMenu.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Menüschaltfläche "Favoriten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Hinzufügen Favorit"im Modus "Favoriten bearbeiten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Hinzufügen Favorit" im normalen Modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Favoriten entfernen"im Modus "Favoriten bearbeiten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Favoriten entfernen"im normalen Modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Ansicht aller Favoriten", wenn die Favoriten-Ansicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Ansicht aller Favoriten", wenn die Favoriten-Ansicht inaktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesEffect.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Einzelnes Lieblingssymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY]  </span> </p> </td> 
   <td colname="col2"> <p>Seitenbeschriftung, die vom Viewer beim Laden generiert wird. </p> <p>Der Name dieses Symbols ist eine Vorlage, wobei <span class="codeph"> XX </span> ein auf Null basierender Druckbogenindex im Querformat ist und optional <span class="codeph"> YY </span> ein auf Null basierender Seitenindex innerhalb des Druckbogens ist, der auf <span class="codeph"> XX </span> ausgerichtet ist. </p> <p>Gilt nur für das ursprünglich geladene Asset; ignoriert, wenn ein Asset mithilfe des API-Aufrufs <span class="codeph"> setAsset() </span> geändert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM  </span> </p> </td> 
   <td colname="col2"> <p> Zeichen, das als Trennzeichen für Seitenbeschriftungen verwendet wird, falls Beschriftungen für linke und rechte Seiten innerhalb eines Druckbogens definiert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Die Hauptsteuerleiste blättert nach links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Die Hauptsteuerungsleiste scrollt nach rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.PLACEHOLDER  </span> </p> </td> 
   <td colname="col2"> <p>Lokalisierte Eingabeaufforderung, die im Sucheingabefeld angezeigt wird, bevor Beginn den Suchtext eingeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_PROMPT  </span> </p> </td> 
   <td colname="col2"> <p>Lokalisierte Meldung, die angezeigt wird, wenn das Suchfeld zum ersten Mal geöffnet wird, und der Benutzer die Suche durchführen lässt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_NO_RESULTS  </span> </p> </td> 
   <td colname="col2"> <p>Lokalisierte Meldung, die angezeigt wird, wenn die Suche keine Ergebnisse zurückgegeben hat. </p> <p>Dieses Symbol unterstützt das folgende Laufzeitersetzungstoken: <span class="codeph"> $SEARCH_TEXT$ </span>. Die Komponente ersetzt sie durch den vom Benutzer eingegebenen Suchtext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_RESULTS  </span> </p> </td> 
   <td colname="col2"> <p>Lokalisierte Meldung, die angezeigt wird, wenn die Suche erfolgreich abgeschlossen wurde, und die mindestens ein Ergebnis zurückgibt. </p> <p>Dieses Symbol unterstützt die folgenden Laufzeitersetzungstoken: </p> <p> 
     <ul id="ul_30B76EAB921848069BE843A5F91F697A"> 
      <li id="li_16AF3EFCC4BF4180B66DE5EA82CC77F4"> <span class="codeph"> $SEARCH_TEXT$  </span> - Der vom Benutzer eingegebene Suchtext. </li> 
      <li id="li_A0FBF12344B04BF0B702A2B7473330A8"> <span class="codeph"> $HIT_COUNT$  </span> - Die Gesamtanzahl der gefundenen Suchtreffer. </li> 
      <li id="li_9EB7B41A989B455ABEC72E052284F117"> <span class="codeph"> $PAGE_COUNT$  </span> - Die Anzahl der Katalogseiten, die mindestens einen Suchtreffer enthalten. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.THUMBNAIL_LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Lokalisierte Bezeichnung für die Ergebnisminiatur des Suchfelds. </p> <p>Dieses Symbol unterstützt die folgenden Laufzeitersetzungstoken: </p> <p> 
     <ul id="ul_7620C59FA56544CD9CE9E49B1871BCC1"> 
      <li id="li_FAF092734B4B4B55A309413690DA3FCC"> <span class="codeph"> $PAGE$  </span> - Seitenzahl. </li> 
      <li id="li_3414176505BB4A768FB42341A315E96F"> <span class="codeph"> $PAGE_HIT_COUNT$  </span> - Die Anzahl der auf der Seite gefundenen Suchergebnisse. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Definiert einen Wert des Attributs <span class="codeph"> aria-label </span> ARIA für das gesamte Suchfeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

