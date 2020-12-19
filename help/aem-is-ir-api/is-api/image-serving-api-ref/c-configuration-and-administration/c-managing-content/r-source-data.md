---
description: Zu den Image Serving-Quelldatendateien gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.
seo-description: Zu den Image Serving-Quelldatendateien gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.
seo-title: Quelldaten
solution: Experience Manager
title: Quelldaten
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Quelldaten{#source-data}

Zu den Image Serving-Quelldatendateien gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.

Alle Quelldatendateien müssen für den Image-Server zugänglich sein. Image Serving bietet eine Reihe von Alternativen zum Festlegen des Speicherorts von Datendateien:

` *`install_`*/ *``*/ *`folderrootPathfilePath`*`

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

Alle ` *`rootPath`*`-Segmente können leere, relative oder absolute Pfadsegmente sein.

` *`Fügen Sie `*` hier entweder einen absoluten oder relativen Dateipfad/Dateinamen ein. ` *``*` requestPath muss ein relativer Dateipfad/Name sein.

`Multiple IS::RootPath` Werte können in ImageServerRegistry.xml (oder über die Admin-Oberfläche) definiert werden. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der Image-Server versucht, alternative Pfade in der angegebenen Reihenfolge zu verwenden, bis die Datendatei gefunden wurde.

Neue Datendateien jeder Art können jederzeit hinzugefügt werden, ohne den Server zu beenden.
