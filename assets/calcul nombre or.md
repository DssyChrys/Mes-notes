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

