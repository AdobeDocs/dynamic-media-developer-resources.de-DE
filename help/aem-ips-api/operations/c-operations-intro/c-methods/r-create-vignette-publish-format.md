---
description: Erstellt ein neues Veröffentlichungsformat für eine Vignette.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 4%

---

# createVignettePublishFormat{#createvignettepublishformat}

Erstellt ein neues Veröffentlichungsformat für eine Vignette.

Vignettenformate geben die Größe veröffentlichter Vignetten und deren Miniaturansichten sowie Zoomstufen, Scharfzeichnungsparameter und die Dateiformatversion für Vignetten an, die aus primären Vignetten erstellt wurden, die auf einem Bild-Rendering-Server von IPS veröffentlicht wurden.

Neuere Image Rendering-Server-Versionen können Pyramidenvignetten unterstützen, sodass für die Veröffentlichung keine spezifischen Vignettenformatgrößen definiert werden müssen.

## Autorisierte Benutzertypen {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Eingabe (createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Erforderlich </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handle an die Firma, zu der die Vignette gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Name zur Identifizierung des Vignettenveröffentlichungsformats. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Gibt die Zielbreite der resultierenden Vignettenansicht in Pixel an. </p> <p>Verwenden Sie Null, damit die Ausgabe-Vignette dieselbe Größe wie die primäre Vignette hat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Erstellt eine Pyramidenvignette, die für das Zoomen auf dem Bild-Rendering-Server optimiert ist. Beginnend mit der maximalen Größe, die durch die Felder Zielgröße der Vignette festgelegt wird, erstellt dies mehrere Größenansichten in einer einzigen Vignetten-Ausgabedatei. Jede darauffolgende Ansichtsgröße wird halbiert, bis die Breite und Höhe innerhalb von 128x128 Pixeln liegen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt die Breite der einzelnen resultierenden Miniaturen in Pixel an. Diese Einstellung ist optional. Belassen Sie Null für keine Miniaturbilddatei. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Dateiformat für die veröffentlichten Vignetten an. Bei einer neuen Version der Bildbearbeitung und einer älteren Version des Bild-Rendering-Servers müssen Sie eine Vignettenversion angeben, die Ihr Bild-Rendering-Server lesen kann. Wenn Sie eine höhere Version angeben, kann der Bild-Rendering-Server die veröffentlichten Vignetten nicht lesen. Auf null gesetzt, um Vignetten mit der neuesten Version zu veröffentlichen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Zeichen an, das den Namen der Vignette vom Suffix für die Breite trennt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Zeichen an, das den Namen der Vignette vom Suffix für die Breite trennt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> schärfen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Wendet die Scharfzeichnung auf das Hauptansichtsbild für jede Veröffentlichungs-Vignettengröße an Scharfzeichnung kann Unschärfen ausgleichen, wenn die Vignetten skaliert werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Die digitale Unschärfemaske ist eine flexible und leistungsstarke Methode, um die Schärfe zu erhöhen, insbesondere bei gescannten Bildern. Damit wird die Größe der einzelnen Überschreitungen (wie viel dunkler und heller die Kantenränder werden) gesteuert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Beeinflusst die Größe der zu vergrößernden Kanten oder die Breite der Kantenränder, sodass ein kleineres Radium die Detailgenauigkeit in kleinerem Maßstab verbessert. Höhere Radiuswerte können zu Lichthöfen an den Kanten führen. Feines Detail benötigt einen kleineren Radius, da winziges Detail der gleichen Größe oder kleiner als der Radius verloren geht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code-Satz </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Steuert die minimale Helligkeitsänderung, die geschärft werden soll, oder den Abstand benachbarter Farbwerte, bevor der Filter funktioniert. Diese Einstellung kann ausgeprägtere Kanten schärfen, während subtilere Kanten unberührt bleiben. Der zulässige Schwellenwert liegt zwischen 0 und 255. </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (createVignettePublishFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Ja | Der Griff zum erstellten Vignettenformat. |

## Beispiele {#section-0564752d439642b9bb8de2903db6de1e}

Dieser Code erstellt das Vignettenveröffentlichungsformat. Die Erstellungsanfrage gibt einen Namen, eine Zielbreite und -höhe sowie andere erforderliche Werte an.

**Anfrage**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Antwort**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```
