---
title: UnCompressOptions
description: Upload-Einstellung zur Verarbeitung von ZIP- und TAR-Dateien als primäre Assets (Keine) oder zum Extrahieren und Hochladen ihrer Inhalte (UnCompress).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# [!DNL UnCompressOptions]{#uncompressoptions}

Upload-Einstellung zur Verarbeitung von ZIP- und TAR-Dateien als primäre Assets (Keine) oder zum Extrahieren und Hochladen ihrer Inhalte (UnCompress).

>[!NOTE]
>
>Die Einstellung &quot;`None`&quot; ist die Standardeinstellung.

## Parameter {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> process</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Steuert die Verarbeitung von ZIP- und TAR-Archivdateien. Es bietet zwei Optionen: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> None:</span> Verarbeiten Sie als primäre Assets. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> UnCompress:</span> Extrahieren und verarbeiten Sie den Inhalt. </li>
     </ul><p>Hinweis: Bei Zeichenfolgenkonstanten wird zwischen Groß- und Kleinschreibung unterschieden. Verwenden Sie <span class="codeph"> UnCompress</span>, nicht <span class="codeph"> uncompress</span> oder <span class="codeph"> unCompress</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Verwendet von {#section-b2a829cf5511412e968bb2000f85cc31}

Der Typ `unCompressionOptions` wird wie folgt verwendet:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
