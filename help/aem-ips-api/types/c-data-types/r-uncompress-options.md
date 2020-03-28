---
description: Upload-Einstellung zur Verarbeitung von ZIP- und TAR-Dateien als Master-Assets (Keine) oder zum Extrahieren und Hochladen ihrer Inhalte (UnCompress).
seo-description: Upload-Einstellung zur Verarbeitung von ZIP- und TAR-Dateien als Master-Assets (Keine) oder zum Extrahieren und Hochladen ihrer Inhalte (UnCompress).
seo-title: UnCompressOptions
solution: Experience Manager
title: UnCompressOptions
topic: Scene7 Image Production System API
uuid: 1e6827db-8c5e-47db-b7ff-4e681e107e57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UnCompressOptions{#uncompressoptions}

Upload-Einstellung zur Verarbeitung von ZIP- und TAR-Dateien als Master-Assets (Keine) oder zum Extrahieren und Hochladen ihrer Inhalte (UnCompress).

>[!NOTE]
>
>`None` ist Standard.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> Prozess</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Steuert die Verarbeitung von ZIP- und TAR-Archivdateien. Bietet 2 Optionen: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> Keine:</span> Als Master-Assets verarbeiten </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> UnCompress:</span> Extrahieren und Verarbeiten von Inhalten. </li>
     </ul><p>Hinweis: Bei Zeichenfolgenkonstanten wird zwischen Groß- und Kleinschreibung unterschieden. Verwenden Sie <span class="codeph"> UnCompress</span>, nicht <span class="codeph"> entpacken</span> oder <span class="codeph"> unCompress</span>. </p></p> </td> 
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

Der `unCompressionOptions` Typ wird verwendet von:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

