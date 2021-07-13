---
description: Die folgenden Absatzformatierungsbefehle werden unterstützt.
solution: Experience Manager
title: Absatzformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

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
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>Absatzformatierung auf Standard zurücksetzen </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>Text linksbündig ausrichten </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>Text rechtsbündig ausrichten. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>Text horizontal zentrieren </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>Text horizontal ausrichten </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>Richten Sie die letzte Zeile eines Absatzes linksbündig aus. </p> </td> 
   <td> <p>Standard; <span class="codeph"> textPs= </span> nur; ignoriert, wenn <span class="codeph"> \qj </span>nicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>Richten Sie die letzte Zeile eines gerechtfertigten Absatzes rechtsbündig aus. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignoriert, wenn  <span class="codeph"> \qj nicht aktiv  </span> ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>Zentrieren Sie die letzte Zeile eines begründeten Absatzes. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignoriert, wenn  <span class="codeph"> \qj nicht aktiv  </span>ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>Die letzte Zeile eines begründeten Absatzes verlängern (ausdehnen). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignoriert, wenn  <span class="codeph"> \qj nicht aktiv  </span>ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Einzug der ersten Zeile. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> nur verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Linker Einzug. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> nur verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Rechter Einzug. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> nur verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Abstand zwischen den Zeilen. </p> </td> 
   <td> <p>0 (Standard) für den automatischen Zeilenabstand; positive Werte, die nur Werte verwenden, wenn größer als der standardmäßige Zeilenabstand ist; negativer Wert, um den Abstand zu erzwingen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zeilenabstand mehrere Flag. </p> </td> 
   <td> <p>Legen Sie den Wert 0 (Standard) fest, wenn <span class="codeph"> \sl </span> sich in Zweigen befindet, auf 1, wenn <span class="codeph"> \sl </span> das Vielfache des Standardabstands beträgt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zusätzlicher Abstand vor Absatz. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>wendet <span class="codeph"> \sb </span> auf den ersten Absatz im Textfeld an, <span class="codeph"> textPs= </span> nicht. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zusätzlicher Abstand nach Absatz. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> wendet <span class="codeph"> \sa </span> auf den letzten Absatz im Textfeld an, <span class="codeph"> textPs= </span> nicht. </p> </td> 
  </tr> 
 </tbody> 
</table>
