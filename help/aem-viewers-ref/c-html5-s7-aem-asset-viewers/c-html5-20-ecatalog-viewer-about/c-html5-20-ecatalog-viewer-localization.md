---
title: Lokalisierung der Elemente der Benutzeroberfläche
description: Bestimmte Inhalte, die der E-Katalog-Viewer anzeigt, können lokalisiert werden, einschließlich Zoom-Schaltflächen, Schaltflächen zum Ändern der Seite, Miniaturschaltflächen, Vollbildschaltflächen, Schließen-Schaltflächen und Schaltflächen der Bildlaufleiste.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 1d7e9eba-b30c-4f85-b551-6842f73dc22c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Lokalisierung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der E-Katalog-Viewer anzeigt, können lokalisiert werden, einschließlich Zoom-Schaltflächen, Schaltflächen zum Ändern der Seite, Miniaturschaltflächen, Vollbildschaltflächen, Schließen-Schaltflächen und Schaltflächen der Bildlaufleiste.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch eine spezielle Viewer-SDK-ID namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßig zugewiesenen Textwert für das englische Gebietsschema ( `"en"`), das mit dem vordefinierten Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für beliebig viele Gebietsschemas enthalten.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jede unterstützte SYMBOL im Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird der vordefinierte Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als lokalisiertes JSON-Objekt an den Viewer übergeben werden. Ein solches Objekt enthält die Liste der unterstützten Gebietsschemas, die SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt:

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

Im obigen Beispiel definiert das Lokalisierungsobjekt zwei Gebietsschemas ( `"en"` und `"fr"`) und stellt die Lokalisierung von zwei Benutzeroberflächenelementen in jedem Gebietsschema bereit.

Der Webseitencode sollte dieses Lokalisierungsobjekt als Wert des Felds `localizedTexts` des Konfigurationsobjekts an den Viewer-Konstruktor übergeben. Eine alternative Option besteht darin, das Lokalisierungsobjekt durch Aufruf der Methode `setLocalizedTexts(localizationInfo)` weiterzugeben.

Die folgenden SYMBOLs werden unterstützt (vorausgesetzt, containerId ist die ID des Viewer-Containers):

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>QuickInfo für ... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für das Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptansichtskomponente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Schließen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Vergrößern" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Verkleinern" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Zurücksetzen des Zooms </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche im Vollbildmodus im Normalzustand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scrollen Sie nach oben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scrollen Sie nach unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_rightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Große nächste Seite" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_leftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Große vorherige Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_lastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche Letzte Seite . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche Letzte Seite . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_firstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Erste Seite" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Erste Seite" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_toolBarRightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Nächste Seite" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Vorherige Seite". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Miniaturansichten"im Miniaturansichtsmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Miniaturen"im normalen Modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Schließen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Schließen des Info-Bedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Social-Freigabe-Tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "E-Mail-Freigabe". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Header des E-Mail-Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>E-Mail-Dialogfeld oben rechts, Schaltfläche zum Schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS </span> </p> </td> 
   <td colname="col2"> <p>Fehlermeldung angezeigt, falls eine E-Mail-Adresse fehlerhaft ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Eingabefeld "An". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Weitere E-Mail-Adresse hinzufügen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Weitere E-Mail-Adresse hinzufügen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM </span> </p> </td> 
   <td colname="col2"> <p>Aus Eingabefeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>Nachrichteneingabefeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche E-Mail-Adresse entfernen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Alle auswählen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Alle auswählen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Schließen", die nach der Formularübermittlung unten im Dialogfeld angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Schließen", die nach der Formularübermittlung unten im Dialogfeld angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche zum Senden des Formulars. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Formularübermittlung". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>Bestätigungsnachricht angezeigt, wenn E-Mail erfolgreich gesendet wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>Fehlermeldung, die angezeigt wird, wenn die E-Mail nicht erfolgreich gesendet wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Freigabe einbetten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Einbetten des Dialogfeldheaders </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Einbetten, Dialogfeld oben rechts, Schaltfläche zum Schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Beschreibung des Einbettungscode-Textes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Kombinationsfeld Einbettungsgröße . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Text für den letzten Eintrag "benutzerdefinierte Größe"im Kombinationsfeld "Einbettungsgröße". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Linkfreigabe". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Link-Dialogfeldüberschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Link-Dialogfeld oben rechts, Schaltfläche zum Schließen. </p> </td> 
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
   <td colname="col2"> <p>Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Alle auswählen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Schaltfläche "Alle auswählen" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Facebook-Freigabe-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "twitter freigeben". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Drucken-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Drucken Sie die Dialogfeldkopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Dialogfeld "Drucken"mit der rechten oberen Schaltfläche zum Schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für den Abschnitt "Druckseiten auswählen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "Aktuelle Seiten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "Bereich von der Seite ausbreiten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die numerische Auswahl "bis". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "Alle Seiten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für den Abschnitt "Seitenverarbeitung". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "1 Seite pro Blatt". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für das Optionsfeld "2 Seiten pro Blatt". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p> Schaltfläche Abbrechen . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Beschriftung für die Schaltfläche "Zum Drucken senden" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Schaltfläche "Zum Drucken senden". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesMenu.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Menüschaltfläche "Favoriten". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Favoriten hinzufügen"im Modus Favoriten bearbeiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Favoriten hinzufügen"im normalen Modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Favoriten entfernen"im Modus Favoriten bearbeiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Favoriten entfernen"im normalen Modus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Alle Favoriten anzeigen", wenn die Favoritenansicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Alle Favoriten anzeigen", wenn die Favoritenansicht inaktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesEffect.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Einzelnes Lieblingssymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY] </span> </p> </td> 
   <td colname="col2"> <p>Seitenbeschriftung, die vom Viewer beim Laden generiert wird. </p> <p>Der Name dieses Symbols ist eine Vorlage, bei der <span class="codeph"> XX </span> ein nullbasierter Spread-Index in Querformat und optional <span class="codeph"> YY </span> ein nullbasierter Seitenindex innerhalb des von <span class="codeph"> XX </span> anvisierten Spreads ist. </p> <p>Gilt nur für das ursprünglich geladene Asset. Wird ignoriert, wenn ein Asset mithilfe des API-Aufrufs <span class="codeph"> setAsset() </span> geändert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM </span> </p> </td> 
   <td colname="col2"> <p> Zeichen, das als Trennzeichen für Seitenbeschriftungen verwendet wird, falls Beschriftungen für linke und rechte Seiten innerhalb eines Druckbereichs definiert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Die Hauptsteuerleiste blättert nach links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Die Hauptsteuerleiste scrollt nach rechts. </p> </td> 
  </tr> 
 </tbody> 
</table>
