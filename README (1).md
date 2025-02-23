
# Documentation API - TP Node.js

## API Endpoints

### Utilisateur

<details>
  <summary>Enregistrement d'un utilisateur (POST)</summary>

  **URL**: `http://localhost:3000/api/v1/users/register`

  **Body**:
  ```json
  {
    "name": "string",
    "email": "string",
    "password": "string",
    "salle": int (peut être null)
  }
  ```

</details>

<details>
  <summary>Connexion d'un utilisateur (POST)</summary>

  **URL**: `http://localhost:3000/api/v1/users/login`

</details>

<details>
  <summary>Modification des données d'un utilisateur (PUT)</summary>

  **URL**: `http://localhost:3000/api/v1/users/update/{id}`

</details>

<details>
  <summary>Récupérer les données de tous les utilisateurs (GET)</summary>

  **URL**: `http://localhost:3000/api/v1/users/`

</details>

<details>
  <summary>Récupérer les données d'un utilisateur (GET)</summary>

  **URL**: `http://localhost:3000/api/v1/users/{id}`

</details>

<details>
  <summary>Supprimer un utilisateur (DELETE)</summary>

  **URL**: `http://localhost:3000/api/v1/users/delete/{id}`

</details>

### Exemple de réponse

<details>
  <summary>Réponse de l'API pour la création d'un utilisateur (POST)</summary>

  **Réponse réussie**:
  ```json
  {
    "message": "Utilisateur créé avec succès",
    "user": {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com",
      "role": "student",
      "salle": 1,
      "createdAt": "2025-02-23T00:35:37.000Z",
      "updatedAt": "2025-02-23T00:35:37.000Z"
    }
  }
  ```

  **Réponse d'erreur**:
  ```json
  {
    "message": "Cet email existe déjà"
  }
  ```

</details>

### Configuration

<details>
  <summary>Variables d'environnement</summary>

  Assurez-vous d'avoir un fichier `.env` avec les variables suivantes définies :

  ```plaintext
  JWT_KEY=your_secret_key
  DB_HOST=localhost
  DB_USER=your_database_user
  DB_PASSWORD=your_database_password
  DB_NAME=nodedatabase
  ```

</details>

### Exemples d'utilisation avec Postman

<details>
  <summary>Enregistrement d'un utilisateur</summary>

  - **Méthode**: POST
  - **URL**: `http://localhost:3000/api/v1/users/register`
  - **Body**: 
    ```json
    {
      "name": "John Doe",
      "email": "john@example.com",
      "password": "password123",
      "salle": 1
    }
    ```

</details>

<details>
  <summary>Connexion d'un utilisateur</summary>

  - **Méthode**: POST
  - **URL**: `http://localhost:3000/api/v1/users/login`
  - **Body**:
    ```json
    {
      "email": "john@example.com",
      "password": "password123"
    }
    ```

</details>

### Structure du projet

<details>
  <summary>Arborescence des fichiers</summary>

  Voici la structure de base du projet :

  ```
  ├── Controllers
  │   └── UsersController.mjs
  ├── Models
  │   └── UserModel.mjs
  ├── Routes
  │   └── UsersRoutes.mjs
  ├── .env
  └── server.js
  ```

</details>

