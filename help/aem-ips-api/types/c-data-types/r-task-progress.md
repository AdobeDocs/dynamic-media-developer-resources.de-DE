---
description: Informationen zum Fortschritt der Aufgabe.
seo-description: Informationen zum Fortschritt der Aufgabe.
seo-title: TaskProgress
solution: Experience Manager
title: TaskProgress
topic: Scene7 Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TaskProgress{#taskprogress}

Informationen zum Fortschritt der Aufgabe.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Beschreibung der Aufgabe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcess</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Anzahl der bereits verarbeiteten Elemente der Aufgabe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Anzahl der derzeit bearbeiteten Elemente der Aufgabe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Anzahl der ausstehenden Elemente der Aufgabe (noch nicht verarbeitet). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Fortschritt</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Dublette</span> </td> 
   <td colname="col3"> % Fortschritt (Bereich 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Statusmeldung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> lastProgressUpdate <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Zeitpunkt der letzten Aktualisierung der Statusinformationen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Array von Elementen der Aufgabe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Die Werte umfassen: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Unbekannt</span>: Wenn die Aufgabe Transitionen zwischen Status überwacht. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Neu</span>: Aufgabe Monitor wurde erstellt, hat aber noch keine Aufgaben akzeptiert. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Verarbeitung</span>: Aufgabe Monitor verarbeitet aktiv Aufgaben. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Anhalten</span>: Aufgabe Monitor beendet einen Auftrag aufgrund einer Anforderung zum Beenden des Auftrags. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Fertig</span>: Aufträge, die den Aufgaben-Monitoraufträgen zugewiesen wurden, wurden abgeschlossen. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Fehlgeschlagen</span>: Gibt einen schwerwiegenden Fehler an. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

