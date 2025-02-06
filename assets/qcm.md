### 1. Quel est le point d'entrée dans une application console en C# ?
**Réponse :** La méthode `Main`**Explication :** En C#, le point d'entrée d'une application console est toujours la méthode `Main()`. Elle doit être déclarée comme `static` et peut accepter un tableau de chaînes de caractères (`string[] args`) en paramètre.
### 2. Laquelle des affirmations suivantes est vraie concernant les exceptions en C# ?
**Réponse :** **c - Les 2 ci-dessusExplication :**
* En C#, toutes les classes d'exception héritent directement ou indirectement de `System.Exception`.
* Les exceptions sont représentées par des classes.
### 3. Quel sera le résultat du programme suivant ?
             {
 	                 public static void Main(){
 	                      	Employee emp = new Employee();
 	                      	Console.Writeline(emp.salary);
 	                 }
              }
**Réponse :** **0 Explication :** En C#, les champs de type `int` sont initialisés par défaut à `0`. Comme `salary` n'est pas initialisé, il prend la valeur par défaut.
### 4. Quel mot-clé permet de déclarer une variable dont le type sera automatiquement déterminé par le compilateur en C# ?
**Réponse :** `var`     **Explication :** Le mot-clé `var` permet de déclarer une variable sans spécifier son type explicite, celui-ci étant déduit du contexte.
### 5. Quel est le modificateur par défaut d'un espace de nom en C# ?
**Réponse :** **`internal`****      ****Explication :** Un espace de nom (namespace) n'a pas de modificateur d'accès propre. Toutefois, les classes à l'intérieur d'un namespace ont par défaut le modificateur `internal`, ce qui signifie qu'elles sont accessibles uniquement dans l'assembly actuel.
### 6. Quel est le modificateur d'accès par défaut des membres d'une classe en C# ?
**Réponse :** **private   Explication :** Par défaut, les membres d'une classe sont `private`, sauf indication contraire.
### 7. Que manque-t-il à la définition de la classe suivante pour que la compilation réussisse ?
**Réponse :** **b - class       Explication :** Une classe doit être déclarée avec le mot-clé `class`, par exemple :
### 8. Le code suivant sera-t-il compilé ?
                     public class @class{}
**Réponse :** **a - Oui         Explication :** En C#, `@` permet d'utiliser un mot réservé (`class` ici) comme identificateur. Ainsi, `@class` est un nom de classe valide.
### 9. Un constructeur peut-il avoir un type de retour ?
**Réponse :** **b - Non       Explication :** Un constructeur ne peut pas avoir de type de retour, même `void`. Son rôle est uniquement d'initialiser l'objet.
### 10. Un constructeur peut-il avoir un nom différent du nom de la classe ?
**Réponse :** **b - Non       Explication :** Un constructeur doit toujours porter le même nom que la classe.
### 11. Laquelle des affirmations suivantes est vraie ?
**Réponse :** **c - Le constructeur ne peut retourner aucune valeur         Explication :** Un constructeur ne retourne jamais de valeur, ni explicitement ni implicitement.
### 12. Quelle est la propriété auto-implémentée dans l'extrait de code ci-dessous ?
                public class Person
      { 
              int Id = 0; 
              public string Name (get; set; } 
              private int_age: 
              public int Age 
              { 
              	get (return_age:) 
              	set (age = value; } 
              }
      	}      
**Réponse :** **b - Name           Explication :** Une propriété auto-implémentée est une propriété avec `{ get; set; }` sans champ sous-jacent explicite. Ici, seule `Name` est une propriété auto-implémentée.
