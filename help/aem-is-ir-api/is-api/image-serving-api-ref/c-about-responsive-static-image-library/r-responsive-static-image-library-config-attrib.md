---
description: Konfigurationsattribute werden als Attribute direkt auf einem IMG-Element definiert, das von der Bibliothek für interaktives Bild verwaltet wird. Jedes Bild kann über einen eigenen Satz von Attributen verfügen.
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Konfigurationsattribute werden als Attribute direkt auf einem IMG-Element definiert, das von der Bibliothek für interaktives Bild verwaltet wird. Jedes Bild kann über einen eigenen Satz von Attributen verfügen.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Optional.

URL zu dem Bild, das Image Serving bereitstellt. Wenn die URL nicht vorhanden ist, verwendet die Bibliothek den Wert, der im Attribut `src` als Fallback festgelegt ist. Dieses Attribut gibt das Anfangsbild und das dynamische Bild an, das von der Bibliothek für interaktives Bild von verschiedenen Orten verwaltet wird.

**Beispiel**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Ist `data-src` eingestellt, ist `src` optional und kann jede URL enthalten, die Sie hinzufügen möchten. Sie kann beispielsweise eine URL zu demselben Image-Server-basierten Bild enthalten, das von der Bibliothek verwendet wird. Sie kann auch einen GIF-Platzhalter oder sogar einen Daten-URI enthalten, um einen zusätzlichen Server-Hin- und Rückflug beim Start zu vermeiden.

Ist `data-src` nicht eingestellt, ist `src` obligatorisch und muss eine URL zu dem Bild enthalten, das Image Serving bereitstellt.

**Beispiel**

Verwenden der Daten-URI für das `src`-Attribut und die Image-Server-URL für das `data-src`-Attribut:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-break-points {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Eine kommagetrennte Liste von Haltepunkten und optional gefolgt von einem Doppelpunkt ( `:`) und Bildserstellungs-Befehlen oder Bildvorgaben. Jeder Haltepunkt ist ein Wert für die Bildbreite, der in logischen CSS-Pixeln definiert wird. Die Bibliothek lädt das Bild mit dem nächstgrößeren Wert aus der Liste und lädt es auf den Client herunter, um es an die CSS-Bildbreite der Laufzeitumgebung anzupassen. (Wenn Sie auf einem hochauflösenden Bildschirm arbeiten, stellen Bilddarstellungen, die vom Server geladen werden, Haltepunktwerte dar, multipliziert mit dem Pixelverhältnis des Geräts.)

Für jeden Haltepunkt aus der Liste ist es möglich, einen oder mehrere Image Serving-Befehle oder Bildvorgabennamen zu definieren. Solche zusätzlichen Parameter werden nur auf das Bild angewendet, wenn dieser Haltepunkt aktuell aktiv ist.

Sie können jeden unterstützten Image Serving-Befehl verwenden, mit Ausnahme der Ansichten, die sich auf die Größe des Antwortbilds auswirken, wie `wid=`, `hei=` oder `scl=`. Dasselbe gilt für Bildvorgaben: Eine Bildvorgabe, die mit der interaktiven Bildbibliothek verwendet wird, darf solche Befehle nicht enthalten.

Mehrere Bildservierungsbefehle oder Bildvorgabennamen werden durch das Zeichen &quot;`&`&quot;getrennt. Wenn der Wert eines Image Serving-Befehls ein Komma enthält, wird dieses durch `%2C` ersetzt. Bildvorgabennamen werden in Dollarzeichen ( `$`) eingeschlossen.

**Beispiele**

**Nur Haltepunkte verwenden**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Verwenden von Bildserstellungs-Befehlen**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Verwenden von Bildvorgaben**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Verwenden der Befehle &quot;Bildvorgaben&quot;und &quot;Image Serving&quot;**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Die folgenden beiden Modi für das intelligente Beschneiden sind in AEM 6.4 und höher und in Dynamic Media Viewers 5.9 und höher verfügbar:

* **Manuell**  - benutzerdefinierte Haltepunkte und entsprechende Bilddienstbefehle werden innerhalb eines Attributs im Bildelement definiert.
* **Smart-Zuschneiden**  - berechnete Smart-Zuschneiden-Darstellungen werden automatisch vom Versand-Server abgerufen. Die beste Darstellung wird unter Verwendung der Laufzeitgröße des Bildelements ausgewählt.

Um den Smart-Zuschneidemodus zu verwenden, legen Sie das `data-mode`-Attribut auf `smart crop` fest.

**Beispiel**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Das zugehörige Bildelement löst während der Laufzeit ein `s7responsiveViewer`-Ereignis aus, wenn sich der Haltepunkt ändert.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```

