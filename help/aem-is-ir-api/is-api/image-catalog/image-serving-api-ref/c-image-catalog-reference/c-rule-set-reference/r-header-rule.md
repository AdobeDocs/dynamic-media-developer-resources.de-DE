---
description: HTTP-Antwort-Header-Element. Optional in <rule>-Elementen.
solution: Experience Manager
title: Header
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---


# Header{#header}

HTTP-Antwort-Header-Element. Optional in `<rule>`-Elementen.

## Attribute {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Erforderlich. Gibt den Namen des HTTP-Headers an.

**`Action`= &quot;set&quot; |`"add"`**: Optional. Der Standardwert ist `"set"`, wodurch jeder aktuelle Header-Wert ersetzt wird. Geben Sie `"add"` an, um den Kopfzeilenwert durch ein Komma zu trennen.

## Daten {#section-a387f541396c49d99c29692a38032914}

Kopfzeilenwert.

## Beschreibung {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Ermöglicht das Hinzufügen neuer HTTP-Antwort-Kopfzeilen sowie das Hinzufügen oder Ersetzen von Werten vordefinierter Kopfzeilen. Namen und Werte müssen den HTTP-Standards entsprechen. Es wird keine zusätzliche Kodierung angewendet.

Image Serving-Ersatzvariablen können im Kopfzeilennamen und im Kopfzeilenwert verwendet werden. Dadurch können beide Zeichenfolgen von der Anforderung gesteuert werden.

## Beispiel {#section-cb5b738b9b93407cb2f4d35af3e59c02}

Die folgende Regel wendet einen benutzerdefinierten Header an, wenn der Header-Wert in der Anforderung als Variable angegeben wird:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Diese Regel wird durch die folgende Anforderung ausgelöst, indem der HTTP-Antwort-Header `Edge-Control::no-store` festgelegt wird:

`http://server/is/image/cat/id?$Edge-Control=no-store`
