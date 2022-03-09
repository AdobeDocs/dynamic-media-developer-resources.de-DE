---
description: Ruft eine Liste der in einem bestimmten Feld verwendeten Zeichen ab.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 12%

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

**Eingabe (getUserCharsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| charField | `xsd:string` | Ja | Bestimmt den Papierkorbsstatus, nach dem gesucht werden soll. |
| includeInactive | `xsd:boolean` | Ja | Inaktive Benutzer ein- oder ausschließen. Benutzer, die keine IPS-Administratoren sind, müssen aktives Mitglied von mindestens einem Unternehmen sein, damit sie API-Aufrufe durchführen können. Ein Autorisierungsfehler wird zurückgegeben, wenn der Benutzer keine aktiven Unternehmensmitgliedschaften hat. |
| includeInvalid | `xsd:boolean` | Nein | Ungültige Benutzer ein- oder ausschließen. |
| companyHandleArray | `types:HandleArray` | Nein | Filtern Sie die Ergebnisse nach Unternehmen. |
| groupHandleArray | `types:HandleArray` | Nein | Filtert Ergebnisse basierend auf Gruppen. |
| userRoleArray | `types:StringArray` | Nein | Filtert Ergebnisse basierend auf der Benutzerrolle. |
| numChars | `xsd:int` | Nein | Aktivieren Sie >1 Zeichen. |

**Ausgabe (getUserCharsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userCharsArray | `types:StringArray` | Ja | Ein Array von Zeichenpräfixen. |

## Beispiele {#section-3702f165e8b041139a6144f4a76ca25f}

Dieses Codebeispiel gibt zurück:

* Die ersten Zeichen der Nachnamen der Benutzer eines bestimmten Unternehmens.
* Eine Gruppe von Gruppen.
* Eine Reihe von Benutzerrollen.

Die String-Konstante Benutzerzeichenfilter Felder bestimmt den Typ der zurückgegebenen Benutzerzeichen.

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
