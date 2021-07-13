---
description: Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammensetzen oder die rtf-formatierten Text enthalten.
solution: Experience Manager
title: Vorlagen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Vorlagen{#templates}

Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammensetzen oder die rtf-formatierten Text enthalten.

Benutzerdefinierte Variablen können verwendet werden, um die Verwendung von Vorlagen weiter zu vereinfachen. Vorlagen werden häufig so eingerichtet, dass ein einfacher Austausch von Bildern oder Text oder das Festlegen anderer Optionen zur Laufzeit möglich ist.

Vorlagen werden als Datensätze in Bildkatalogen gespeichert, wobei der Vorlagentext im Feld `catalog::Modifier` und das Feld `catalog::Path` leer sind oder ein statisches Hintergrundbild angeben, das nicht dynamisch geändert werden kann.

Vorlagen werden mit dem Befehl `template=` oder in der Pfadkomponente der Anfrage-URL angegeben. Für die meisten Anwendungen wird empfohlen, den Befehl `template=` zu verwenden, um Vorlagen anzugeben. Der Befehl `template=`darf nicht im Feld `catalog::PostModifier` auftreten und darf nur im Feld `catalog::Modifier` einer verschachtelten IS-Anforderung (d. h. in einem `src=is{...}`-Konstrukt) vorkommen. Vorlagendatensätze können nicht in `src=`- oder `mask=`Befehlen referenziert werden.

Alle in die Vorlage eingebetteten `src=`- oder `mask=`Befehle können in den Hauptkatalog der Anforderung oder in einen anderen Bildkatalog aufgelöst werden. Wenn kein `rootId` explizit angegeben ist, wird vom Hauptkatalog ausgegangen. Die mit `template=` angegebene Vorlage kann sich auch im Hauptkatalog oder in einem anderen Bildkatalog befinden.

Es wird dringend empfohlen, stets Standarddefinitionen für alle Variablen einzubeziehen, die in einer Vorlage verwendet werden. Auf diese Weise kann die Bildausgabe der Vorlage immer einfach durch Angabe der `attribute::RootId`- und `catalog::Id`-Werte angezeigt werden, ohne dass Sie wissen müssen, welche Variablen in der Vorlage verwendet werden.

Die vordefinierte Pfadersetzungsvariable `$object$` kann verwendet werden, um das im URL-Pfad angegebene Bildobjekt auch in verschachtelten oder eingebetteten Anforderungen auf jede Ebenenquelle oder -maske ( `src=` oder `mask=`) anzuwenden.

* [Beispiel A](r-example-a.md)
* [Beispiel B](r-example-b.md)
* [Beispiel C](r-example-c.md)
