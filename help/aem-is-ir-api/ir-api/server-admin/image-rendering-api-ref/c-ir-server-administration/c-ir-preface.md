---
description: In dieser Dokumentation werden Probleme mit der Serververwaltung erläutert und die Konfigurationseinstellungen für das Dynamic Media-Bild-Rendering beschrieben.
solution: Experience Manager
title: Server-Administrations-Vorwort
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 65fc3510-3d47-4650-bf89-322b517dc004
TQID: 'https://experienceleague.adobe.com/IXe7n1U-Fx2YRroKjS6uszhughS9vNA9I-MLciDJsz0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 0%

---

# Server-Administrations-Vorwort{#server-administration-preface}

In dieser Dokumentation werden Probleme mit der Serververwaltung erläutert und die Konfigurationseinstellungen für das Dynamic Media-Bild-Rendering beschrieben.

**Vorgesehene Zielgruppe**

Diese Dokumentation richtet sich an Systemadministratoren und Webmaster, die Dynamic Media Image Rendering installieren, konfigurieren und verwalten müssen.

**Dokumentkonventionen**

Elementen, die in dieser Dokumentation beschrieben werden, wird oft das Präfix der folgenden Elementtypen vorangestellt:

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>attribute::Item </p></td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „attribute::“ bezieht sich auf ein Bildkatalogattribut. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>catalog:item </p></td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „catalog::“ bezieht sich auf ein Materialkatalogdatenfeld. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>icc:item </p></td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „icc::“ bezieht sich auf ein Feld in der ICC-Farbprofilzuordnung. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>makro::item </p></td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „Makro::“ bezieht sich auf ein Feld in der Makrodefinitionstabelle. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ruleset:item </p></td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „ruleset::“ bezieht sich auf ein Element in einem Regelsatz zur Vorverarbeitung von URLs. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>default::Item </p></td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „default::“ bezieht sich auf ein Attribut des Standardbildkatalogs. </p></td> 
 </tr> 
</table>

