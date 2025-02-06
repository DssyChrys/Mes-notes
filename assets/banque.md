### **Réponse à la question 1 :**
La méthode `virerVers(int montant, Compte destination)` permet d'effectuer un virement d'un compte à un autre.
* Elle **retire** d'abord le montant du compte actuel (`this.retirer(montant)`).
* Ensuite, elle **dépose** ce montant sur le compte `destination` (`destination.deposer(montant)`).
* **Nombre de comptes impliqués :** 2 (le compte source et le compte destination).
### **Réponse à la question 2 :**
Voici la classe `Compte` modifiée pour inclure le **nom du titulaire**, un **constructeur** et une **méthode d'affichage améliorée** :
using System;
class Compte
{
    private string titulaire;
    private int solde;
```
// Constructeur
public Compte(string titulaire)
{
    this.titulaire = titulaire;
    this.solde = 0;
}

public void Deposer(int montant)
{
    solde += montant;
}

public void Retirer(int montant)
{
    solde -= montant;
}

public void VirerVers(int montant, Compte destination)
{
    this.Retirer(montant);
    destination.Deposer(montant);
}

public void Afficher()
{
    Console.WriteLine($"Titulaire: {titulaire}, Solde: {solde}");
}
```
}
class Program
{
    static void Main()
    {
        Compte compte1 = new Compte("Alice");
        Compte compte2 = new Compte("Bob");
```
    compte1.Deposer(500);
    compte1.VirerVers(200, compte2);
    
    compte1.Afficher(); // Titulaire: Alice, Solde: 300
    compte2.Afficher(); // Titulaire: Bob, Solde: 200
}
```
}
### **Modifications apportées :**
1. Ajout de l'attribut `titulaire` (nom du propriétaire du compte).
1. Création d'un **constructeur** pour initialiser `titulaire` et `solde`.
1. Modification de la méthode `Afficher()` pour inclure le **nom du titulaire**.
1. Ajout d'un programme de test dans `Main()` pour illustrer le fonctionnement.

