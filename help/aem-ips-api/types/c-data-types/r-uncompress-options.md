---
title: UncompressOptions
description: Upload-Einstellung für die Verarbeitung von ZIP- und TAR-Dateien als primäre Assets (keine) oder für die Extraktion und den Upload ihrer Inhalte (Uncompress).
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

Upload-Einstellung für die Verarbeitung von ZIP- und TAR-Dateien als primäre Assets (keine) oder für die Extraktion und den Upload ihrer Inhalte (Uncompress).

>[!NOTE]
>
>Die Einstellung `None` ist die Standardeinstellung.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> Prozess</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Steuert die ZIP- und TAR-Archivdateiverarbeitung. Es stehen zwei Optionen zur Verfügung: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB">Keine <span class="codeph">: </span> als primäre Assets verarbeiten. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> UnCompress</span> Extrahieren und Verarbeiten des Inhalts. </li>
     </ul><p>Hinweis: Bei Zeichenfolgenkonstanten wird zwischen Groß- und Kleinschreibung unterschieden. Verwenden Sie <span class="codeph"> Uncompress</span>, nicht <span class="codeph"> Uncompress</span>, oder <span class="codeph"> uncompress</span>. </p></p> </td> 
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

Der `unCompressionOptions` wird verwendet von:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
