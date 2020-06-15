---
description: Aktualisiert die Einstellungen für das Vignettenveröffentlichungsformat.
seo-description: Aktualisiert die Einstellungen für das Vignettenveröffentlichungsformat.
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---


# updateVignettePublishFormat{#updatevignettepublishformat}

Aktualisiert die Einstellungen für das Vignettenveröffentlichungsformat.

## Autorisierte Benutzertypen {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Input (updateVignettePublishFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Ja | Handle für das Veröffentlichungsformat. |
| ` *`name`*` | `xsd:string` | Nein | Name des Veröffentlichungsformats. |
| ` *`targetWidth`*` | `xsd:int` | Ja | Gibt die Zielgruppe der resultierenden Vignettenbreite in Pixel an. Verwenden Sie Null, damit die Ausgabevignette dieselbe Größe hat wie die primäre Vignette. |
| ` *`targetHeight`*` | `xsd:int` | Ja | Gibt die Zielgruppe der resultierenden Vignettenhöhe in Pixel an. Verwenden Sie Null, damit die Ausgabevignette dieselbe Größe hat wie die primäre Vignette. |
| ` *`createPyramid`*` | `xsd:boolean` | Ja | Erstellt eine zum Zoomen auf dem Image Rendering-Server optimierte Pryramidenvignette. Ausgehend von der Maximalgröße, die in den Feldern zur Bestimmung der Größe der Zielvignette festgelegt wird, werden in einer einzigen Vignettendatei Ansichten in verschiedenen Größen erstellt. Die Größe jeder weiteren Ansicht wird jedesmal halbiert, bis Höhe und Breite bei 128 x 128 Pixeln liegen. |
| ` *`thumbWidth`*` | `xsd:int` | Ja | Gibt die Breite der resultierenden Miniaturansichten in Pixel an. Diese Einstellung ist optional. Ohne Miniaturansicht als Null belassen. |
| ` *`saveAsVersion`*` | `xsd:int` | Ja | Gibt das Dateiformat für die veröffentlichten Vignetten an. Bei einer neuen Version von Image Authoring und einer älteren Version des Image Rendering-Servers müssen Sie eine Vignettenversion angeben, die der ImageRendering-Server lesen kann. Wenn Sie eine höhere Version angeben, kann der Image Rendering-Server die veröffentlichten Vignetten nicht lesen. Auf null setzen, um Vignetten mit der neuesten Version zu veröffentlichen. |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | Ja | Gibt an, durch welches Zeichen der Name der Vignette und das Suffix, das seine Größe angibt, getrennt werden sollen. |
| ` *`scharfzeichnen`*` | `xsd:int` | Nein | Wendet Scharfzeichnen auf das Hauptbild der Ansicht für jede Vignettengröße im Veröffentlichungsmodus an. Durch Scharfzeichnen kann die Weichzeichnung kompensiert werden, wenn die Vignetten skaliert werden. |
| ` *`usmAmount`*` | `xsd:double` | Ja | Die digitale Unschärfemaske ist eine flexible und leistungsstarke Methode, um die Schärfe zu erhöhen, besonders bei gescannten Bildern. Dadurch wird die Größenordnung jedes Überlaufs gesteuert (je dunkler und leichter die Kantengrenzen werden). |
| ` *`usmRadius`*` | `xsd:double` | Ja | Beeinflusst die Größe der zu verbessernden Kanten oder die Breite der Kantenfelge, sodass ein kleinerer Radius die Details vergrößert. Höhere Radiuswerte können Halos an den Kanten verursachen. Die feinen Details benötigen einen kleineren Radius, da winzige Details derselben Größe oder kleiner als der Radius verloren gehen. |
| ` *`usmThreshold`*` | `xsd:int` | Ja | Steuert die minimale Helligkeitsänderung, die scharfgezeichnet werden soll, oder wie weit die angrenzenden Tonwerte voneinander entfernt sein müssen, bevor der Filter funktioniert. Durch diese Einstellung können ausgeprägtere Kanten scharfgezeichnet werden, während subtilere Kanten unberührt bleiben. Der zulässige Bereich von Schwellenwert ist 0 bis 255. |

**Output (updateVignettePublishFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Ja | Bearbeiten Sie das aktualisierte Vignettenveröffentlichungsformat. |

## Beispiel {#section-fcba4bf2b7264786a676e315a35dbe43}

Dieses Codebeispiel aktualisiert ein Vignettenveröffentlichungsformat und gibt den Handle in das aktualisierte Format zurück.

**Anforderung**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Antwort**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```

