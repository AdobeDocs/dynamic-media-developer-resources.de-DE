---
description: Veröffentlicht Metadaten auf dem Metadaten-Server.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL MetadataPublishJobType]{#metadatapublishjobtype}

Veröffentlicht Metadaten auf dem Metadaten-Server.

Syntax

## Parameter {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Legen Sie fest auf <span class="codeph"> True</span> zum Veröffentlichen <i>all</i> Daten erneut an den Metadaten-Server übermittelt. <p>Hinweis: Je nach Datenmenge kann dies mehrere Minuten bis zu einigen Stunden dauern. </p><p>Legen Sie diesen Parameter nicht fest, wenn Sie nur neue oder geänderte Metadaten veröffentlichen möchten. </p></td> 
  </tr> 
 </tbody> 
</table>
