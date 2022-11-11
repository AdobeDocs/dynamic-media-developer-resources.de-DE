---
description: Informationen zum Aufgabenfortschritt
solution: Experience Manager
title: TaskProgress
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 35e3be1e-ccc2-460c-98c1-bbefab1df699
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---

# [!DNL TaskProgress]{#taskprogress}

Informationen zum Aufgabenfortschritt

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Beschreibung des Aufgabentyps. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Anzahl der bereits verarbeiteten Aufgabenelemente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Anzahl der derzeit verarbeiteten Aufgabenelemente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Anzahl der ausstehenden Aufgabenelemente (noch nicht verarbeitet). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progress</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Fortschritt in % (Bereich 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Fortschrittsmeldung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Zeitpunkt der letzten Aktualisierung der Fortschrittsinformationen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Array von Aufgabenelementen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Zu den Werten gehören: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> unbekannt</span>: Wenn die Aufgabenüberwachung zwischen Status wechselt. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Neu</span>: Der Aufgabenmonitor wurde erstellt, hat jedoch noch keine Aufgaben akzeptiert. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Verarbeitung</span>: Die Aufgabenüberwachung verarbeitet aktiv Aufgaben. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Anhalten</span>: Der Aufgabenmonitor stoppt einen Auftrag aufgrund einer Anfrage zum Anhalten des Vorgangs. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Fertig</span>: Die den Aufgabenüberwachungsaufträgen zugewiesenen Aufträge wurden abgeschlossen. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Fehlgeschlagen</span>: Gibt einen schwerwiegenden Fehler an. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
