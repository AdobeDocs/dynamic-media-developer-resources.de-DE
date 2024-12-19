---
description: Generiert ein Miniaturbild für Ihr Video.
solution: Experience Manager
title: Medienoptionen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f37d935d-fe74-4878-8477-d2144d58d982
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# [!DNL MediaOptions]{#mediaoptions}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:HandleArray</span> </td> 
   <td colname="col3">Ein Array von <span class="codeph"> PropertySet</span> behandelt Verweise auf Videokodierungsvorgaben zum Transkodieren von Videos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Wenn „true“, wird das erste Einzelbild des Videos extrahiert und als Miniaturbild verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:ThumbnailOptions</span> </td> 
   <td colname="col3">Optional. Ermöglicht die Auswahl eines bestimmten Videoframes, der als Miniaturbild verwendet werden soll. <p>Um ein Miniaturbild anzugeben, übergeben Sie die Zeit (in Millisekunden ab Videostart) für den gewünschten Frame. Die Werte reichen von 0 bis zum Ende des Videos. <p>Hinweis: Wenn Sie die Zeit falsch angeben, wird für <span class="codeph"> GenerateThumbnail </span> true festgelegt. </p></p><p>Siehe <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> ThumbnailOptions</a>. </p></td> 
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

Der `mediaOptions` wird verwendet von:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
