---
description: Einstellungen, die die Bildschärfe für optimierte Pyramidendateien verbessern.
seo-description: Einstellungen, die die Bildschärfe für optimierte Pyramidendateien verbessern.
seo-title: UnsharpMaskOptions
solution: Experience Manager
title: UnsharpMaskOptions
topic: Scene7 Image Production System API
uuid: 73073de0-41b6-471c-8887-f6b94ed2af90
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 10%

---


# UnsharpMaskOptions{#unsharpmaskoptions}

Einstellungen, die die Bildschärfe für optimierte Pyramidendateien verbessern.

`unsharpMaskOptions=[ *`Stärke, Radius, Schwellenwert, Monochrom`*]`

## Parameter {#section-c3f0d03136ba4422819cb463bd393885}

Geben Sie einen Wert für `unsharpMaskOptions`-Optionen mit `minOccurs=" *`n`*".` ein

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Name </th>
   <th colname="col2" class="entry"> Typ </th>
   <th colname="col3" class="entry"> Beschreibung </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> Betrag</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:Dublette</span></td>
   <td colname="col3"><p>Steuert den Kontrast, der auf Kantenpixel angewendet wird. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Bereich: 0,0-5,0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Standard: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> radius</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:Dublette</span></td>
   <td colname="col3"><p>Steuert die Schärfe, indem die Anzahl der Pixel um den Rand eines Bilds festgelegt wird. Der richtige Wert hängt von der Größe des Bilds ab. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Bereich: 0,0-250,0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Bei niedrigen Werten werden nur Kantenpixel scharfgezeichnet. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Bei hohen Werten wird ein breiterer Pixelbereich scharfgezeichnet. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> Schwellenwert</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Legt fest, wie stark sich die Pixel vom umgebenden Bereich unterscheiden müssen, bevor sie als Kantenpixel betrachtet werden und scharfgezeichnet werden können. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Bereich: 0 - 255 (nur Ganzzahlen). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Standard: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> Monochrom</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Zu den Werten gehören nur <span class="codeph"> 0</span> oder <span class="codeph"> 1</span>. </p><p>Auf <span class="codeph"> 0</span> setzen, um jede Farbkomponente separat anzuwenden, oder auf <span class="codeph"> 1</span>, um nur die Bildhelligkeit (Intensität) anzuwenden. Auch die Ebenenmaske oder die Composite-Maske wird scharfgezeichnet. </p><p><span class="codeph"><span class="varname"> Bei Graustufenbildern werden </span></span> Monochrome ignoriert. </p></td>
  </tr>
 </tbody>
</table>

## Beispiel {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Verwendet von {#section-db8124a5468b498694a780f8a56a4560}

Der Typ `unsharpMaskOptions` wird verwendet von:

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Image Serving API-Referenz: op_usm](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)

