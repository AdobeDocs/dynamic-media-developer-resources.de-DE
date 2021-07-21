---
description: Veröffentlicht Metadaten auf dem Metadaten-Server.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadaten
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---

# MetadataPublishJobType{#metadatapublishjobtype}

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
   <td colname="col3">Auf <span class="codeph"> True</span> setzen, um <i>alle</i>-Daten erneut auf dem Metadaten-Server zu veröffentlichen. <p>Hinweis:  Je nach Datenmenge kann dies mehrere Minuten bis zu einigen Stunden dauern. </p><p>Legen Sie diesen Parameter nicht fest, wenn Sie nur neue oder geänderte Metadaten veröffentlichen möchten. </p></td> 
  </tr> 
 </tbody> 
</table>
