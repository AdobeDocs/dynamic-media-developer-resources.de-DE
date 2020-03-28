---
description: Dienstprogramm zur Bildüberprüfung. Dieses Befehlszeilendienstprogramm überprüft die Bilddateien, um sicherzustellen, dass sie gültig sind und problemlos von Image Serving gelesen werden können.
seo-description: Dienstprogramm zur Bildüberprüfung. Dieses Befehlszeilendienstprogramm überprüft die Bilddateien, um sicherzustellen, dass sie gültig sind und problemlos von Image Serving gelesen werden können.
seo-title: validieren
solution: Experience Manager
title: validieren
topic: Scene7 Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# validieren{#validate}

Dienstprogramm zur Bildüberprüfung. Dieses Befehlszeilendienstprogramm überprüft die Bilddateien, um sicherzustellen, dass sie gültig sind und problemlos von Image Serving gelesen werden können.

Alle Nicht-PTIFF-Bilddateien müssen validiert werden, bevor die Datei als Quellbild für Image Serving zur Verfügung gestellt wird. PTIFF-Bilder sollten nach potenziell unzuverlässigen Kopiervorgängen validiert werden.

## Nutzung {#usage}

` validate *``* [ *``*] [ *`fileTypeOptionsSourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg| -ptif| -any </span> </p> <p>Art der Quelldatei; muss mindestens einer angegeben werden (-beliebige erlaubt die gleichen Bilddateitypen, die von IC unterstützt werden). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Optionen </span></span> </p> </td> 
  <td class="stentry"> <p>Andere Befehlsoptionen (siehe unten). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span></span> </p> </td> 
  <td class="stentry"> <p> Bilddatei. Keine oder mehr, durch Leerzeichen getrennt. </p> </td> 
 </tr> 
</table>

## Returns {#section-67a7cf7c53144fbb8f24b818f4a10901}

0, wenn erfolgreich. Wenn ein Fehler auftritt, wird ein Wert von ungleich null zurückgegeben und Fehlerdetails werden an gesendet `stderr`.

## Optionen {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList- <span class="varname"> Listendatei </span></span> </p> </td> 
  <td class="stentry"> <p>Gibt eine separate Textdatei an, die die Liste der Bilddateien enthält. Ein Datensatz pro Datei. Wenn <span class="codeph"> -fileList </span> enthalten ist, darf <span class="varname"> sourceFile nicht angegeben </span> werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Aktiviert die Überprüfung der gesamten Bilddatei. Standardmäßig wird nur die Bildüberschrift überprüft. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Prüft die Gültigkeit des eingebetteten Profils. Standardmäßig ist der Textkörper des Profils nicht markiert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -gewiesen16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> lehnt Bilder mit 16 Bit pro Bildkomponente ab. Wird immer vom Image-Server bei der Überprüfung von Remote-Quellbildern angegeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Druckt weitere Informationen, wenn das Bild ungültig ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>Deaktiviert die <span class="codeph"> stdout- </span>/ <span class="codeph"> stderr- </span> Ausgabe. Es wird nur ein Status zurückgegeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Beendet die Verarbeitung, wenn ein Fehler bei der Dateivalidierung auftritt, selbst wenn noch weitere Dateien überprüft werden müssen. Standardmäßig wird die Verarbeitung fortgesetzt, wenn ein Überprüfungsfehler auftritt </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Version </span> </p> </td> 
  <td class="stentry"> <p>Gibt Versionsinformationen für dieses Dienstprogramm zurück. Geben Sie ohne weitere Optionen an. </p> </td> 
 </tr> 
</table>

