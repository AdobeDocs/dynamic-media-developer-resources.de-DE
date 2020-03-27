---
description: Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des gerade wiedergegebenen Videos anzeigt.
seo-description: Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des gerade wiedergegebenen Videos anzeigt.
seo-title: Videozeit
solution: Experience Manager
title: Videozeit
topic: Dynamic media
uuid: f8ba615f-661a-4750-bdf7-559650d464af
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video time{#video-time}

Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des gerade wiedergegebenen Videos anzeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Schriftfamilie, Schriftgröße und Schriftfarbe für die Videozeit gehören zu den Eigenschaften, die CSS steuern kann. Sie kann auch relativ zur Steuerleiste, in der sie enthalten ist, mithilfe von CSS positioniert werden.

Das Erscheinungsbild der Videozeit wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer .s7videotime
```

## CSS-Eigenschaften der Videozeit {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Videozeitsteuerung. Diese Eigenschaft ist erforderlich, damit Internet Explorer 8 oder höher ordnungsgemäß funktioniert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfamilie, die für die Zeitanzeige verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftgröße, die für die Zeitanzeige verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfarbe, die für die Zeitanzeige verwendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** `#BBBBBB`: Legen Sie die Videozeit auf hellgrau (hexadezimal) fest, wobei die Größe bei 12 Pixeln liegt, 15 Pixel von oben in der Steuerleiste und 80 Pixel von der oberen und rechten Kante der Steuerleiste entfernt.

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

