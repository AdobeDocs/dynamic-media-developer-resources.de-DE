---
description: Speichern Sie das Bild in der Datei.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# saveToFile{#savetofile}

Speichern Sie das Bild in der Datei.

`req=saveToFile&name= *`file`*[&timeout= *`val`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>Relativer Pfad zur Zielbilddatei. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Zeitüberschreitungsintervall (Millisekunden). </p></td> 
 </tr> 
</table>

Speichert das Antwortbild in einer Datei auf dem Server, anstatt es an den Client zurückzugeben.

Wenn die Speicheranfrage erfolgreich abgeschlossen wurde, gibt die Anfrage mehrere Java-formatierte Eigenschaften zurück, darunter die folgenden:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Eigenschaft</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Zeit der Dateierstellung (Anzahl der Millisekunden seit Mitternacht, 1. Januar 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelTotal</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Anzahl der Pixel im gespeicherten Bild. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> done</span> bei Erfolg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Gibt den HTTP-Antwortstatus 200 bei Erfolg zurück und 403, wenn die Anfrage fehlschlägt oder eine Zeitüberschreitung aufweist. Die Antwort hat den MIME-Typ `text/plain` und ist nicht zwischenspeicherbar.

&quot;Wichtiges Speichern in Dateien&quot;muss aktiviert sein, indem der Pfad zu einem vorhandenen beschreibbaren Ordner in `attribute::SavePath` angegeben wird. `saveToFile=` schlägt fehl, wenn `attribute::SavePath` leer ist.

*`file`* ist erforderlich und muss ein relativer Pfad sein, der mit `attribute::SavePath` kombiniert wird. Image Serving erstellt keine Ordner. Der Zielordner muss auf dem Server vorhanden sein und über die entsprechenden Berechtigungseinstellungen für Image Serving verfügen, um Dateien zu erstellen.

`timeout=` ist optional. Der Standardwert für die Zeitüberschreitung beträgt 60.000 ms oder der Wert, der mit `PS::SaveTimeout` konfiguriert ist.
