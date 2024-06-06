---
description: Bildvalidierungsprogramm. Dieses Befehlszeilen-Dienstprogramm überprüft Bilddateien, um sicherzustellen, dass sie gültig sind und Image Serving sie problemlos lesen kann.
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

Bildvalidierungsprogramm. Dieses Befehlszeilen-Dienstprogramm überprüft Bilddateien, um sicherzustellen, dass sie gültig sind und problemlos von Image Serving gelesen werden können.

Alle Nicht-PTIFF-Bilddateien müssen die Validierung bestehen, bevor die Datei als Quellbild für Image Serving verfügbar gemacht wird. PTIFF-Bilder sollten nach potenziell unzuverlässigen Kopiervorgängen validiert werden.

## Nutzung {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>Quelldateityp; mindestens ein muss angegeben werden (-any lässt dieselben Bilddateitypen zu, die von IC unterstützt werden). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options </span> </span> </p> </td> 
  <td class="stentry"> <p>Andere Befehlsoptionen (siehe unten). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Bilddatei. Keine oder mehr, durch Leerzeichen getrennt. </p> </td> 
 </tr> 
</table>

## Rückgabe {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 bei Erfolg. Wenn ein Fehler auftritt, wird ein Wert ungleich null zurückgegeben und Fehlerdetails werden an gesendet `stderr`.

## Optionen {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Gibt eine separate Textdatei an, die die Liste der Bilddateien enthält. Ein Datensatz pro Datei. Wenn <span class="codeph"> -fileList </span> enthalten ist, <span class="varname"> sourceFile </span> darf nicht angegeben werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Aktiviert die Überprüfung der gesamten Bilddatei. Standardmäßig wird nur die Bildkopfzeile validiert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Überprüft das eingebettete Farbprofil auf Gültigkeit. Standardmäßig ist das Hauptteilprofil nicht aktiviert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> lehnt Bilder mit 16 Bit pro Bildkomponente ab. Wird immer vom Image-Server bei der Überprüfung von Remote-Quellbildern angegeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Druckt weitere Informationen, wenn das Bild ungültig ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>Deaktiviert <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> Ausgabe. Es wird nur ein Status zurückgegeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Beendet die Verarbeitung, wenn bei der Dateivalidierung ein Fehler auftritt, auch wenn noch weitere Dateien validiert werden müssen. Die Verarbeitung wird standardmäßig fortgesetzt, wenn ein Validierungsfehler auftritt </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Gibt Versionsinformationen für dieses Dienstprogramm zurück. Geben Sie ohne weitere Optionen an. </p> </td> 
 </tr> 
</table>
