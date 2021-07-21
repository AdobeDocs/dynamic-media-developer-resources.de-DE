---
description: Einstellungen zur Verbesserung der Bildschärfe für optimierte Pyramid TIF-Dateien.
solution: Experience Manager
title: UnsharpMaskOptions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 7150b4a8-a44d-4858-96f2-6004d5f48e77
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 10%

---

# UnsharpMaskOptions{#unsharpmaskoptions}

Einstellungen zur Verbesserung der Bildschärfe für optimierte Pyramid TIF-Dateien.

`unsharpMaskOptions=[ *`Stärke, Radius, Schwellenwert, Monochrom`*]`

## Parameter {#section-c3f0d03136ba4422819cb463bd393885}

Geben Sie einen Wert für `unsharpMaskOptions`-Optionen mit `minOccurs=" *`n`*".` an.

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
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Steuert den auf Kantenpixel angewendeten Kontrast. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Bereich: 0.0-5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Standard: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> radius</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Steuert die Schärfe, indem die Anzahl der Pixel um den Rand eines Bildes festgelegt wird. Der richtige Wert hängt von der Größe des Bilds ab. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Bereich: 0.0-250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Bei niedrigen Werten werden nur Kantenpixel scharfgezeichnet. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Hohe Werte schärfen einen größeren Bereich von Pixeln. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> Schwellenwert</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Legt fest, wie sich verschiedene Pixel vom Umgebungsbereich unterscheiden müssen, bevor sie als Kantenpixel betrachtet werden und scharfgezeichnet werden können. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Bereich: 0 - 255 (nur Ganzzahlen). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Standard: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monochrome</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Die Werte umfassen nur <span class="codeph"> 0</span> oder <span class="codeph"> 1</span>. </p><p>Auf <span class="codeph"> 0</span> setzen, um auf jede Farbkomponente separat anzuwenden, oder auf <span class="codeph"> 1</span> , um nur auf die Bildhelligkeit (Intensität) anzuwenden. Die Ebenenmaske oder die zusammengesetzte Maske wird ebenfalls scharfgezeichnet. </p><p><span class="codeph"><span class="varname"> </span></span> Monochromeien werden bei Graustufenbildern ignoriert. </p></td>
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

Der Typ `unsharpMaskOptions` wird wie folgt verwendet:

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Image Serving-API-Referenz: op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)

