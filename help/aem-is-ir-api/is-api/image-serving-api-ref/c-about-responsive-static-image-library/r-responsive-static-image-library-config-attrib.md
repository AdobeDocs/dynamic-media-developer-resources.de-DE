---
description: Konfigurationsattribute werden als Attribute direkt auf einem IMG-Element definiert, das von der Bibliothek "Responsives Bild"verwaltet wird. Jedes Bild kann über einen eigenen Satz von Attributen verfügen.
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Konfigurationsattribute werden als Attribute direkt auf einem IMG-Element definiert, das von der Bibliothek &quot;Responsives Bild&quot;verwaltet wird. Jedes Bild kann über einen eigenen Satz von Attributen verfügen.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Optional.

URL zum Bild, das von Image Serving bereitgestellt wird. Wenn die URL nicht vorhanden ist, verwendet die Bibliothek den Wert, der in `src` -Attribut als Fallback. Dieses Attribut stellt das Anfangsbild und das dynamische Bild bereit, das von der Bibliothek für responsives Bild von verschiedenen Orten aus verwaltet wird.

**Beispiel**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Wenn `data-src` festgelegt ist, `src` ist optional und kann jede URL enthalten, die Sie hinzufügen möchten. Beispielsweise kann es eine URL zum selben Bild enthalten, das auf Image Serving basiert und von der Bibliothek verwendet wird. Oder sie kann einen GIF-Platzhalter oder sogar einen Daten-URI enthalten, um einen zusätzlichen Server-Round-Trip beim Start zu vermeiden.

Wenn `data-src` nicht festgelegt ist, `src` ist obligatorisch und muss eine URL zum Bild enthalten, das von Image Serving bereitgestellt wird.

**Beispiel**

Verwenden des Daten-URI für `src` -Attribut und Image Serving-URL für `data-src` Attribut:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## Datenhaltepunkte {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Eine kommagetrennte Liste von Haltepunkten, optional gefolgt von einem Doppelpunkt ( `:`) und Image Serving-Befehle oder Bildvorgaben. Jeder Breakpoint ist ein Bildbreitenwert, der in logischen CSS-Pixeln definiert ist. Die Bibliothek lädt das Bild mit dem nächstgrößeren Wert aus der Liste und lädt es auf den Client herunter, um es der CSS-Bildbreite der Laufzeitumgebung anzupassen. (Wenn Sie auf einem Bildschirm mit hoher Dichte arbeiten, stellen die vom Server geladenen Bildausgabeformate Breakpoint-Werte dar, multipliziert mit dem Pixelverhältnis des Geräts.)

Für jeden Haltepunkt aus der Liste ist es möglich, einen oder mehrere Image Serving-Befehle oder Bildvorgabennamen zu definieren. Solche zusätzlichen Parameter werden nur auf das Bild angewendet, wenn dieser bestimmte Breakpoint aktuell aktiv ist.

Sie können jeden unterstützten Image Serving-Befehl verwenden, mit Ausnahme der Ansichtsbefehle, die sich auf die Größe des Antwortbilds auswirken, z. B. `wid=`, `hei=`oder `scl=`. Dasselbe gilt für Bildvorgaben: Eine Bildvorgabe, die mit der responsiven Bildbibliothek verwendet wird, darf solche Befehle nicht enthalten.

Mehrere Image Serving-Befehle oder Bildvorgabennamen werden durch &quot;&quot;getrennt. `&`&quot;. Wenn ein Image Serving-Befehl ein Komma in seinem Wert hat, wird dieses Komma durch `%2C`. Namen von Bildvorgaben werden in Dollarzeichen ( `$`).

**Beispiele**

**Nur Haltepunkte verwenden**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Verwenden von Image Serving-Befehlen**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Verwenden von Bildvorgaben**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Verwenden von Bildvorgaben und Image Serving-Befehlen**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Die folgenden beiden smarten Zuschneidemodi sind in AEM 6.4 und höher sowie in Dynamic Media Viewers 5.9 und höher verfügbar:

* **Manuell** - Benutzerdefinierte Haltepunkte und entsprechende Image Service-Befehle werden innerhalb eines Attributs im Bildelement definiert.
* **Smartes Zuschneiden** - Berechnete Ausgabedarstellungen für smartes Zuschneiden werden automatisch vom Bereitstellungsserver abgerufen. Die beste Ausgabedarstellung wird mithilfe der Laufzeitgröße des Bildelements ausgewählt.

Um den Modus Smartes Zuschneiden zu verwenden, legen Sie die `data-mode` Attribut `smart crop`.

**Beispiel**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Das zugehörige Bildelement sendet einen `s7responsiveViewer` -Ereignis während der Laufzeit, wenn sich der Breakpoint ändert.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
