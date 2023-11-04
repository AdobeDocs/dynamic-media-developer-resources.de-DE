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

Vorlagen werden als Datensätze in Bildkatalogen gespeichert, wobei der Vorlagentext im `catalog::Modifier` und dem `catalog::Path` leer oder ein statisches Hintergrundbild angeben, das nicht dynamisch geändert werden kann.

Vorlagen werden mit der Variablen `template=` -Befehl oder in der Pfadkomponente der Anfrage-URL. Für die meisten Anwendungen wird empfohlen, die `template=` -Befehl, um Vorlagen anzugeben. Die `template=`darf nicht im `catalog::PostModifier` und kann nur im `catalog::Modifier` in einer verschachtelten IS-Anforderung (d. h. in einer `src=is{...}` -Konstrukt). Vorlagendatensätze werden unter `src=` oder `mask=`Befehle.

Alle `src=` oder `mask=`-Befehle, die in die Vorlage eingebettet sind, können in den Hauptkatalog der Anforderung oder in einen anderen Bildkatalog aufgelöst werden. Wenn nicht `rootId` explizit angegeben ist, wird vom Hauptkatalog ausgegangen. Die mit `template=` kann sich auch im Hauptkatalog oder in einem anderen Bildkatalog befinden.

Es wird dringend empfohlen, stets Standarddefinitionen für alle Variablen einzubeziehen, die in einer Vorlage verwendet werden. Auf diese Weise kann die Bildausgabe der Vorlage immer einfach durch Angabe der zugehörigen `attribute::RootId` und `catalog::Id`, ohne wissen zu müssen, welche Variablen in der Vorlage verwendet werden.

Die vordefinierte Pfadersetzungsvariable `$object$` kann verwendet werden, um das im URL-Pfad angegebene Bildobjekt auf eine beliebige Ebenenquelle oder -maske anzuwenden ( `src=` oder `mask=`), auch in verschachtelten oder eingebetteten Anforderungen.

* [Beispiel A](r-example-a.md)
* [Beispiel B](r-example-b.md)
* [Beispiel C](r-example-c.md)
