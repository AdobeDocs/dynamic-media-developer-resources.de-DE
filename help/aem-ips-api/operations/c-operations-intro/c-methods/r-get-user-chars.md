---
description: Ruft eine Liste der in einem bestimmten Feld verwendeten Zeichen ab.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
TQID: 'https://experienceleague.adobe.com/ojFrVXletWbKwGTjfJIfRI9M9BBJT7zj4AGrvVMP6T8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 10%

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
| charField | `xsd:string` | Ja | Legt den zu suchenden Papierkorb-Status fest. |
| includeInaktiv | `xsd:boolean` | Ja | Ein- oder Ausschließen von inaktiven Benutzern. Nicht-IPS-Admin-Benutzer müssen aktive Mitglieder mindestens eines Unternehmens sein, um API-Aufrufe ausführen zu können. Ein Autorisierungsfehler wird zurückgegeben, wenn der Benutzer keine aktiven Unternehmensmitgliedschaften hat. |
| includeInvalid | `xsd:boolean` | Nein | Ein- oder Ausschließen von ungültigen Benutzern. |
| companyHandleArray | `types:HandleArray` | Nein | Filtern Sie die Ergebnisse nach Unternehmen. |
| groupHandleArray | `types:HandleArray` | Nein | Filtert Ergebnisse nach Gruppen. |
| userRoleArray | `types:StringArray` | Nein | Filtert Ergebnisse nach Benutzerrolle. |
| numChars | `xsd:int` | Nein | Aktivieren Sie >1 Zeichen. |

**Ausgabe (getUserCharsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userCharsArray | `types:StringArray` | Ja | Ein Array von Zeichenpräfixen. |

## Beispiele {#section-3702f165e8b041139a6144f4a76ca25f}

Dieses Code-Beispiel gibt zurück:

* Erste Zeichen der Nachnamen der Benutzer eines bestimmten Unternehmens.
* Eine Gruppe.
* Eine Reihe von Benutzerrollen.

Die Zeichenfolgenkonstante des Benutzerzeichenfilters bestimmt den Typ der zurückgegebenen Benutzerzeichen.

**Anfrage**

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

