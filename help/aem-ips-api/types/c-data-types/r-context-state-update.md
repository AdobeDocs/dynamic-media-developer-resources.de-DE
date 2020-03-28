---
description: Aktualisiert den Status des Veröffentlichungskontexts für ein Asset.
seo-description: Aktualisiert den Status des Veröffentlichungskontexts für ein Asset.
seo-title: ContextStateUpdate
solution: Experience Manager
title: ContextStateUpdate
topic: Scene7 Image Production System API
uuid: ef579d3c-1899-4088-903e-e6ed5a414ca8
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# ContextStateUpdate{#contextstateupdate}

Aktualisiert den Status des Veröffentlichungskontexts für ein Asset.

Syntax

## Parameter {#section-9f747df071854c6896fdbb95684ad947}

Legen Sie den Veröffentlichungskontextstatus eines Assets mit `setAssetsContextState`fest.

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
   <td colname="col3"> Behandeln Sie den Veröffentlichungskontext. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> publishState</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">Der aktualisierte Status "Veröffentlicht"des Assets für den angegebenen Veröffentlichungskontext. Umfasst: 
    <ul id="ul_CF6019C4CA3648B687C252F1A7C2EAAF">
     <li id="li_4367D7A058F045D98CDF58009E2AC7BC"><span class="codeph"> MarkedForPublish</span></li>
     <li id="li_EEFC6A76C1014C6D9D5E66F271B68606"><span class="codeph"> NotMarkedForPublish</span></li>
     <li id="li_5145CFA39F5249C48DBD0A37543AF055"><span class="codeph"></span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [Veröffentlichungsstatus](../../string-constants/c-string-constants/r-publish-state.md#reference-a9d80231514b4272b39d10c1a7aadca8)

