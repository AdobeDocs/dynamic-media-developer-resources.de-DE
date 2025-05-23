---
title: config
description: Für alle Viewer gemeinsamer Parameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 5%

---

# config{#config}

Für alle Viewer gemeinsamer Parameter.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span> </span> </p> </td> 
   <td colname="col2"> <p>Katalog/ID für die Viewer-Konfiguration. </p> <p> Gibt einen Bildkatalogeintrag an, der die Viewer-Konfigurationseigenschaften <span class="codeph"> Katalog::UserData-</span> enthält. Wenn dieser Befehl vorhanden ist, sendet der Viewer einen <span class="codeph"> Befehl req=userdata </span> für <span class="codeph"> configId-</span> an den Server und extrahiert Eigenschaften aus der Antwort. Die Eigenschaften werden zum Initialisieren des Viewers verwendet. Wenn die URL-Zeichenfolge dieselben Eigenschaften angibt, überschreiben sie die Werte aus <span class="codeph"> Catalog::UserData-</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle Viewer-Befehle, die in `catalog::UserData` angegeben werden können, erwarten `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` und `config` selbst.

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Keine.

## Beispiel 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Ein Bildkatalog mit dem Namen 2020 enthält die `preset-oct`. Das `catalog::UserData` Feld dieses Katalogeintrags enthält die folgenden Daten:

```
style=customStyle.css
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=2020/preset-oct
```

Dieses Beispiel entspricht dem folgenden Befehl, der explizit in der URL angegeben ist:

```
style=customStyle.css
```

## Beispiel 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Ein Bildkatalog mit dem Namen 2019 enthält die `spin-oct`. Das `catalog::UserData` Feld dieses Katalogeintrags enthält die folgenden Daten:

```
zoomStep=3 
maxZoom=200
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=2019/spin-oct
```

Dieses Beispiel entspricht dem folgenden Befehl, der explizit in der URL angegeben ist:

```
zoomStep=3&maxZoom=200
```

## Beispiel 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

Eine Viewer-Vorgabe mit dem Namen `Shoppable_Banner` enthält die folgenden Daten:

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

Dieses Beispiel entspricht den folgenden Befehlen, die explizit in der URL angegeben sind:

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Beispiel 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

Eine Viewer-Vorgabe mit dem Namen `Shoppable_Video_Dark` enthält die folgenden Daten:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

Dieses Beispiel entspricht den folgenden Befehlen, die explizit in der URL angegeben sind:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Beispiel 5 {#section-19b988551d1d492a9079948e0b04b38f}

Eine Viewer-Vorgabe mit dem Namen `Carousel_Dotted_light` die folgenden Daten:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Dieses Beispiel entspricht den folgenden Befehlen, die explizit in der URL angegeben sind:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
