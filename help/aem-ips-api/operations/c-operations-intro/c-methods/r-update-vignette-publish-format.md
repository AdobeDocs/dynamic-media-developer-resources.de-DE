---
description: Aktualisiert die Vignettenveröffentlichungsformateinstellungen.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 5%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

Aktualisiert die Vignettenveröffentlichungsformateinstellungen.

## Autorisierte Benutzertypen {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Eingabe (updateVignettePublishFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| vignetteFormatHandle | `xsd:string` | Ja | Publish-Formatgriff. |
| name | `xsd:string` | Nein | Publish-Formatname. |
| targetWidth | `xsd:int` | Ja | Gibt die Zielbreite der resultierenden Vignettenansicht in Pixel an. Verwenden Sie Null, damit die Ausgabe-Vignette dieselbe Größe wie die primäre Vignette hat. |
| targetHeight | `xsd:int` | Ja | Gibt die Zielhöhe der resultierenden Vignettenansicht in Pixel an. Verwenden Sie Null, damit die Ausgabe-Vignette dieselbe Größe wie die primäre Vignette hat. |
| createPyramid | `xsd:boolean` | Ja | Erstellt eine Pyramidenvignette, die für das Zoomen auf dem Bild-Rendering-Server optimiert ist. Beginnend mit der maximalen Größe, die durch die Felder Zielgröße der Vignette festgelegt wird, erstellt dies mehrere Größenansichten in einer einzigen Vignetten-Ausgabedatei. Jede darauffolgende Ansichtsgröße wird halbiert, bis die Breite und Höhe innerhalb von 128x128 Pixeln liegen. |
| thumbWidth | `xsd:int` | Ja | Gibt die Breite der einzelnen resultierenden Miniaturen in Pixel an. Diese Einstellung ist optional. Belassen Sie Null für keine Miniaturbilddatei. |
| saveAsVersion | `xsd:int` | Ja | Gibt das Dateiformat für die veröffentlichten Vignetten an. Bei einer neuen Version der Bildbearbeitung und einer älteren Version des Bild-Rendering-Servers müssen Sie eine Vignettenversion angeben, die Ihr Bild-Rendering-Server lesen kann. Wenn Sie eine höhere Version angeben, kann der Bild-Rendering-Server die veröffentlichten Vignetten nicht lesen. Auf null gesetzt, um Vignetten mit der neuesten Version zu veröffentlichen. |
| sizeSuffixSeparator | `xsd:string` | Ja | Gibt das Zeichen an, das den Namen der Vignette vom Suffix für die Breite trennt. |
| schärfen | `xsd:int` | Nein | Wendet für jede Veröffentlichungs-Vignettengröße eine Scharfzeichnung auf das Hauptansichtsbild an. Durch die Scharfzeichnung können Unschärfen ausgeglichen werden, wenn die Vignetten skaliert werden. |
| sumAmount | `xsd:double` | Ja | Die digitale Unschärfemaske ist eine flexible und leistungsstarke Methode, um die Schärfe zu erhöhen, insbesondere bei gescannten Bildern. Damit wird die Größe jeder Überschreitung festgelegt (wie viel dunkler und heller die Randkanten werden). |
| sumRadius | `xsd:double` | Ja | Beeinflusst die Größe der zu vergrößernden Kanten oder die Breite der Kantenränder, sodass ein kleinerer Radius die Detailgenauigkeit in kleinerem Maßstab verbessert. Höhere Radiuswerte können zu Lichthöfen an den Kanten führen. Feines Detail benötigt einen kleineren Radius, da winziges Detail der gleichen Größe oder kleiner als der Radius verloren geht. |
| Summenschwellenwert | `xsd:int` | Ja | Steuert die minimale Helligkeitsänderung, die geschärft werden soll, oder den Abstand benachbarter Farbwerte, bevor der Filter funktioniert. Diese Einstellung kann ausgeprägtere Kanten schärfen, während subtilere Kanten unberührt bleiben. Der zulässige Schwellenwert liegt zwischen 0 und 255. |

**Ausgabe (updateVignettePublishFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Ja | Verarbeiten Sie das aktualisierte Vignettenveröffentlichungsformat. |

## Beispiel {#section-fcba4bf2b7264786a676e315a35dbe43}

Dieses Codebeispiel aktualisiert ein Vignettenveröffentlichungsformat und gibt den Ziehgriff auf das aktualisierte Format zurück.

**Anfrage**

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
