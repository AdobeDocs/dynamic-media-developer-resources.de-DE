---
description: Zu den Quelldatendateien für Image Serving gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.
solution: Experience Manager
title: Source-Daten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Source-Daten{#source-data}

Zu den Quelldatendateien für Image Serving gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.

Alle Quelldatendateien müssen für den Image-Server verfügbar sein. Image Serving bietet eine Reihe von Alternativen zum Festlegen des Speicherorts von Datendateien:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> relativer Pfad und Name der Bilddatei, der in einer Image Serving HTTP-Anforderung angegeben ist</span> </p></td> 
 </tr> 
</table>

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt ist.

Alle `*`rootPath`*` -Segmente können leere, relative oder absolute Pfadsegmente sein.

`*`catalogPath`*` ist entweder ein absoluter oder relativer Dateipfad/-name. `*`requestPath`*` muss ein relativer Dateipfad/Dateiname sein.

`Multiple IS::RootPath` -Werte können in ImageServerRegistry.xml (oder über die Admin-Oberfläche) definiert werden. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der Image-Server versucht alternative Pfade in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.

Neue Datendateien jeder Art können jederzeit hinzugefügt werden, ohne den Server zu stoppen.
