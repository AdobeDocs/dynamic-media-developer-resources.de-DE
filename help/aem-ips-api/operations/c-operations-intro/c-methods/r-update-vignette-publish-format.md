---
description: Aktualisiert die Einstellungen für das Vignettenveröffentlichungsformat.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '439'
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

**Eingabe (updateVignettePublishFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handle des Unternehmens. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Ja | Handle für das Veröffentlichungsformat. |
| `*`name`*` | `xsd:string` | Nein | Name des Veröffentlichungsformats. |
| `*`targetWidth`*` | `xsd:int` | Ja | Gibt die Zielbreite der resultierenden Vignettenansicht in Pixel an. Verwenden Sie null, damit die Ausgabemignette dieselbe Größe wie die primäre Vignette hat. |
| `*`targetHeight`*` | `xsd:int` | Ja | Gibt die Zielhöhe der resultierenden Vignettenansicht in Pixel an. Verwenden Sie null, damit die Ausgabemignette dieselbe Größe wie die primäre Vignette hat. |
| `*`createPyramid`*` | `xsd:boolean` | Ja | Erstellt eine zum Zoomen auf dem Image Rendering-Server optimierte Pryramidenvignette. Ausgehend von der Maximalgröße, die in den Feldern zur Bestimmung der Größe der Zielvignette festgelegt wird, werden in einer einzigen Vignettendatei Ansichten in verschiedenen Größen erstellt. Die Größe jeder weiteren Ansicht wird jedesmal halbiert, bis Höhe und Breite bei 128 x 128 Pixeln liegen. |
| `*`thumbWidth`*` | `xsd:int` | Ja | Gibt die Breite jeder resultierenden Miniaturansicht in Pixel an. Diese Einstellung ist optional. Lassen Sie den Wert null für keine Miniaturansicht-Datei. |
| `*`saveAsVersion`*` | `xsd:int` | Ja | Gibt das Dateiformat für die veröffentlichten Vignetten an. Bei einer neuen Version von Image Authoring und einer älteren Version des Image Rendering Server müssen Sie eine Vignettenversion angeben, die Ihr ImageRendering Server lesen kann. Wenn Sie eine höhere Version angeben, kann der Image Rendering-Server die veröffentlichten Vignetten nicht lesen. Auf null setzen, um Vignetten in der neuesten Version zu veröffentlichen. |
| `*`sizeSuffixSeparator`*` | `xsd:string` | Ja | Gibt an, durch welches Zeichen der Name der Vignette und das Suffix, das seine Größe angibt, getrennt werden sollen. |
| `*`Scharfzeichnen`*` | `xsd:int` | Nein | Wendet die Scharfzeichnung auf das Hauptansichtsbild für jede Veröffentlichungsvignettengröße an. Durch Scharfzeichnen können bei Skalierung der Vignetten verschwommene Stellen kompensiert werden. |
| `*`usmAmount`*` | `xsd:double` | Ja | Die digitale Unschärfemaske ist eine flexible und leistungsstarke Methode, um die Schärfe zu erhöhen, insbesondere bei gescannten Bildern. Dies steuert die Größe jedes Überschießens (wie viel dunkler und heller die Kantengrenzen werden). |
| `*`usmRadius`*` | `xsd:double` | Ja | Betrifft die Größe der zu verbessernden Kanten oder die Breite der Kantenrimen, sodass ein kleinerer Radius die Detailgenauigkeit vergrößert. Höhere Radiuswerte können Halos an den Kanten verursachen. Für feine Details ist ein kleinerer Radius erforderlich, da winzige Details derselben Größe oder kleiner als der Radius verloren gehen. |
| `*`usmThreshold`*` | `xsd:int` | Ja | Steuert die minimale Helligkeitsänderung, die scharfgezeichnet werden soll, oder die Entfernung zwischen benachbarten Tonwerten, bevor der Filter funktioniert. Mit dieser Einstellung können ausgeprägtere Kanten scharfgezeichnet werden, während feinere Kanten unberührt bleiben. Der zulässige Schwellenwert beträgt 0 bis 255. |

**Ausgabe (updateVignettePublishFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Ja | Zum aktualisierten Vignetten-Veröffentlichungsformat wechseln. |

## Beispiel {#section-fcba4bf2b7264786a676e315a35dbe43}

Dieses Codebeispiel aktualisiert ein Vignetten-Veröffentlichungsformat und gibt den Handle in das aktualisierte Format zurück.

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
