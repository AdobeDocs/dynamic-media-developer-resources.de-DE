---
description: Generiert ein Miniaturbild für Ihr Video.
seo-description: Generiert ein Miniaturbild für Ihr Video.
seo-title: MediaOptions
solution: Experience Manager
title: MediaOptions
topic: Scene7 Image Production System API
uuid: 4de59678-1bef-484c-9a43-ded531537aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MediaOptions{#mediaoptions}

Generiert ein Miniaturbild für Ihr Video.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:HandleArray</span> </td> 
   <td colname="col3">Ein Array von <span class="codeph"> Eigenschaftensätzen</span> behandelt das Verweisen auf Videokodierungsvorgaben zum Transkodieren von Videos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateMiniaturansicht</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Wenn "true", wird der erste Frame des Videos extrahiert und als Miniaturbild verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ThumbnailOptions</span> </td> 
   <td colname="col3">Optional. Ermöglicht die Auswahl eines bestimmten Videobilds, das als Miniaturbild verwendet werden soll. <p>Wenn Sie ein Miniaturbild angeben möchten, geben Sie die Zeit (in Millisekunden nach dem Beginn) für den zu verwendenden Frame ein. Die Werte reichen von 0 bis zum Ende des Videos. <p>Hinweis: Wenn Sie die Uhrzeit falsch angeben, <span class="codeph"> ist "Miniaturansicht</span> "standardmäßig auf "true"eingestellt. </p></p><p>Siehe <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> Miniaturoptionen</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## Verwendet von {#section-87cb83407198432c95eaa2db9f12f9db}

Der `mediaOptions` Typ wird verwendet von:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

