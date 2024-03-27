## DEFINITION DE CERTAINS TERMES JAVA :

**Classe abstraite :**

- Une classe abstraite en Java est une classe qui ne peut pas être instanciée directement. Elle sert de modèle pour d'autres classes qui en héritent, appelées classes concrètes. Une classe abstraite peut contenir des méthodes abstraites (déclarées mais non implémentées) ainsi que des méthodes concrètes (avec une implémentation). Les méthodes abstraites doivent être implémentées par les classes filles. Une classe abstraite est déclarée avec le mot-clé abstract

**Ramasse-miettes (Garbage Collector) :**

- Le ramasse-miettes est un composant du système d'exécution Java responsable de la gestion automatique de la mémoire. Son rôle est de récupérer la mémoire des objets qui ne sont plus référencés par le programme en cours d'exécution, libérant ainsi la mémoire non utilisée. Cela évite les fuites de mémoire et permet aux développeurs de se concentrer sur la logique de leur programme sans avoir à gérer manuellement la mémoire allouée et désallouée.

**Autoboxing :**

- L'autoboxing est un mécanisme introduit dans Java qui automatise la conversion entre les types primitifs et leurs classes d'emballage correspondantes. Par exemple, il permet à un programmeur de stocker automatiquement une valeur entière dans un objet **Integer** sans nécessiter une conversion explicite. De même, lors de l'extraction de valeurs à partir de collections (par exemple, `ArrayList<Integer>`..), Java convertira automatiquement les objets Integer en types primitifs **int** si nécessaire.

**Sérialisation :**

- La sérialisation en Java est le processus de conversion d'un objet en une séquence d'octets qui peuvent être facilement sauvegardés sur un support de stockage ou transmis sur un réseau. Cette séquence d'octets peut être ensuite reconstruite pour reconstituer l'objet d'origine. La sérialisation est utilisée pour la persistance d'objets (sauvegarde dans des fichiers ou des bases de données) ou pour la communication entre des applications distribuées. En Java, pour qu'un objet soit sérialisable, sa classe doit implémenter l'interface **Serializable**.
