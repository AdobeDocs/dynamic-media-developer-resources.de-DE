---
description: Direkten Zugriff auf pfadbasierte Assets zulassen.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Direkten Zugriff auf pfadbasierte Assets zulassen.

Wenn dieses Attribut definiert ist, ist der pfadbasierte Zugriff für die angegebenen Objekttypen zulässig oder eingeschränkt, je nachdem, ob die Variable `include` oder `exclude` verwendet.

>[!NOTE]
>
>Wenn die Variable `AllowDirectAccess` -Attribut nicht angegeben ist, lautet der Standardwert `exclude`.

* `include` ermöglicht den Zugriff auf die angegebenen Objekttypen und beschränkt den Zugriff auf alle anderen.
* `exclude` beschränkt den Zugriff auf die angegebenen Objekttypen und ermöglicht den Zugriff für alle anderen.

Wenn `include` nor `exclude` festgelegt ist, `include` wird angenommen.

Die folgenden Typen können gesteuert werden:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Beispiele {#section-4c3765ebaa4245a799b454fc196f9237}

* Zulassen des direkten Zugriffs nur für `IS` und `STATIC` Objekttypen

  `AllowDirectAccess=include:IS,STATIC`

* Direkten Zugriff auf alle Objektarten zulassen (mit Ausnahme von `IS` und `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Direkten Zugriff zulassen für *no* Objekttypen (d. h., keine einschließen)

  `AllowDirectAccess=include:`

* Direkten Zugriff zulassen für *all* Objekttypen (d. h. keine ausschließen)

  `AllowDirectAccess=exclude:`

* Entspricht `include:IS,STATIC` (if `include`/ `exclude` nicht vorhanden ist, `include` wird angenommen)

  `AllowDirectAccess=IS,STATIC`

  Beachten Sie, dass der Standardwert verwendet wird, wenn die Variable `AllowDirectAccess` für dieses Unternehmen nicht angegeben ist.

* Keine einschließen, entspricht `include:` (if `include`/ `exclude` nicht vorhanden ist, `include` wird angenommen)

  `AllowDirectAccess=`
