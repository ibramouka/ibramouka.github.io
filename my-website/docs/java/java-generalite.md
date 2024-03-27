## JVM :
-La JVM est une machine virtuelle qui permet à l'ordinateur d'exécuter des programmes
Java qui ont été compilés en bytecode. Le bytecode est indépendant de la plate-forme, et
s'exécute sur tout ordinateur qui héberge une JVM.
-Il comprend un compilateur juste à
temps (JIT) qui convertit le bytecode en instructions en langage machine, permettant aux
applications de s'exécuter aussi rapidement qu'un exécutable natif

**En java quelle difference entre methode public privée et protected**

En Java, les mots-clés public, private et protected sont des modificateurs d'accès utilisés pour spécifier la portée (ou la visibilité) des membres d'une classe (méthodes, variables, etc.). Voici les différences entre ces trois modificateurs :

**- Public (public) :**
Une méthode ou un champ déclaré comme public est accessible de n'importe où, que ce soit à l'intérieur de la classe, à l'extérieur de la classe dans le même package, ou à l'extérieur du package.
Cela signifie que la méthode ou le champ peut être utilisé par d'autres classes sans aucune restriction.

**- Private (private) :**
Une méthode ou un champ déclaré comme private est accessible uniquement à l'intérieur de la classe où il est déclaré.
Cela signifie qu'il ne peut pas être accédé directement par une autre classe, même si elle est dans le même package.

**- Protected (protected) :**
Une méthode ou un champ déclaré comme protected est accessible à la fois dans la classe où il est défini, dans toutes les sous-classes (même si elles sont dans un package différent), et dans d'autres classes du même package.
Il est similaire au mode default (ou sans modificateur) en ce sens qu'il autorise l'accès à d'autres classes dans le même package. La différence réside dans le fait qu'il autorise également l'accès aux sous-classes même si elles sont situées dans un package différent.
En résumé :

    - public : accessible partout.
    - private : accessible uniquement dans la classe.
    - protected : accessible dans la classe, dans ses sous-classes et dans le même package.

##  Qu’est-ce qu’une exception ? Décrivez brièvement les deux types d’exception utilisés dans le code en Java

En Java, une exception est une anomalie ou une situation imprévue qui se produit pendant l'exécution d'un programme. 
Lorsqu'une exception se produit, elle interrompt normalement le flux normal du programme et peut être gérée par des mécanismes spécifiques de gestion des erreurs.
Il existe deux types d'exceptions en Java :

**- Exceptions vérifiées (checked exceptions) :**
- Les exceptions vérifiées sont des exceptions qui doivent être soit capturées (avec un bloc try-catch) soit déclarées dans la signature de la méthode (avec une clause throws).
- Ces exceptions sont généralement utilisées pour signaler des conditions qui peuvent survenir lors de l'exécution d'une méthode, mais qui sont hors du contrôle du programmeur (par exemple, les erreurs d'entrée-sortie).
- Les classes d'exceptions vérifiées héritent de la classe Exception ou de ses sous-classes, à l'exception des classes RuntimeException et de ses sous-classes.

**- Exceptions non vérifiées (unchecked exceptions) :**
- Les exceptions non vérifiées sont des exceptions qui n'ont pas besoin d'être déclarées dans la signature de la méthode ou d'être capturées explicitement.
- Elles sont souvent utilisées pour signaler des erreurs de programmation, telles que les divisions par zéro, les accès à des indices de tableau inexistant, etc.
- Les classes d'exceptions non vérifiées héritent de la classe RuntimeException ou de ses sous-classes.

En résumé, les exceptions vérifiées doivent être gérées explicitement dans le code, tandis que les exceptions non vérifiées peuvent être ignorées (mais ce n'est généralement pas une bonne pratique) car elles sont souvent le résultat d'erreurs de programmation qui devraient être corrigées.

## – Que sont les classes d’emballage (aussi appelées classes d’enveloppe ou wrapper classes)? Citez deux d’entre elles et leur primitif correspondant. Comment chacun se rapporte-t-il à un objet ?

Les classes d'emballage (ou wrapper classes en anglais) en Java sont des classes qui enveloppent (ou encapsulent) les types de données primitifs Java. Elles permettent de traiter les types primitifs comme des objets. Chaque type primitif a sa classe d'emballage correspondante. Ces classes fournissent des méthodes utiles pour travailler avec les types primitifs comme s'ils étaient des objets, notamment pour effectuer des opérations de conversion, de comparaison, etc.
Deux exemples de classes d'emballage et leur type primitif correspondant sont les suivants :

**Integer :**
- Type primitif correspondant : int
- Integer permet de représenter des valeurs entières et fournit des méthodes pour effectuer des opérations arithmétiques, des conversions de chaînes, etc.

**Double :**
- Type primitif correspondant : double
- Double permet de représenter des valeurs décimales en double précision et fournit des méthodes similaires à Integer pour les opérations arithmétiques, les conversions de chaînes, etc.

Chaque instance de ces classes d'emballage enveloppe un seul objet de type primitif. Par exemple, si vous avez besoin de stocker un entier dans une collection Java qui accepte uniquement des objets (comme ArrayList), vous pouvez utiliser la classe d'emballage Integer pour envelopper votre entier. De même, si vous souhaitez utiliser des méthodes spécifiques aux objets sur un type primitif, vous pouvez utiliser la classe d'emballage correspondante pour cela. En Java, grâce à l'autoboxing et au unboxing, vous pouvez souvent passer de façon transparente entre les types primitifs et leurs classes d'emballage correspondantes sans avoir à effectuer explicitement la conversion.