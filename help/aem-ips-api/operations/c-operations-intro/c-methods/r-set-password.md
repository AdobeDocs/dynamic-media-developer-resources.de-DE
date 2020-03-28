---
description: Legt das Kennwort eines bestimmten Benutzers oder des Standardbenutzers auf einen bestimmten Wert fest, je nachdem, ob Sie ein Benutzerhandle angeben.
seo-description: Legt das Kennwort eines bestimmten Benutzers oder des Standardbenutzers auf einen bestimmten Wert fest, je nachdem, ob Sie ein Benutzerhandle angeben.
seo-title: setPassword
solution: Experience Manager
title: setPassword
topic: Scene7 Image Production System API
uuid: 78067f8d-4191-4580-a5a8-adb6edfcfab8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setPassword{#setpassword}

Legt das Kennwort eines bestimmten Benutzers oder des Standardbenutzers auf einen bestimmten Wert fest, je nachdem, ob Sie ein Benutzerhandle angeben.

Das Ablaufdatum des Kennworts ist optional. Wenn das Kennwort weggelassen wird, läuft es nie ab.

## Autorisierte Benutzertypen {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*Nur* der `IpsAdmin` Benutzertyp ist berechtigt, setPassword-Aufrufe gegen andere Benutzer auszuführen.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## Parameter {#section-0531294341f7483d89dacaa393dd659a}

**Input (setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Benutzerhandle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Kennwort </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Kennwort. </p> <p>Für das ausgewählte Kennwort werden die folgenden Anforderungen erzwungen: </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">Bei Kennwörtern wird zwischen Groß- und Kleinschreibung unterschieden. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">Die Mindestlänge des Kennworts beträgt acht Zeichen. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">Das Kennwort muss ein oder mehrere Zeichen aus den folgenden Zeichenklassen enthalten: 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Kleinere englische Zeichen. Beispiel: <span class="codeph"> b c d e </span> usw. </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Großbuchstabe englische Zeichen. Beispiel: <span class="codeph"> A B C D E </span> usw. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Zahlen. Beispiel: <span class="codeph"> 1 2 3 4 5 </span> usw. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Sonderzeichen. Sie können beispielsweise Folgendes verwenden: <span class="codeph"> ~ ! @ # $ % ^ * ( ) _ + - = { }| [ ] &amp; \ : "; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> password <span class="varname"> Expires </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Bestimmt das Ablaufdatum des Kennworts. <p>Hinweis:  Geben Sie die Zeitzone mit der Anforderung für dieses Feld ein. Die Zeitzonen werden auf "Central Time"eingestellt. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (setPasswordReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-23a6fbabdb3c4c3180076057e47ae567}

In diesem Codebeispiel wird ein Benutzerkennwort erstellt. Das Kennwort läuft nie ab, da es nicht `passwordExpires` angegeben wurde.

**Anforderung**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Antwort**

Keine.
