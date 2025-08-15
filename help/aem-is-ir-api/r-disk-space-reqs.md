---
title: Anforderungen und Empfehlungen an den Festplattenspeicher
description: Neben dem erforderlichen Speicherplatz für die Installation der Software stellt Image Serving die folgenden Anforderungen an den erforderlichen Speicherplatz.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Anforderungen und Empfehlungen an den Festplattenspeicher{#disk-space-requirements-and-recommendations}

Neben dem erforderlichen Speicherplatz für die Installation der Software stellt Image Serving die folgenden Anforderungen an den Festplattenspeicher:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Beschreibung/ Standardspeicherort/ festlegen mit</b> </th> 
   <th class="entry"> <b>Berechnung/Empfehlung</b> </th> 
   <th class="entry"> <b>Kommentare</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Source-Bilder, Schriftarten, ICC-Profile</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>variiert; siehe Kommentare unten. </p> </td> 
   <td> <p>Nur für den Bildserver muss zugänglich sein. Die Server ändern die Daten nie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP-Antwort-Daten-Cache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders-</span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; mindestens 2 GB empfohlen. </p> </td> 
   <td> <p>Dieser Cache speichert auch verschachtelte/eingebettete Daten und fremde Quellbilder. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache für Bildkatalogdaten</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder-</span> </p> </td> 
   <td> <p>Der Katalogordner darf das 1,5-fache des Platzes belegen. </p> </td> 
   <td> <p>Wird beim erstmaligen Laden von Katalogen befüllt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Protokolldaten</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder-</span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile-</span> </p> </td> 
   <td> <p>100 MB oder mehr. </p> </td> 
   <td> <p>Er variiert je nach Protokollierungskonfiguration und Server-Nutzung. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Temporäre Dateien des Bildservers</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory-</span> </p> </td> 
   <td> <p>100 MB sind für die meisten Anwendungen ausreichend. </p> </td> 
   <td> <p>Kurzlebige Daten; kann für andere Quellbilder als PTIFF und bestimmte Antwortbildformate erforderlich sein. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Erforderlicher Speicherplatz für Quell-Images {#section-317da75099ad480d9a461c7e706d4f1c}

Adobe empfiehlt, alle Quellbilder mithilfe des Befehlszeilen-Tools Image Converter (IC) in das Pyramid TIFF-Dateiformat (PTIFF) zu konvertieren. Diese Konvertierung gewährleistet eine optimale Laufzeitleistung der Bildbereitstellung für alle Anwendungen. Der Bildserver kann zwar alle von IC akzeptierten Quelldateiformate verarbeiten, Dynamic Media unterstützt solche Verwendungszwecke jedoch nicht.

Wenn Sie PTIFF-Dateien verwenden, können die folgenden Faustregeln helfen, den Speicherplatzbedarf zu bestimmen.

*`total_space`* (Bytes) = *`number_of_images`* × (2000 + *`avg_pixel_count`* x *`avg_num_components`* × *`p_factor`*)

* *`avg_pixel_count`* Die durchschnittliche Pixelgröße (Breite x Höhe) aller Quellbilder im Original. Wenn die Originalbilder beispielsweise etwa 2K × 2K Pixel groß sind, wären dies 4 Megapixel.
* *`avg_num_components`* hängt vom Typ der Bilder ab. Für RGB-Images sind es 3, für CMYK- oder RGBA-Images 4. Verwenden Sie 3.5, wenn die Hälfte der Bilder RGB und die andere Hälfte RGBA sind.
* *`p_factor`* Abhängig vom Komprimierungstyp und der Qualitätseinstellung bei der Konvertierung der Bilder mit IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF-Kompression</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>unkomprimiert </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0,75, je nach Bild </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG-Komprimierung </p> </td> 
   <td> <p> 1 (typisch für JPEG Quality 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Annäherung berücksichtigt nicht den Dateisystem-Overhead. Der tatsächliche Speicherplatz auf der Disc kann wesentlich größer sein.

**Beispiel**

Bei einer Image-Serving-Bereitstellung wird erwartet, dass 30.000 ältere Bilder mit niedriger Auflösung mit einer durchschnittlichen Größe von 500 × 500 RGB-Pixel verwendet werden. Neue Bilddaten in Druckqualität werden mit einer Rate von 10.000 pro Jahr hinzugefügt. Die typische CMYK-Bildgröße beträgt 4K × 6K Byte. Alle Daten werden in JPEG in hoher Qualität komprimiert. Der gesamte Speicherplatz nach dreijähriger Nutzung wird wie folgt geschätzt:

*`total_space`* = 30.000 × (2 K + 0,5 K × 0,5 K × 3 × 0,1) + 3 × 10.000 × (2 K + 4 K × 6 K × 4 × 0,1) = 2,2 G + 268 GB = ca. 270 GB

Für eine garantierte beste Qualität kann eine Komprimierung wie z.B. ein Reißverschluss verwendet werden. Bei einer *`p_factor`* von 0,4 ist der insgesamt erforderliche Speicherplatz etwa viermal so groß. In diesem Fall etwas mehr als 1 Terabyte.
