---
description: Die folgenden Absatzformatierungsbefehle werden unterstützt.
seo-description: Die folgenden Absatzformatierungsbefehle werden unterstützt.
seo-title: Absatzformatierung
solution: Experience Manager
title: Absatzformatierung
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '239'
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
   <td> <p> <span class="codeph"> textPs=  </span> nur </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>Text linksbündig ausrichten </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>Text rechtsbündig ausrichten </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>Text horizontal zentrieren </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>Richten Sie den Text horizontal aus. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> nur </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>Richten Sie die letzte Zeile eines Absatzes linksbündig aus. </p> </td> 
   <td> <p>Standard; Nur <span class="codeph"> textPs= </span>; ignoriert, wenn <span class="codeph"> \qj </span>nicht aktiv ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>Richten Sie die letzte Zeile eines begründeten Absatzes rechtsbündig aus. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignoriert, wenn  <span class="codeph"> \qj nicht aktiv  </span> ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>Zentriert die letzte Zeile eines begründeten Absatzes. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignoriert, wenn  <span class="codeph"> \qj nicht aktiv  </span>ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>Die letzte Zeile eines begründeten Absatzes wird abgeglichen (gestreckt). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignoriert, wenn  <span class="codeph"> \qj nicht aktiv  </span>ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Einzug erste Zeile. </p> </td> 
   <td> <p>Twips; Nur <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Linker Einzug. </p> </td> 
   <td> <p>Twips; Nur <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Rechter Einzug. </p> </td> 
   <td> <p>Twips; Nur <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Abstand zwischen den Zeilen. </p> </td> 
   <td> <p>0 (Standard) für den automatischen Zeilenabstand; positive Werte, die nur dann einen Wert verwenden, wenn der Zeilenabstand größer als der Standardabstand ist; negativer Wert, um den Abstand zu erzwingen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zeilenabstand für mehrere Flag. </p> </td> 
   <td> <p>Auf 0 setzen (Standard), wenn <span class="codeph"> \sl </span> sich in Twips befindet, auf 1, wenn <span class="codeph"> \sl </span> sich in einem Vielfachen des Standardabstands befindet. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zusätzlicher Abstand vor Absatz </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>wendet <span class="codeph"> \sb </span> auf den ersten Absatz im Textfeld an, <span class="codeph"> textPs= </span> nicht. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zusätzlicher Abstand nach Absatz </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> wendet <span class="codeph"> \sa </span> auf den letzten Absatz im Textfeld an, <span class="codeph"> textPs= </span> nicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

