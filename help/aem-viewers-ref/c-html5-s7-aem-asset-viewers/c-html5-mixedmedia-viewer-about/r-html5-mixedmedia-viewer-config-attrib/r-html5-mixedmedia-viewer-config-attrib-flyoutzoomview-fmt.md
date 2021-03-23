---
description: Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.
seo-description: Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
feature: Dynamic Media Classic,Viewer,SDK/API,Mix-Mediensets
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. </p> <p>Beachten Sie, dass die Komponente standardmäßig einen weißen Hintergrund hat. Um ihn vollständig transparent zu machen, setzen Sie die CSS-Eigenschaft <span class="codeph"> background-color</span> auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
