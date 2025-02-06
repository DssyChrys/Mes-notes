### **Classes principales :**
1. **Liquide**
	1. **Attributs :**
		1. Nom (string) → ex. "Rhum", "Jus d'orange"
		1. Alcoolisé (bool) → Indique si le liquide est alcoolisé
	1. **Méthodes :**
		1. AfficherDetails() → Affiche les informations du liquide
1. **Bouteille**
	1. 
		**Attributs :**
		1. LiquideContenu (Liquide)
		1. VolumeTotal (double) → Capacité totale de la bouteille (ex. 1L)
		1. VolumeRestant (double) → Quantité restante
	1. 
		**Méthodes :**
		1. Verser(double quantité, Shaker shaker) → Verse une quantité dans un shaker
		1. EstVide() → Vérifie si la bouteille est vide
1. **Shaker**
	1. 
		**Attributs :**
		1. ContenanceMax (double) → Capacité du shaker (ex. 0.5L)
		1. Contenu (Dictionnaire<Liquide, double>) → Stocke les liquides et leurs quantités
	1. 
		**Méthodes :**
		1. AjouterLiquide(Liquide liquide, double quantité) → Ajoute un liquide dans le shaker
		1. Secouer() → Mélange le contenu
		1. Vider() → Vide le contenu (simule le service du cocktail)
		1. Laver() → Nettoie le shaker
1. **Recette**
	1. 
		**Attributs :**
		1. Nom (string) → ex. "Mojito"
		1. Proportions (Dictionnaire<Liquide, double>) → Associe chaque liquide à une proportion
	1. 
		**Méthodes :**
		1. PréparerCocktail(double quantitéTotale, List<Bouteille> bouteilles, Shaker shaker) → Suit la recette en versant les bons liquides dans le shaker selon la proportion
1. **Bar**
	1. 
		**Attributs :**
		1. Bouteilles (Liste) → Stocke toutes les bouteilles disponibles
		1. Shakers (Liste) → Stocke les shakers disponibles
		1. Recettes (Liste) → Stocke toutes les recettes
	1. 
		**Méthodes :**
		1. PréparerCocktail(string nomRecette, double quantité) → Recherche la recette et appelle PréparerCocktail()
		1. AfficherStock() → Affiche l’état des bouteilles et des shakers
### **Résumé du fonctionnement :**
1. Le **bar** contient des **bouteilles**, des **shakers**, et des **recettes**.
1. On choisit une **recette** et une quantité souhaitée.
1. On verse les liquides dans un **shaker** en respectant les proportions.
1. On **secoue** le shaker.
1. On **vide** le shaker pour servir le cocktail.
1. On **lave** le shaker après usage



ENONCE
	Exercice1 (Spts) 
	Cet exercice a pour but de réfléchir sur la conception d'un programme, sa structuration en classes. Il ne s'agit pas pour le moment de réaliser ce programme, mais juste de concevoir son architecture. 
	On fait des cocktails avec différents liquides (alcools, sodas, jus de fruits). On a un bar avec des bouteilles qui peuvent être pleines ou à moitié vides. On a des shakers qui ont une contenance donnée.
	 Il y a des recettes de cocktails qui indiquent seulement les proportions. Ces recettes peuvent s'appliquer à des quantités plus ou moins grandes selon les besoins du moment. 
	Les cocktails se font en déversant une partie du contenu des bouteilles dans des shakers. 
	Après, il faut secouer. Les shakers sont ensuite vidés (dans les verres, mais on ne tiendra pas compte des verres dans cette application). Il faut les laver après usage. 

	Question: quelles classes faut-il créer ? Quelles informations faut-il dans chaque classe ? 
	Quelles méthodes faut-il écrire, et dans quelle classe les mettre?

