---
description: Ruft ein Array von Benutzern ab, wie durch Handles für Unternehmens-, Gruppen- und Benutzerrollen angegeben. Mit diesem Vorgang können Sie zurückgegebene Benutzer sortieren und nach Zeichen filtern.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
TQID: 'https://experienceleague.adobe.com/17FQLNVfRg84FeVetVfuTWoLRMf8ugBwXBi2CpmLZfI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
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
