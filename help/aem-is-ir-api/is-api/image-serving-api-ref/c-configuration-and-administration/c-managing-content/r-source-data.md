---
description: Zu den Image Serving-Quelldatendateien gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.
solution: Experience Manager
title: Quelldaten
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Quelldaten{#source-data}

Zu den Image Serving-Quelldatendateien gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.

Alle Quelldatendateien müssen für den Image-Server zugänglich sein. Image Serving bietet eine Reihe von Alternativen zum Festlegen des Speicherorts von Datendateien:

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> Pfad und Name der relativen Bilddatei, die in einer Image Serving-HTTP-Anforderung angegeben wurden</span> </p></td> 
 </tr> 
</table>

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt ist.

Alle `*`rootPath`*`-Segmente können leere, relative oder absolute Pfadsegmente sein.

`*`Fügen Sie `*` hier entweder einen absoluten oder relativen Dateipfad/Dateinamen ein. `*``*` requestPath muss ein relativer Dateipfad/Name sein.

`Multiple IS::RootPath` Werte können in ImageServerRegistry.xml (oder über die Admin-Oberfläche) definiert werden. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der Image-Server versucht, in der angegebenen Reihenfolge alternative Pfade auszuprobieren, bis die Datendatei gefunden wurde.

Neue Datendateien jeder Art können jederzeit hinzugefügt werden, ohne den Server zu beenden.
