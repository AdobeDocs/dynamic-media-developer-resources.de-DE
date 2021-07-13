---
description: style
solution: Experience Manager
title: style
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 7%

---

# style{#style}

Sie können den folgenden Befehl sowohl in der URL-Abfragezeichenfolge als auch in der Konfiguration anwenden. Der in der URL-Abfragezeichenfolge angewendete Befehl hat immer Vorrang vor dem in config vorhandenen Befehl.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Relativer oder absoluter CSS-Speicherort. </p> <p>Gibt den Speicherort der benutzerdefinierten CSS-Datei an. Wenn der <span class="codeph"><span class="varname"> cssPath</span></span> relativ ist, wird er für den HTML-Seitenspeicherort des Viewers und den Wert des Parameters <span class="codeph"> contentUrl=</span> aufgelöst. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle Asset-Verweise in der CSS-Datei werden mit dem CSS-Dateispeicherort aufgelöst, nicht mit dem Speicherort der aufrufenden HTML-Seite.

## Eigenschaften {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Optional.

## Standard {#section-79a827f7a3bb4f36b3d72c309155059e}

Keine.

## Beispiele {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
