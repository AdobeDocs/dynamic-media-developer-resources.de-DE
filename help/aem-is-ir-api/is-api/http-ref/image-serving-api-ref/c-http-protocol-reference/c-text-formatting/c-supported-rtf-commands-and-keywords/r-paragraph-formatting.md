---
description: Die folgenden Absatzformatierungsbefehle werden unterstützt.
solution: Experience Manager
title: Absatzformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
TQID: 'https://experienceleague.adobe.com/bksi7t36irm8XQqI0LtJl3kNaSCZANRzbCKf80o-eNM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# Absatzformatierung{#paragraph-formatting}

Die folgenden Absatzformatierungsbefehle werden unterstützt.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Befehl </p> </th> 
   <th class="entry"> <p>Beschreibung </p> </th> 
   <th class="entry"> <p>Anmerkungen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Absatzformatierung auf Standard zurücksetzen. </p> </td> 
   <td> <p> <span class="codeph"> textPs= nur </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Linksbündiger Text. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Text rechts ausrichten. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Text horizontal zentrieren. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Text horizontal ausrichten. </p> </td> 
   <td> <p> <span class="codeph"> textPs= nur </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastQL-</span> </td> 
   <td> <p>Linke Ausrichtung der letzten Zeile eines Absatzes. </p> </td> 
   <td> <p>Standard; nur <span class="codeph"> textPs= </span>; wird ignoriert, wenn <span class="codeph"> \qj </span>nicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastQr </span> </td> 
   <td> <p>Richten Sie die letzte Zeile eines gerechtfertigten Absatzes rechts aus. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>; wird ignoriert, wenn <span class="codeph"> \qj </span> nicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastQC </span> </td> 
   <td> <p>Zentriert die letzte Zeile eines gerechtfertigten Absatzes. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>; wird ignoriert, wenn <span class="codeph"> \qj </span>nicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastQJ </span> </td> 
   <td> <p>Richten Sie die letzte Zeile eines gerechtfertigten Absatzes aus (dehnen Sie sie). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>; wird ignoriert, wenn <span class="codeph"> \qj </span>nicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> n </span> </span> </td> 
   <td> <p>Einzug der ersten Zeile. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= nur </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Linker Einzug. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= nur </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Rechter Einzug. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= nur </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Abstand zwischen den Zeilen. </p> </td> 
   <td> <p>0 (Standard) für automatischen Zeilenabstand; positive Werte nur verwenden, wenn der Wert größer als der standardmäßige Zeilenabstand ist; negativer Wert für den erzwungenen Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Mehrfachkennzeichnung für Zeilenabstand. </p> </td> 
   <td> <p>Setzen Sie auf 0 (Standard), wenn <span class="codeph"> \sl </span> in Twips vorliegt, auf 1, wenn <span class="codeph"> \sl </span> im Vielfachen des Standardabstands liegt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Zusätzliches Leerzeichen vor dem Absatz. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>gilt <span class="codeph"> \sb </span> für den ersten Absatz im Textfeld, <span class="codeph"> textPs= </span> nicht. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> n </span> </span> </td> 
   <td> <p>Zusätzliches Leerzeichen nach Absatz. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> gilt <span class="codeph"> \sa </span> für den letzten Absatz im Textfeld, <span class="codeph"> textPs= </span> nicht. </p> </td> 
  </tr> 
 </tbody> 
</table>
