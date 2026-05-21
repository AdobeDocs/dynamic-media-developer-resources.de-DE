---
description: Zu den Quelldatendateien der Bildbereitstellung gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.
solution: Experience Manager
title: Source-Daten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
TQID: 'https://experienceleague.adobe.com/36EvEOjHZ8ik-gps-vaap5PhFCf5rwV9ecfkKHZcIhk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Source-Daten{#source-data}

Zu den Quelldatendateien der Bildbereitstellung gehören Bild- und Maskendateien, Schriftarten und ICC-Profile.

Alle Quelldatendateien müssen für den Bildserver zugänglich sein. Die Bildbereitstellung bietet eine Reihe von Alternativen zum Angeben des Speicherorts von Datendateien:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath-</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> in einer Image-Serving-HTTP-Anfrage angegebene relative Bilddateipfad und -name</span> </p></td> 
 </tr> 
</table>

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt wird.

Alle `*`rootPath`*`-Segmente können leere, relative oder absolute Pfadsegmente sein.

`*`catalogPath`*` ist entweder ein absoluter oder relativer Dateipfad/Name. `*`requestPath`*` muss ein relativer Dateipfad/Name sein.

`Multiple IS::RootPath` können in ImageServerRegistry.xml (oder über die Admin-Schnittstelle) definiert werden. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der Bild-Server versucht alternative Pfade in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.

Neue Datendateien jeglicher Art können jederzeit hinzugefügt werden, ohne den Server anzuhalten.
