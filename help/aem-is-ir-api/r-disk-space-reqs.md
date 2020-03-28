---
description: 'Zusätzlich zum für die Installation der Software erforderlichen Speicherplatz verfügt Image Serving über die folgenden Speicherplatzanforderungen '
seo-description: 'Zusätzlich zum für die Installation der Software erforderlichen Speicherplatz verfügt Image Serving über die folgenden Speicherplatzanforderungen '
seo-title: Speicherplatzanforderungen und Empfehlungen
solution: Experience Manager
title: Speicherplatzanforderungen und Empfehlungen
topic: Scene7 Image Serving - Image Rendering API
uuid: a6a21886-94d6-45b3-af68-497e039bdbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Speicherplatzanforderungen und Empfehlungen{#disk-space-requirements-and-recommendations}

Zusätzlich zu dem für die Installation der Software erforderlichen Speicherplatz verfügt Image Serving über folgende Speicherplatzanforderungen:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Beschreibung/ Standardposition/-satz</b> </th> 
   <th class="entry"> <b>Berechnung/Empfehlung</b> </th> 
   <th class="entry"> <b>Kommentare</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Quellbilder, Schriftarten, ICC-Profile</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span><span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varianten; siehe Kommentare unten. </p> </td> 
   <td> <p>Nur der Zugriff auf den Image-Server ist erforderlich. die Server ändern nie Daten. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP-Antwortdatencache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; mindestens 2 GB empfohlen. </p> </td> 
   <td> <p>Dieser Cache speichert auch verschachtelte/eingebettete Daten und Bilder aus ausländischen Quellen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Datencache des Bildkatalogs</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Der Katalogordner darf das 1,5-fache Leerzeichen verwenden. </p> </td> 
   <td> <p>Wird ausgefüllt, wenn Kataloge zum ersten Mal geladen werden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Protokolldaten</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 MB oder mehr. </p> </td> 
   <td> <p>Je nach Protokollierungskonfiguration und Serververwendung unterschiedlich. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Temporäre Dateien des Image-Servers</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MBytes sind für die meisten Anwendungen ausreichend. </p> </td> 
   <td> <p>Daten mit kurzer Lebensdauer; kann für andere Quellbilder als PTIFFs und bestimmte Antwortbildformate benötigt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Speicherplatzanforderungen für Quellbilder {#section-317da75099ad480d9a461c7e706d4f1c}

Es wird empfohlen, alle Quellbilder mit dem Bildkonverter-Befehlszeilenwerkzeug (IC) in das Pyramid TIFF-Dateiformat (PTIFF) zu konvertieren. Diese Konvertierung gewährleistet eine optimale Laufzeitleistung des Image Serving für alle Anwendungen. Während der Image-Server alle von IC akzeptierten Quelldateiformate verarbeiten kann, bietet Scene7 keine Unterstützung für solche Verwendungen.

Wenn Sie PTIFF-Dateien verwenden, können Sie mithilfe der folgenden Faustregeln die Platzanforderungen festlegen.

*`total_space`* (Byte) = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* Die durchschnittliche Pixelgröße (Breite x Höhe) aller Originalbilder. Wenn die Originalbilder beispielsweise in der Regel ca. 2.000 x 2.000 Pixel groß sind, beträgt dies 4.000 Pixel.
* *`avg_num_components`* Hängt vom Bildtyp ab. Bei meist RGB-Bildern ist es 3, bei meist CMYK- oder RGBA-Bildern 4. Verwenden Sie 3,5, wenn die Hälfte der Bilder RGB und die andere Hälfte RGBA sind.
* *`p_factor`* Hängt vom Komprimierungstyp und der Qualitätseinstellung ab, wenn die Bilder mit IC konvertiert werden.

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
>Diese Annäherung berücksichtigt nicht den Dateisystemaufwand. Der eigentliche Speicherplatz auf der Festplatte kann wesentlich größer sein.

**Beispiel**

Bei einer Image Serving-Bereitstellung werden voraussichtlich 30.000 ältere Bilder mit niedriger Auflösung und einer durchschnittlichen Größe von 500 x 500 RGB-Pixeln verwendet. Es wird erwartet, dass neue Bilddaten in Druckqualität mit einer Rate von 10.000 pro Jahr hinzugefügt werden. Die typische CMYK-Bildgröße beträgt 4.000 x 6.000 Byte. Alle Daten werden mit hoher Qualität JPEG komprimiert. Der gesamte Speicherplatz nach 3 Jahren Nutzung wird wie folgt geschätzt:

*`total_space`* = 30.000 x (2k + 0,5k x 0,5k x 3 x 0,1) + 3 x 10.000 x (2k + 4k x 6k x 4 x 0,1) = 2,2 G + 268 GB = ca. 270 GB

Für eine garantiert beste Qualität kann eine Deflate-Komprimierung (zip) verwendet werden. Wenn man *`p_factor`* von 0,4 ausgeht, ist der benötigte Speicherplatz insgesamt etwa viermal größer. In diesem Fall etwas mehr als 1 TB.
