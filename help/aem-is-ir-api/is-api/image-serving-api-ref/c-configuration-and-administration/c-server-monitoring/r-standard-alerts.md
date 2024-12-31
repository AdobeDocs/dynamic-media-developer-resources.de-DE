---
description: Standardwarnungen werden am Ende des konfigurierten Mittelungsintervalls mit einer konsolidierten E-Mail-Nachricht gesendet.
solution: Experience Manager
title: Standardwarnungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Standardwarnungen{#standard-alerts}

Standardwarnungen werden am Ende des konfigurierten Mittelungsintervalls mit einer konsolidierten E-Mail-Nachricht gesendet.

In der folgenden Tabelle werden die einzelnen Arten von Standardwarnhinweisen beschrieben.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Warnhinweistyp</b> </th> 
   <th class="entry"> <b>Titel-ID</b> </th> 
   <th class="entry"> <b>Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Gesperrte Anfrage </p> </td> 
   <td> <p>Sperren </p> </td> 
   <td> <p>Wird gesendet, wenn eine Anfrage innerhalb des angegebenen Schwellenwerts keine Antwort an den Client zurückgibt. Kann ein Hinweis auf hängende Anfragen sein, die zu einer Deaktivierung des Java-Thread-Pools führen können. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Hohe gleichzeitige Nutzung </p> </td> 
   <td> <p>Konz </p> </td> 
   <td> Wird ausgegeben, wenn die Anzahl der gleichzeitig verarbeiteten Anfragen (die <i>Überschneidung</i>) den angegebenen Schwellenwert überschreitet. Kann auf eine Serverüberlastung hinweisen. </td> 
  </tr> 
  <tr> 
   <td> <p>Mindestverkehr </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Wird generiert, wenn die Gesamtanfragerate unter den angegebenen Schwellenwert fällt. Zeigt normalerweise ein Problem mit der Server-Kommunikation an (z. B. wenn ein Server offline geschaltet wird). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fehlerrate </p> </td> 
   <td> <p>Fehler </p> </td> 
   <td> <p>Wird ausgegeben, wenn die durchschnittliche Rate von HTTP-Fehlerantworten während des Sampling-Intervalls den angegebenen Schwellenwert überschreitet. Kann ein Hinweis auf Konfigurationsprobleme, fehlende Bilder oder Website-Programmierung oder Datenbankfehler sein. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Antwortzeit </p> </td> 
   <td> <p>Time </p> </td> 
   <td> <p>Wird gesendet, wenn die durchschnittliche Verarbeitungszeit für Anfragen während des Sampling-Intervalls den angegebenen Schwellenwert überschreitet. Zeigt normalerweise eine temporäre oder persistente Überlastung des Server- oder Backend-Bildspeichersystems an. </p> <p>Fehlerantworten werden bei der Berechnung der durchschnittlichen Antwortzeit nicht berücksichtigt. </p> </td> 
  </tr> 
 </tbody> 
</table>
