---
title: style
description: style
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
TQID: 'https://experienceleague.adobe.com/vkV2CfEEhJmPdQg64y0G-5Ep-T6SPd4tQX88CWbPryw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 7%

---

# style{#style}

Sie können den folgenden Befehl sowohl in der URL-Abfragezeichenfolge als auch in der Konfiguration anwenden. Der Befehl, der in der URL-Abfragezeichenfolge angewendet wird, hat immer Vorrang vor demselben Befehl, der in der Konfiguration vorhanden ist.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Relativer oder absoluter CSS-Speicherort. </p> <p>Gibt den Speicherort der benutzerdefinierten CSS-Datei an. Wenn der <span class="codeph"><span class="varname"> cssPath</span></span> relativ ist, wird er gegen den Seitenspeicherort des HTML-Viewers und den Wert <span class="codeph"> Parameters contentUrl=</span> aufgelöst. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle Asset-Verweise innerhalb der CSS-Datei werden gegen den Speicherort der CSS-Datei aufgelöst, nicht gegen den Speicherort der aufrufenden HTML-Seite.

## Eigenschaften {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Optional.

## Standard {#section-79a827f7a3bb4f36b3d72c309155059e}

Keine.

## Beispiele {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
