---
description: Konfigurationsattribute werden als Attribute direkt in einem IMG-Element definiert, das von der responsiven Bildbibliothek verwaltet wird. Jedes Bild kann über eigene Attribute verfügen.
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Konfigurationsattribute werden als Attribute direkt in einem IMG-Element definiert, das von der responsiven Bildbibliothek verwaltet wird. Jedes Bild kann über eigene Attribute verfügen.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Optional.

URL zum Bild, das von Image Serving bereitgestellt wird. Wenn die URL nicht vorhanden ist, verwendet die Bibliothek den Wert, der in `src` Attribut als Fallback festgelegt ist. Dieses Attribut stellt das Ausgangsbild und das dynamische Bild bereit, die die Bibliothek Responsive Bilder von verschiedenen Orten aus verwaltet.

**Beispiel**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Wenn `data-src` festgelegt ist, ist `src` optional und kann jede URL enthalten, die Sie hinzufügen möchten. Beispielsweise kann sie eine URL zu demselben Image-Serving-basierten Bild enthalten, das die Bibliothek verwendet. Sie kann auch einen GIF-Platzhalter oder sogar einen Daten-URI enthalten, um einen zusätzlichen Server-Roundtrip beim Start zu vermeiden.

Wenn `data-src` nicht festgelegt ist, ist `src` obligatorisch und muss eine URL zu dem Bild enthalten, das von Image Serving bereitgestellt wird.

**Beispiel**

Verwenden des Daten-URI für das `src` und der Image-Serving-URL für das `data-src`:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Eine kommagetrennte Liste von Haltepunkten, denen optional ein Doppelpunkt ( `:`) sowie Bildbereitstellungsbefehle oder Bildvorgaben folgen. Jeder Haltepunkt ist ein Wert für die Bildbreite, der in logischen CSS-Pixeln definiert ist. Die -Bibliothek lädt das Bild mit dem größten Wert aus der Liste und skaliert es auf dem Client herunter, um es an die CSS-Bildbreite zur Laufzeit anzupassen. (Wenn Sie mit einem Bildschirm mit hoher Dichte arbeiten, stellen die vom Server geladenen Bildausgabedarstellungen Breakpoint-Werte dar, die mit dem Pixelverhältnis des Geräts multipliziert werden.)

Für jeden Haltepunkt aus der Liste können Sie einen oder mehrere Bildbereitstellungsbefehle oder Bildvorgabennamen definieren. Diese zusätzlichen Parameter werden nur dann auf das Bild angewendet, wenn dieser bestimmte Haltepunkt derzeit aktiv ist.

Sie können jeden unterstützten Bildbereitstellungsbefehl verwenden, mit Ausnahme der Ansichtsbefehle, die die Größe des Antwortbildes beeinflussen, z. B. `wid=`, `hei=` oder `scl=`. Dieselbe Einschränkung gilt für Bildvorgaben: Eine mit der responsiven Bildbibliothek verwendete Bildvorgabe darf solche Befehle nicht enthalten.

Mehrere Bildbereitstellungsbefehle oder Bildvorgabennamen werden durch das Zeichen &quot;`&`&quot; getrennt. Wenn ein Bildbereitstellungsbefehl ein Komma in seinem Wert enthält, wird dieses Komma durch `%2C` ersetzt. Namen von Bildvorgaben sind in Dollarzeichen ( `$`) eingeschlossen.

**Beispiele**

**Nur Haltepunkte verwenden**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Verwenden von Image-Serving-Befehlen**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Verwenden von Bildvorgaben**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Verwenden von Bildvorgaben und Bildbereitstellungsbefehlen**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Die folgenden beiden Modi für smartes Zuschneiden sind in AEM 6.4 und höher und Dynamic Media Viewer 5.9 und höher verfügbar:

* **Manuell** - Benutzerdefinierte Haltepunkte und entsprechende Bilddienstbefehle werden in einem -Attribut im Bildelement definiert.
* **Smartes Zuschneiden** - Berechnete Ausgabedarstellungen für smartes Zuschneiden werden automatisch vom Versandserver abgerufen. Die beste Ausgabedarstellung wird anhand der Laufzeitgröße des Bildelements ausgewählt.

Um den Modus für smartes Zuschneiden zu verwenden, setzen Sie das `data-mode` auf `smart crop`.

**Beispiel**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Das zugehörige Bildelement sendet zur Laufzeit ein `s7responsiveViewer`-Ereignis, wenn sich der Breakpoint ändert.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
