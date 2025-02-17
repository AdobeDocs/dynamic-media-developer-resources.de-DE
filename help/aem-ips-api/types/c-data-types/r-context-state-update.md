---
description: Aktualisiert den Status des Veröffentlichungskontexts für ein Asset.
solution: Experience Manager
title: ContextStateUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e450d28-ec79-4540-824b-b0121b72c857
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 9%

---

# [!DNL ContextStateUpdate]{#contextstateupdate}

Aktualisiert den Status des Veröffentlichungskontexts für ein Asset.

Syntax

## Parameter {#section-9f747df071854c6896fdbb95684ad947}

Festlegen des Veröffentlichungskontextstatus eines Assets mit `setAssetsContextState`.

<table id="table_FD172CEA4EFE44E08ADA22D090DC06CA">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Name </th>
   <th colname="col2" class="entry"> Typ </th>
   <th colname="col3" class="entry"> Beschreibung </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string </span></td>
   <td colname="col3"> Verarbeiten Sie den Veröffentlichungskontext. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> publishState</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">Der aktualisierte Veröffentlichungsstatus des Assets für den angegebenen Veröffentlichungskontext. Beinhaltet: 
    <ul id="ul_CF6019C4CA3648B687C252F1A7C2EAAF">
     <li id="li_4367D7A058F045D98CDF58009E2AC7BC"><span class="codeph"> Zur Veröffentlichung markiert</span></li>
     <li id="li_EEFC6A76C1014C6D9D5E66F271B68606"><span class="codeph"> NotMarked for Publish</span></li>
     <li id="li_5145CFA39F5249C48DBD0A37543AF055"><span class="codeph"></span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [Status von Publish](../../string-constants/c-string-constants/r-publish-state.md#reference-a9d80231514b4272b39d10c1a7aadca8)
