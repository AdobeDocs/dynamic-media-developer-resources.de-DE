---
description: Erstellt ein neues Veröffentlichungsformat für eine Vignette.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 14%

---

# createVignettePublishFormat{#createvignettepublishformat}

Erstellt ein neues Veröffentlichungsformat für eine Vignette.

Vignettenformate geben die Größe veröffentlichter Vignetten und deren Miniaturansichten sowie Zoomstufen, Scharfzeichnungsparameter und die Dateiformatversion für Vignetten an, die aus primären Vignetten erzeugt werden, die von IPS auf einem Image Rendering-Server veröffentlicht werden.

Neuere Image Rendering-Serverversionen unterstützen Pyramid-Vignetten, sodass keine spezifischen Vignettenformatgrößen für die Veröffentlichung definiert werden müssen.

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
   <td colname="col4"> Handle mit dem Unternehmen, zu dem die Vignette gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Name zur Identifizierung des Vignettenveröffentlichungsformats. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Gibt die Zielbreite der resultierenden Vignettenansicht in Pixel an. </p> <p>Verwenden Sie null, damit die Ausgabemignette dieselbe Größe wie die primäre Vignette hat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Erstellt eine zum Zoomen auf dem Image Rendering-Server optimierte Pryramidenvignette. Ausgehend von der Maximalgröße, die in den Feldern zur Bestimmung der Größe der Zielvignette festgelegt wird, werden in einer einzigen Vignettendatei Ansichten in verschiedenen Größen erstellt. Die Größe jeder weiteren Ansicht wird jedesmal halbiert, bis Höhe und Breite bei 128 x 128 Pixeln liegen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt die Breite jeder resultierenden Miniaturansicht in Pixel an. Diese Einstellung ist optional. Lassen Sie den Wert null für keine Miniaturansicht-Datei. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Dateiformat für die veröffentlichten Vignetten an. Bei einer neuen Version von Image Authoring und einer älteren Version des Image Rendering Server müssen Sie eine Vignettenversion angeben, die Ihr ImageRendering Server lesen kann. Wenn Sie eine höhere Version angeben, kann der Image Rendering-Server die veröffentlichten Vignetten nicht lesen. Auf null setzen, um Vignetten in der neuesten Version zu veröffentlichen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Zeichen an, das den Vignettennamen und das Suffix trennt und die Breite angibt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Gibt das Zeichen an, das den Vignettennamen und das Suffix trennt und die Breite angibt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Scharfzeichnen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Wendet die Scharfzeichnung auf das Hauptansichtsbild für jede Veröffentlichungsvignettengröße an. Das Scharfzeichnen kann die Weichzeichnung bei der Skalierung der Vignetten kompensieren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Die digitale Unschärfemaske ist eine flexible und leistungsstarke Methode, um die Schärfe zu erhöhen, insbesondere bei gescannten Bildern. Dies steuert die Größe jedes Überschießens (wie viel dunkler und leichter die Kantengrenzen werden). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Hat Auswirkungen auf die Größe der zu verbessernden Kanten oder die Breite der Kantenrimen, sodass ein kleineres Radium die Detailschärfe vergrößert. Höhere Radiuswerte können Halos an den Kanten verursachen. Für feine Details ist ein kleinerer Radius erforderlich, da winzige Details derselben Größe oder kleiner als der Radius verloren gehen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Codeausdruck  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Steuert die minimale Helligkeitsänderung, die scharfgezeichnet werden soll, oder die Entfernung zwischen benachbarten Tonwerten, bevor der Filter funktioniert. Mit dieser Einstellung können ausgeprägtere Kanten scharfgezeichnet werden, während feinere Kanten unberührt bleiben. Der zulässige Bereich von 0 bis 255. </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (createVignettePublishFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Ja | Der Griff zum erstellten Vignettenformat. |

## Beispiele {#section-0564752d439642b9bb8de2903db6de1e}

Dieser Code erstellt das Vignettenveröffentlichungsformat. Die Erstellungsanfrage gibt einen Namen, eine Zielbreite und -höhe sowie andere erforderliche Werte an.

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
