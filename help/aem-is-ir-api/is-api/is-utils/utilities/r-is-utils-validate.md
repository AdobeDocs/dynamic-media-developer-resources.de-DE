---
description: Dienstprogramm zur Bildvalidierung. Dieses Befehlszeilenprogramm überprüft Bilddateien, um sicherzustellen, dass sie gültig sind und von Image Serving problemlos gelesen werden können.
solution: Experience Manager
title: validieren
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---

# validieren{#validate}

Dienstprogramm zur Bildvalidierung. Dieses Befehlszeilenprogramm überprüft Bilddateien, um sicherzustellen, dass sie gültig sind und von der Bildbereitstellung problemlos gelesen werden können.

Alle Nicht-PTIFF-Bilddateien müssen die Validierung bestehen, bevor die Datei Image Serving als Quellbild zur Verfügung gestellt wird. PTIFF-Bilder sollten nach potenziell unzuverlässigen Kopiervorgängen validiert werden.

## Nutzung {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -Beliebige </span> </p> <p>Source-Dateityp; es muss mindestens einer angegeben werden (-any lässt dieselben Bilddateitypen zu, die von IC unterstützt werden). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Optionen </span> </span> </p> </td> 
  <td class="stentry"> <p>Andere Befehlsoptionen (siehe unten). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Bilddatei. Keine oder mehr, durch Leerzeichen getrennt. </p> </td> 
 </tr> 
</table>

## Rückgabe {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 bei Erfolg. Wenn ein Fehler auftritt, wird ein Wert ungleich null zurückgegeben und Fehlerdetails werden an `stderr` gesendet.

## Optionen {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Gibt eine separate Textdatei an, die die Liste der Bilddateien enthält. Ein Datensatz pro Datei. Wenn <span class="codeph"> -fileList-</span> enthalten ist, darf <span class="varname"> sourceFile-</span> nicht angegeben werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels-</span> </p> </td> 
  <td class="stentry"> <p>Ermöglicht die Überprüfung der gesamten Bilddatei. Standardmäßig wird nur die Bildkopfzeile validiert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateColorProfile-</span> </p> </td> 
  <td class="stentry"> <p>Prüft das eingebettete Farbprofil auf Gültigkeit. Standardmäßig ist das Hauptteilprofil nicht aktiviert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -ject16BitPerComponent-</span> </p> </td> 
  <td class="stentry"> <p> Lehnt Bilder mit 16 Bit pro Bildkomponente ab. Wird vom Bildserver immer angegeben, wenn Remote-Quellbilder validiert werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Druckt weitere Informationen, wenn das Bild ungültig ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - stille </span> </p> </td> 
  <td class="stentry"> <p>Deaktiviert <span class="codeph"> Ausgabe von stdout </span>/ <span class="codeph"> stderr </span>. Es wird nur ein Status zurückgegeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError-</span> </p> </td> 
  <td class="stentry"> <p>Beendet die Verarbeitung, wenn ein Dateivalidierungsfehler auftritt, selbst wenn zusätzliche Dateien noch validiert werden müssen. Standardmäßig wird die Verarbeitung bei einem Validierungsfehler fortgesetzt </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Gibt Versionsinformationen für dieses Dienstprogramm aus. Geben Sie ohne andere Optionen an. </p> </td> 
 </tr> 
</table>
