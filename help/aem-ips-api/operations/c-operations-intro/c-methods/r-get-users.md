---
description: Ruft eine Gruppe von Benutzern ab, die durch die Handles für Unternehmens-, Gruppen- und Benutzerrollen angegeben sind. Dieser Vorgang ermöglicht die Sortierung der zurückgegebenen Benutzer und die Filterung nach Zeichen.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 10%

---

# getUsers{#getusers}

Ruft eine Gruppe von Benutzern ab, die durch die Handles für Unternehmens-, Gruppen- und Benutzerrollen angegeben sind. Dieser Vorgang ermöglicht die Sortierung der zurückgegebenen Benutzer und die Filterung nach Zeichen.

## Autorisierte Benutzertypen {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | Nein | Inaktive Benutzer ein- oder ausschließen. Benutzer, die keine IPS-Administratoren sind, müssen aktives Mitglied von mindestens einem Unternehmen sein, damit sie API-Aufrufe durchführen können. Ein Autorisierungsfehler wird zurückgegeben, wenn der Benutzer keine aktiven Unternehmensmitgliedschaften hat. |
| `*`includeInvalid`*` | `xsd:boolean` | Nein | Hiermit können Sie ungültige Benutzer ein-/ausschließen. |
| `*`companyHandleArray`*` | `types:HandleArray` | Nein | Ergebnisse nach Unternehmen filtern. |
| `*`groupHandleArray`*` | `types:HandleArray` | Nein | Ergebnisse nach Gruppe filtern. |
| `*`userRoleArray`*` | `types:StringArray` | Nein | Ergebnisse nach Benutzerrolle filtern. |
| `*`charFilterField`*` | `xsd:string` | Nein | Ergebnisse nach dem Zeichenfolgenpräfix des Felds filtern (siehe [!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | Nein | Ergebnisse nach einem bestimmten Zeichen filtern. |
| `*`sortBy`*` | `xsd:string` | Nein | Auswahl der Sortierungsfelder für Benutzer. |
| `*`recordsPerPage`*` | `xsd:int` | Nein | Gibt die angegebene Anzahl von Datensätzen pro Seite zurück. |
| `*`resultsPage`*` | `xsd:int` | Nein | Ergebnisseite. |

**Ausgabe (getUsersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | Ja | Eine Gruppe von Benutzern. |

## Beispiele {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Dieses Codebeispiel gibt das Array von Benutzern für mehrere optionale Parameter zurück. Benutzerrollen, Benutzerzeichenfilterfelder und Benutzersortierungsfelder werden mithilfe bestimmter Zeichenfolgenkonstanten bestimmt.

**Anforderung**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Antwort**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
