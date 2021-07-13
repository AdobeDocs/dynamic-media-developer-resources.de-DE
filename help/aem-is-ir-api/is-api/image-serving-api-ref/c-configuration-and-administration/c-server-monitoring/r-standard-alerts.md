---
description: Standardwarnungen werden mit einer konsolidierten E-Mail-Nachricht am Ende des konfigurierten Durchschnitts gesendet.
solution: Experience Manager
title: Standardmäßige Warnungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Standardmäßige Warnungen{#standard-alerts}

Standardwarnungen werden mit einer konsolidierten E-Mail-Nachricht am Ende des konfigurierten Durchschnitts gesendet.

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
   <td> <p>Wird gesendet, wenn eine Anfrage innerhalb des angegebenen Schwellenwerts keine Antwort an den Client zurückgibt. Kann auf hängende Anfragen hinweisen, was zu einer Erschöpfung des Java-Thread-Pools führen kann. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Hohe Gleichzeitigkeit </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Wird ausgegeben, wenn die Anzahl der gleichzeitig verarbeiteten Anforderungen (die <i>überlappenden</i>) den festgelegten Schwellenwert überschreitet. Kann auf eine Überlastungsbedingung des Servers hinweisen. </td> 
  </tr> 
  <tr> 
   <td> <p>Minimaler Traffic </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Wird generiert, wenn die Gesamtanfragerate unter den angegebenen Schwellenwert fällt. Gibt typischerweise ein Problem mit der Serverkommunikation an (z. B. wenn ein Server aus der Warteschlange genommen wird). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fehlerrate </p> </td> 
   <td> <p>Fehler </p> </td> 
   <td> <p>Wird ausgegeben, wenn die durchschnittliche Rate von HTTP-Fehlerantworten während des Sampling-Intervalls den festgelegten Schwellenwert überschreitet. Kann auf Konfigurationsprobleme, fehlende Bilder, Website-Programmierung oder Datenbankfehler hinweisen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Reaktionszeit </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Wird gesendet, wenn die durchschnittliche Verarbeitungszeit für Anfragen während des Stichprobenintervalls über dem festgelegten Schwellenwert liegt. Gibt normalerweise eine vorübergehende oder dauerhafte Überlastungsbedingung des Server- oder Backend-Bildspeichersystems an. </p> <p>Fehlerantworten werden bei der Berechnung der durchschnittlichen Antwortzeit nicht berücksichtigt. </p> </td> 
  </tr> 
 </tbody> 
</table>
