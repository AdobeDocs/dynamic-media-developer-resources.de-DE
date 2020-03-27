---
description: Ruft ein Benutzerarray ab, das nach Firmen-, Gruppen- und Benutzerrollenhandlern angegeben ist. Mit diesem Vorgang können Sie zurückgegebene Benutzer sortieren und nach Zeichen filtern.
seo-description: Ruft ein Benutzerarray ab, das nach Firmen-, Gruppen- und Benutzerrollenhandlern angegeben ist. Mit diesem Vorgang können Sie zurückgegebene Benutzer sortieren und nach Zeichen filtern.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Scene7 Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUsers{#getusers}

Ruft ein Benutzerarray ab, das nach Firmen-, Gruppen- und Benutzerrollenhandlern angegeben ist. Mit diesem Vorgang können Sie zurückgegebene Benutzer sortieren und nach Zeichen filtern.

## Autorisierte Benutzertypen {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`includeInactive`*` | `xsd:boolean` | Nein | Inaktive Benutzer ein- oder ausschließen. Nicht-IPS-Administratoren müssen Mitglied von mindestens einer Firma sein, um für alle API-Aufrufe autorisiert zu sein. Ein Autorisierungsfehler wird zurückgegeben, wenn der Benutzer über keine aktive Firma verfügt. |
| ` *`includeInvalid`*` | `xsd:boolean` | Nein | Hiermit können Sie ungültige Benutzer ein-/ausschließen. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Nein | Filtern Sie die Ergebnisse nach Firma. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Nein | Filtern Sie die Ergebnisse nach Gruppe. |
| ` *`userRoleArray`*` | `types:StringArray` | Nein | Filtern Sie die Ergebnisse nach Benutzerrolle. |
| ` *`charFilterField`*` | `xsd:string` | Nein | Ergebnisse nach dem Zeichenfolgenpräfix des Felds filtern (siehe [!DNL Trash State).] |
| ` *`charFilter`*` | `xsd:string` | Nein | Filtern Sie die Ergebnisse nach einem bestimmten Zeichen. |
| ` *`sortBy`*` | `xsd:string` | Nein | Auswahl der Benutzersortierungsfelder. |
| ` *`recordsPerPage`*` | `xsd:int` | Nein | Gibt die angegebene Anzahl von Datensätzen pro Seite zurück. |
| ` *`resultsPage`*` | `xsd:int` | Nein | Ergebnisseite. |

**Ausgabe (getUsersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`userArray`*` | `types:UserArray` | Ja | Ein Array von Benutzern. |

## Beispiele {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Dieses Codebeispiel gibt das Array der Benutzer für mehrere optionale Parameter zurück. Benutzerrollen, Filterfelder für Benutzerzeichen und Benutzersortierungsfelder werden mithilfe bestimmter Zeichenfolgenkonstanten bestimmt.

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

