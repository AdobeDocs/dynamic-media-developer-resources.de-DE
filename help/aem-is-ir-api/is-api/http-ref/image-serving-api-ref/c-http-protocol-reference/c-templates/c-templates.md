---
title: Vorlagen
description: Vorlagen können verwendet werden, um die Länge und Komplexität von Anfragen zu reduzieren, die mehrere Bildebenen zusammensetzen oder RTF-formatierten Text enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
TQID: 'https://experienceleague.adobe.com/FFRoxO7iVDzE7Kta5Vig4RtaPWa890tNHPwsAOcWVCw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 300
ht-degree: 0%

---

# Vorlagen{#templates}

Vorlagen können verwendet werden, um die Länge und Komplexität von Anfragen zu reduzieren, die mehrere Bildebenen zusammensetzen oder RTF-formatierten Text enthalten.

Benutzerdefinierte Variablen können verwendet werden, um die Verwendung von Vorlagen weiter zu vereinfachen. Vorlagen werden häufig so eingerichtet, dass Bilder oder Text einfach ausgetauscht oder andere Optionen zur Laufzeit festgelegt werden können.

Vorlagen werden als Datensätze in Bildkatalogen gespeichert, wobei der Vorlagentext im Feld `catalog::Modifier` und das Feld `catalog::Path` leer ist oder ein statisches Hintergrundbild angibt, das nicht dynamisch geändert werden kann.

Vorlagen werden mit dem Befehl `template=` oder in der Pfadkomponente der Anfrage-URL angegeben. Für die meisten Anwendungen wird empfohlen, den Befehl `template=` zum Angeben von Vorlagen zu verwenden. Der `template=`Befehl darf nicht im Feld &quot;`catalog::PostModifier`&quot; auftreten und darf nur im Feld &quot;`catalog::Modifier`&quot; in einer verschachtelten IS-Anfrage auftreten (d. h. in einem `src=is{...}`). Vorlagendatensätze dürfen in `src=`- oder `mask=`Befehlen nicht referenziert werden.

Alle in `mask=` Vorlage eingebetteten `src=` oder Befehle können in den Hauptkatalog der Anfrage oder in einen anderen Bildkatalog aufgelöst werden. Wenn kein `rootId` explizit angegeben ist, wird der Hauptkatalog angenommen. Die mit `template=` angegebene Vorlage kann sich auch im Hauptkatalog oder einem anderen Bildkatalog befinden.

Es wird dringend empfohlen, immer Standarddefinitionen für alle in einer Vorlage verwendeten Variablen einzuschließen. Auf diese Weise kann die Bildausgabe der Vorlage immer einfach durch Angabe von `attribute::RootId` und `catalog::Id` angezeigt werden, ohne wissen zu müssen, welche Variablen in der Vorlage verwendet werden.

Die vordefinierte Pfadersatzvariable `$object$` kann verwendet werden, um das im URL-Pfad angegebene Bildobjekt auf eine beliebige Ebenenquelle oder -maske ( `src=` oder `mask=`) anzuwenden, selbst in verschachtelten oder eingebetteten Anfragen.

* [Beispiel A](r-example-a.md)
* [Beispiel B](r-example-b.md)
* [Beispiel C](r-example-c.md)
