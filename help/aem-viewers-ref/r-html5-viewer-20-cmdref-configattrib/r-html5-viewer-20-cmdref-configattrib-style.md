---
description: style
solution: Experience Manager
title: style
feature: Dynamic Media Classic,Viewer,SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 7%

---


# style{#style}

Sie können den folgenden Befehl sowohl aus der URL-Abfrage als auch aus der Konfiguration anwenden. Der in der URL-Abfrage verwendete Befehl hat immer Vorrang vor dem in config vorhandenen Befehl.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Relativer oder absoluter CSS-Speicherort. </p> <p>Gibt den Speicherort der benutzerdefinierten CSS-Datei an. Wenn der Parameter <span class="codeph"><span class="varname"> cssPath</span></span> relativ ist, wird er für den HTML-Speicherort der Viewer-Seite und den Wert des Parameters <span class="codeph"> contentUrl=</span> aufgelöst. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle Asset-Verweise in der CSS-Datei werden mit dem Speicherort der CSS-Datei und nicht mit dem Speicherort der aufrufenden HTML-Seite aufgelöst.

## Eigenschaften {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Optional.

## Standard {#section-79a827f7a3bb4f36b3d72c309155059e}

Keine.

## Beispiele {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
