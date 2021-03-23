---
description: Parameter, die allen Viewern gemein sind.
seo-description: Parameter, die allen Viewern gemein sind.
seo-title: config
solution: Experience Manager
title: config
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
feature: Dynamic Media Classic,Viewer,SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 3%

---


# config{#config}

Parameter, die allen Viewern gemein sind.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>Katalog/ID für die Viewer-Konfiguration. </p> <p> Gibt einen Bildkatalogeintrag an, der die Viewer-Konfigurationseigenschaften im Katalog <span class="codeph"> enthält::UserData </span>. Wenn dieser Befehl vorhanden ist, sendet der Viewer den Befehl <span class="codeph"> req=userdata </span> für <span class="codeph"> configId </span> an den Server und extrahiert Eigenschaften aus der Antwort. Die Eigenschaften werden zum Initialisieren des Viewers verwendet. Wenn die URL-Zeichenfolge dieselben Eigenschaften angibt, überschreiben sie die Werte aus dem Katalog <span class="codeph">::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle Viewer-Befehle, die in `catalog::UserData` angegeben werden können, erwarten `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` und `config` selbst.

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Keine.

## Beispiel 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Ein Bildkatalog mit dem Namen 2020 enthält den Eintrag `preset-oct`. Das Feld `catalog::UserData` dieses Katalogeintrags enthält die folgenden Daten:

```
style=customStyle.css
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=2020/preset-oct
```

Dies entspricht den folgenden Befehlen, die explizit in der URL angegeben werden:

```
style=customStyle.css
```

## Beispiel 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Ein Bildkatalog mit dem Namen 2019 enthält den Eintrag `spin-oct`. Das Feld `catalog::UserData` dieses Katalogeintrags enthält die folgenden Daten:

```
zoomStep=3 
maxZoom=200
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=2019/spin-oct
```

Dies entspricht den folgenden Befehlen, die explizit in der URL angegeben werden:

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

Dies entspricht den folgenden Befehlen, die explizit in der URL angegeben werden:

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

Dies entspricht den folgenden Befehlen, die explizit in der URL angegeben werden:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Beispiel 5 {#section-19b988551d1d492a9079948e0b04b38f}

Eine Viewer-Vorgabe mit dem Namen `Carousel_Dotted_light` der folgenden Daten:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Laden Sie den Viewer mit dem folgenden Befehl:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Dies entspricht den folgenden Befehlen, die explizit in der URL angegeben werden:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

