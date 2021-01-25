---
description: Standardwarnungen werden mit einer konsolidierten E-Mail-Nachricht am Ende des konfigurierten Mittelungsintervalls gesendet.
seo-description: Standardwarnungen werden mit einer konsolidierten E-Mail-Nachricht am Ende des konfigurierten Mittelungsintervalls gesendet.
seo-title: Standardwarnungen
solution: Experience Manager
title: Standardwarnungen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d3294434-a44b-4742-9d77-a6945760d33c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---


# Standardwarnungen{#standard-alerts}

Standardwarnungen werden mit einer konsolidierten E-Mail-Nachricht am Ende des konfigurierten Mittelungsintervalls gesendet.

In der folgenden Tabelle werden die einzelnen Typen von Standardwarnungen beschrieben.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Warnungstyp</b> </th> 
   <th class="entry"> <b>Titel-ID</b> </th> 
   <th class="entry"> <b>Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Gesperrte Anforderung </p> </td> 
   <td> <p>Sperren </p> </td> 
   <td> <p>Wird gesendet, wenn eine Anforderung innerhalb des angegebenen Schwellenwerts keine Antwort an den Client zurückgibt. Kann auf unerwartete Anfragen hindeuten, was zu einer Dezimierung des Java-Threadpools führen kann. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Hohe Konsequenz </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Wird ausgegeben, wenn die Anzahl der gleichzeitig verarbeiteten Anforderungen (die <i>überlappende</i>) den angegebenen Schwellenwert überschreitet. Kann auf eine Überlastungsbedingung des Servers hindeuten. </td> 
  </tr> 
  <tr> 
   <td> <p>Minimaler Traffic </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Wird generiert, wenn die Anforderungsrate insgesamt unter den angegebenen Schwellenwert fällt. Zeigt in der Regel ein Serverkommunikationsproblem an (z. B. wenn ein Server offline genommen wird). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fehlerquote </p> </td> 
   <td> <p>Fehler </p> </td> 
   <td> <p>Wird ausgegeben, wenn die durchschnittliche Rate von HTTP-Fehlerantworten während des Stichprobenintervalls den angegebenen Schwellenwert überschreitet. Kann als Hinweis auf Konfigurationsprobleme, fehlende Bilder, Website-Programmierung oder Datenbankfehler dienen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Reaktionszeit </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Wird gesendet, wenn die durchschnittliche Verarbeitungszeit der Anforderung während des Stichprobenintervalls über dem angegebenen Schwellenwert wächst. Gibt normalerweise eine temporäre oder beständige Überlastungsbedingung des Server- oder Backend-Image-Datenspeicherung-Systems an. </p> <p>Fehlerantworten werden bei der Berechnung der durchschnittlichen Antwortzeit nicht berücksichtigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

