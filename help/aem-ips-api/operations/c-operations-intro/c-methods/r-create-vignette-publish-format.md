---
description: Erstellt ein neues Veröffentlichungsformat für eine Vignette.
seo-description: Erstellt ein neues Veröffentlichungsformat für eine Vignette.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Dynamic Media Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

Erstellt ein neues Veröffentlichungsformat für eine Vignette.

Vignettenformate geben die Größe veröffentlichter Vignetten und deren Miniaturansichten sowie Zoomstufen, Scharfzeichnungsparameter und die Dateiformatversion für Vignetten an, die aus primären Vignetten erstellt wurden, die auf einem Image Rendering-Server vom IPS veröffentlicht wurden.

Neuere Image Rendering-Serverversionen unterstützen Pyramidenvignetten, sodass keine spezifischen Vignettenformatgrößen für die Veröffentlichung definiert werden müssen.

## Autorisierte Benutzertypen {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Input (createVignettePublishFormatParam)**

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
   <td colname="col4"> Handle zur Firma, zu der die Vignette gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Name zur Identifizierung des Vignettenveröffentlichungsformats. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Gibt die Zielgruppe der resultierenden Vignettenbreite in Pixel an. </p> <p>Verwenden Sie Null, damit die Ausgabevignette dieselbe Größe hat wie die primäre Vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Erstellt eine zum Zoomen auf dem Image Rendering-Server optimierte Pryramidenvignette. Ausgehend von der Maximalgröße, die in den Feldern zur Bestimmung der Größe der Zielvignette festgelegt wird, werden in einer einzigen Vignettendatei Ansichten in verschiedenen Größen erstellt. Die Größe jeder weiteren Ansicht wird jedesmal halbiert, bis Höhe und Breite bei 128 x 128 Pixeln liegen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt die Breite der resultierenden Miniaturansichten in Pixel an. Diese Einstellung ist optional. Ohne Miniaturansicht als Null belassen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Dateiformat für die veröffentlichten Vignetten an. Bei einer neuen Version von Image Authoring und einer älteren Version des Image Rendering-Servers müssen Sie eine Vignettenversion angeben, die der ImageRendering-Server lesen kann. Wenn Sie eine höhere Version angeben, kann der Image Rendering-Server die veröffentlichten Vignetten nicht lesen. Auf null setzen, um Vignetten mit der neuesten Version zu veröffentlichen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Zeichen an, durch das der Vignettenname und das Suffix mit der Breite getrennt werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Zeichen an, durch das der Vignettenname und das Suffix mit der Breite getrennt werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> scharfzeichnen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Wendet das Scharfzeichnen auf das Hauptbild der Ansicht für jede veröffentlichte Vignettengröße an. Das Scharfzeichnen kann die Weichzeichnung kompensieren, wenn die Vignetten skaliert werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Die digitale Unschärfemaske ist eine flexible und leistungsstarke Methode, um die Schärfe zu erhöhen, besonders bei gescannten Bildern. Dadurch wird die Größenordnung jedes Überschießens gesteuert (je dunkler und hell die Kantengrenzen werden). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Beeinflusst die Größe der zu verbessernden Kanten oder die Breite der Kantenfelge, sodass ein kleineres Radium die Detailgenauigkeit der Skalierung verbessert. Höhere Radiuswerte können Halos an den Kanten verursachen. Die feinen Details benötigen einen kleineren Radius, da winzige Details derselben Größe oder kleiner als der Radius verloren gehen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codebegriff  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Steuert die minimale Helligkeitsänderung, die scharfgezeichnet werden soll, oder wie weit die angrenzenden Tonwerte voneinander entfernt sein müssen, bevor der Filter funktioniert. Durch diese Einstellung können ausgeprägtere Kanten scharfgezeichnet werden, während subtilere Kanten unberührt bleiben. Der zulässige Bereich von 0 bis 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignettePublishFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Ja | Der Griff zum erstellten Vignettenformat. |

## Beispiele {#section-0564752d439642b9bb8de2903db6de1e}

Dieser Code erstellt das Vignettenveröffentlichungsformat. Die Erstellungsanforderung gibt einen Namen, eine Breite und Höhe der Zielgruppe sowie andere erforderliche Werte an.

**Anforderung**

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

