---
description: 'Zusätzlich zu dem für die Installation der Software erforderlichen Speicherplatz weist Image Serving die folgenden Speicherplatzanforderungen auf '
solution: Experience Manager
title: Anforderungen an Speicherplatz und Empfehlungen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Anforderungen an Speicherplatz und Empfehlungen{#disk-space-requirements-and-recommendations}

Zusätzlich zu dem für die Installation der Software erforderlichen Speicherplatz bietet Image Serving die folgenden Speicherplatzanforderungen:

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
   <td> <p>Varianten; siehe Kommentare unten. </p> </td> 
   <td> <p>Nur der Zugriff auf den Image-Server muss möglich sein. die Server ändern nie Daten. </p> </td> 
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
   <td> <p>100 MByte oder mehr. </p> </td> 
   <td> <p>variiert je nach Protokollierungskonfiguration und Verwendung des Servers. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Temporäre Dateien für Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MByte sind für die meisten Verwendungen ausreichend. </p> </td> 
   <td> <p>Kurzlebige Daten; kann für andere Quellbilder als PTIFFs und bestimmte Antwortbildformate benötigt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Speicherplatzanforderungen für Quellbilder {#section-317da75099ad480d9a461c7e706d4f1c}

Es wird empfohlen, alle Quellbilder mithilfe des Image Converter-Befehlszeilen-Tools (IC) in das Pyramid TIFF-Dateiformat (PTIFF) zu konvertieren. Diese Konvertierung gewährleistet eine optimale Laufzeitleistung des Image Serving für alle Anwendungen. Während der Image-Server alle von IC akzeptierten Quelldateiformate verarbeiten kann, bietet Dynamic Media keine Unterstützung für solche Verwendungen.

Wenn Sie PTIFF-Dateien verwenden, helfen Ihnen die folgenden Faustregeln bei der Bestimmung der Platzanforderungen.

*`total_space`* (Byte) = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* Die durchschnittliche Pixelgröße (Breite x Höhe) aller Originalbilder. Wenn die Originalbilder beispielsweise in der Regel etwa 2.000 x 2.000 Pixel groß sind, wären dies 4.000 Pixel.
* *`avg_num_components`* Hängt vom Typ der Bilder ab. Für die meisten RGB-Bilder ist es 3, für meist CMYK- oder RGBA-Bilder ist es 4. Verwenden Sie 3,5, wenn die Hälfte der Bilder RGB und die andere Hälfte RGBA ist.
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
   <td> <p>Nicht komprimiert </p> </td> 
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

Bei einer Image Serving-Bereitstellung werden voraussichtlich 30.000 ältere Bilder mit niedriger Auflösung mit einer durchschnittlichen Größe von 500 x 500 RGB Pixel verwendet. Es wird erwartet, dass neue Bilddaten in Druckqualität mit einer Rate von 10.000 pro Jahr hinzugefügt werden. Die typische CMYK-Bildgröße beträgt 4.000 x 6.000 Byte. Alle Daten werden mit hoher JPEG-Qualität komprimiert. Die Gesamtmenge des Festplattenspeichers nach dreijähriger Nutzung wird wie folgt geschätzt:

*`total_space`* = 30.000 x (2 k + 0,5 k x 0,5 k x 3 x 0,1) + 3 x 10.000 x (2 k + 4 k x 6 k x 4 x 0,1) = 2,2 G + 268 GB = ca. 270 GB

Für eine garantierte beste Qualität kann eine Deflate-Komprimierung (zip) verwendet werden. Angenommen, ein *`p_factor`* von 0,4 ist der insgesamt erforderliche Speicherplatz etwa viermal größer. In diesem Fall etwas mehr als 1 TB.
