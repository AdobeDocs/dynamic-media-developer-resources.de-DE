---
title: Anforderungen an Speicherplatz und Empfehlungen
description: Neben dem für die Installation der Software erforderlichen Speicherplatz weist Image Serving die folgenden Speicherplatzanforderungen auf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Anforderungen an Speicherplatz und Empfehlungen{#disk-space-requirements-and-recommendations}

Neben dem für die Installation der Software erforderlichen Speicherplatz weist Image Serving die folgenden Speicherplatzanforderungen auf:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Beschreibung/Standardposition/-satz mit</b> </th> 
   <th class="entry"> <b>Berechnung/Empfehlung</b> </th> 
   <th class="entry"> <b>Kommentare</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Quellbilder, Schriftarten, ICC-Profile</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Variiert; siehe Kommentare unten. </p> </td> 
   <td> <p>Nur der Image-Server darf darauf zugreifen; die Server ändern keine Daten. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP-Antwortdaten-Cache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; mindestens 2 GB empfohlen. </p> </td> 
   <td> <p>Dieser Cache speichert außerdem verschachtelte/eingebettete Daten und Bilder aus ausländischen Quellen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache für Bildkatalogdaten</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Lassen Sie zu, dass der Katalogordner das 1,5-fache Leerzeichen verwendet. </p> </td> 
   <td> <p>Wird beim ersten Laden von Katalogen aufgefüllt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Protokolldaten</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 MB oder mehr. </p> </td> 
   <td> <p>Dies hängt von der Protokollierungskonfiguration und der Verwendung des Servers ab. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Temporäre Dateien für Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MB sind für die meisten Verwendungen ausreichend. </p> </td> 
   <td> <p>Kurzlebige Daten; können für andere Quellbilder als PTIFFs und bestimmte Antwortbildformate benötigt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Speicherplatzanforderungen für Quellbilder {#section-317da75099ad480d9a461c7e706d4f1c}

Adobe empfiehlt, alle Quellbilder mithilfe des Befehlszeilenwerkzeugs (IC) von Image Converter in das Pyramid TIFF-Dateiformat (PTIFF) zu konvertieren. Diese Konvertierung gewährleistet eine optimale Laufzeitleistung des Image Serving für alle Anwendungen. Während der Image-Server alle von IC akzeptierten Quelldateiformate verarbeiten kann, unterstützt Dynamic Media diese Verwendung nicht.

Wenn Sie PTIFF-Dateien verwenden, helfen Ihnen die folgenden Faustregeln bei der Bestimmung der Platzanforderungen.

*`total_space`* (Byte) = *`number_of_images`*  × (2000 + *`avg_pixel_count`* x *`avg_num_components`*  ×  *`p_factor`*)

* *`avg_pixel_count`* Die durchschnittliche Pixelgröße (Breite x Höhe) aller Originalbilder. Wenn die Originalbilder beispielsweise in der Regel etwa 2 KB × 2 KB Pixel groß sind, wären dies 4 Megapixel.
* *`avg_num_components`* Hängt vom Typ der Bilder ab. Für die meisten RGB-Bilder ist es 3, für meist CMYK- oder RGBA-Bilder 4. Verwenden Sie 3,5, wenn die Hälfte der Bilder RGB und die andere Hälfte RGBA ist.
* *`p_factor`* Hängt vom Komprimierungstyp und von der Qualität ab, die bei der Konvertierung der Bilder mit IC eingestellt werden.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF-Komprimierung</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>unkomprimiert </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Komprimierung </p> </td> 
   <td> <p> 25-0,75, je nach Bild </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG-Komprimierung </p> </td> 
   <td> <p> 1 (typisch für JPEG-Qualität 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Annäherung berücksichtigt nicht den Verwaltungsaufwand des Dateisystems. Der tatsächliche Speicherplatz auf der Festplatte kann erheblich größer sein.

**Beispiel**

Bei einer Image Serving-Bereitstellung werden voraussichtlich 30.000 ältere Bilder mit niedriger Auflösung mit einer durchschnittlichen Größe von 500 × 500 RGB Pixel verwendet. Neue Bilddaten in Druckqualität werden mit einer Rate von 10.000 pro Jahr hinzugefügt. Die typische CMYK-Bildgröße beträgt 4 k × 6 k Byte. Alle Daten werden mit hoher JPEG-Qualität komprimiert. Die Gesamtmenge des Festplattenspeichers nach dreijähriger Nutzung wird wie folgt geschätzt:

*`total_space`* = 30,000 × (2k + 0,5k × 0,5k × 3 × 0,1) + 3 × 10,000 × (2k + 4k × 6k × 4 × 0,1) = 2,2 G + 268 GB = ca. 270 GB

Für eine garantierte beste Qualität kann eine Komprimierung wie zip verwendet werden. Angenommen, ein *`p_factor`* von 0,4 ist der insgesamt erforderliche Speicherplatz etwa viermal größer. In diesem Fall etwas mehr als 1 Terabyte.
