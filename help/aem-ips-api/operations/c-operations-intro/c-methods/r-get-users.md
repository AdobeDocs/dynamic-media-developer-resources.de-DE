---
description: Ruft ein Array von Benutzern ab, wie durch Handles für Unternehmens-, Gruppen- und Benutzerrollen angegeben. Mit diesem Vorgang können Sie zurückgegebene Benutzer sortieren und nach Zeichen filtern.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 9%

---

# getUsers{#getusers}

Ruft ein Array von Benutzern ab, wie durch Handles für Unternehmens-, Gruppen- und Benutzerrollen angegeben. Mit diesem Vorgang können Sie zurückgegebene Benutzer sortieren und nach Zeichen filtern.

## Autorisierte Benutzertypen {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| includeInaktiv | `xsd:boolean` | Nein | Ein- oder Ausschließen von inaktiven Benutzern. Nicht-IPS-Admin-Benutzer müssen aktive Mitglieder mindestens eines Unternehmens sein, um API-Aufrufe ausführen zu können. Ein Autorisierungsfehler wird zurückgegeben, wenn der Benutzer keine aktiven Unternehmensmitgliedschaften hat. |
| includeInvalid | `xsd:boolean` | Nein | Ermöglicht das Ein-/Ausschließen ungültiger Benutzer. |
| companyHandleArray | `types:HandleArray` | Nein | Filtern Sie die Ergebnisse nach Unternehmen. |
| groupHandleArray | `types:HandleArray` | Nein | Ergebnisse nach Gruppe filtern. |
| userRoleArray | `types:StringArray` | Nein | Filtern Sie die Ergebnisse nach Benutzerrolle. |
| charFilterField | `xsd:string` | Nein | Ergebnisse nach dem Zeichenfolgenpräfix des Felds filtern (siehe [!DNL Trash State).] |
| charFilter | `xsd:string` | Nein | Filtern Sie die Ergebnisse nach einem bestimmten Zeichen. |
| sortBy | `xsd:string` | Nein | Auswahl der Sortierfelder des Benutzers. |
| recordsPerPage | `xsd:int` | Nein | Gibt die angegebene Anzahl von Datensätzen pro Seite zurück. |
| resultsPage | `xsd:int` | Nein | Ergebnisseite. |

**Ausgabe (getUsersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userArray | `types:UserArray` | Ja | Ein Array von Benutzern. |

## Beispiele {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Dieses Codebeispiel gibt das Array von Benutzern für mehrere optionale Parameter zurück. Benutzerrollen, Benutzerzeichenfilterfelder und Benutzersortierfelder werden mithilfe spezifischer Zeichenfolgenkonstanten bestimmt.

**Anfrage**

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
