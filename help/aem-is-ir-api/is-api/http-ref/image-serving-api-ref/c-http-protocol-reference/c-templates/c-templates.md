---
title: Vorlagen
description: Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammensetzen oder die rtf-formatierten Text enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Vorlagen{#templates}

Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammensetzen oder die rtf-formatierten Text enthalten.

Benutzerdefinierte Variablen können zur weiteren Vereinfachung der Vorlagenverwendung verwendet werden. Vorlagen werden häufig so eingerichtet, dass ein einfacher Austausch von Bildern oder Text oder das Festlegen anderer Optionen zur Laufzeit möglich ist.

Vorlagen werden als Datensätze in Bildkatalogen gespeichert, wobei der Vorlagentext im Feld `catalog::Modifier` und das Feld `catalog::Path` leer sind oder ein statisches Hintergrundbild angegeben wird, das nicht dynamisch geändert werden kann.

Vorlagen werden mit dem Befehl `template=` oder in der Pfadkomponente der Anfrage-URL angegeben. Für die meisten Anwendungen wird empfohlen, den Befehl `template=` zu verwenden, um Vorlagen anzugeben. Der Befehl `template=`darf nicht im Feld `catalog::PostModifier` auftreten und darf nur im Feld `catalog::Modifier` einer verschachtelten IS-Anforderung (d. h. in einem `src=is{...}` -Konstrukt) auftreten. Vorlagendatensätze werden möglicherweise nicht in den Befehlen `src=` oder `mask=`referenziert.

Alle `src=` - oder `mask=` -Befehle, die in die Vorlage eingebettet sind, können in den Hauptkatalog der Anforderung oder in einen anderen Bildkatalog aufgelöst werden. Wenn keine explizite Angabe von `rootId` erfolgt, wird vom Hauptkatalog ausgegangen. Die mit `template=` angegebene Vorlage befindet sich möglicherweise auch im Hauptkatalog oder in einem anderen Bildkatalog.

Es wird dringend empfohlen, stets Standarddefinitionen für alle Variablen einzubeziehen, die in einer Vorlage verwendet werden. Auf diese Weise kann die Bildausgabe der Vorlage immer einfach durch Angabe von `attribute::RootId` und `catalog::Id` angezeigt werden, ohne dass Sie wissen müssen, welche Variablen in der Vorlage verwendet werden.

Die vordefinierte Pfadersetzungsvariable `$object$` kann verwendet werden, um das im URL-Pfad angegebene Bildobjekt auch in verschachtelten oder eingebetteten Anforderungen auf jede Ebenenquelle oder -maske ( `src=` oder `mask=`) anzuwenden.

* [Beispiel A](r-example-a.md)
* [Beispiel B](r-example-b.md)
* [Beispiel C](r-example-c.md)
