---
description: Bild in Datei speichern
seo-description: Bild in Datei speichern
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveToFile{#savetofile}

Bild in Datei speichern

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Datei</span> </p> </td> 
  <td class="stentry"> <p>Relativer Pfad zur Bilddatei der Zielgruppe. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Zeitüberschreitungsintervall (Millisekunden). </p></td> 
 </tr> 
</table>

Speichert das Antwortbild in einer Datei auf dem Server, anstatt es an den Client zurückzugeben.

Nach erfolgreichem Abschluss der Speicheranforderung gibt die Anforderung mehrere Java-formatierte Eigenschaften zurück, darunter die folgenden:

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
   <td> <p> <span class="codeph"> bei erfolgreicher Ausführung</span> durchgeführt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Gibt HTTP-Antwortstatus 200 bei erfolgreicher Ausführung und 403 zurück, wenn die Anforderung fehlschlägt oder abgelaufen ist. Die Antwort hat den MIME-Typ `text/plain` und kann nicht zwischengespeichert werden.

Wichtiges Speichern in Dateien muss aktiviert werden, indem der Pfad zu einem vorhandenen schreibbaren Ordner in `attribute::SavePath`angegeben wird. `saveToFile=` schlägt fehl, wenn `attribute::SavePath` leer ist.

*`file`* ist erforderlich und muss ein relativer Pfad sein, der mit `attribute::SavePath`kombiniert wird. Mit Image Serving werden keine Ordner erstellt. Der Ordner &quot;Zielgruppe&quot;muss auf dem Server vorhanden sein und über die entsprechenden Dateieinstellungen zum Erstellen von  für Image Serving verfügen.

`timeout=` ist optional. Der Standardwert für die Zeitüberschreitung ist 60.000 msec oder der Wert, mit dem `PS::SaveTimeout`der Wert konfiguriert wurde.
