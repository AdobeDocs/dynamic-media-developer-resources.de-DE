---
description: Ruft eine Liste der in einem bestimmten Feld verwendeten Zeichen ab.
seo-description: Ruft eine Liste der in einem bestimmten Feld verwendeten Zeichen ab.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Scene7 Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUserChars{#getuserchars}

Ruft eine Liste der in einem bestimmten Feld verwendeten Zeichen ab.

Syntax

## Autorisierte Benutzertypen {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Input (getUserCharsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`charField`*` | `xsd:string` | Ja | Legt den Papierkorbsstatus fest, nach dem gesucht werden soll. |
| ` *`includeInactive`*` | `xsd:boolean` | Ja | Inaktive Benutzer ein- oder ausschließen. Nicht-IPS-Administratoren müssen Mitglied von mindestens einer Firma sein, um für alle API-Aufrufe autorisiert zu sein. Ein Autorisierungsfehler wird zurückgegeben, wenn der Benutzer über keine aktive Firma verfügt. |
| ` *`includeInvalid`*` | `xsd:boolean` | Nein | Schließen Sie ungültige Benutzer ein oder aus. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Nein | Filtern Sie die Ergebnisse nach Firma. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Nein | Die Ergebnisse der Filter basieren auf Gruppen. |
| ` *`userRoleArray`*` | `types:StringArray` | Nein | Filter werden basierend auf der Benutzerrolle angezeigt. |
| ` *`numChars`*` | `xsd:int` | Nein | Aktivieren Sie >1 Zeichen. |

**Output (getUserCharsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`userCharsArray`*` | `types:StringArray` | Ja | Ein Array von Zeichenpräfixen. |

## Beispiele {#section-3702f165e8b041139a6144f4a76ca25f}

Dieses Codebeispiel gibt Folgendes zurück:

* Erste Zeichen der Nachnamen der Benutzer einer bestimmten Firma.
* Eine Gruppe von Gruppen.
* Ein Satz von Benutzerrollen.

Die Zeichenfolgen-Konstante &quot;Benutzerzeichenfilter-Felder&quot;bestimmt den Typ der zurückgegebenen Benutzerzeichen.

**Anforderung**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Antwort**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```

