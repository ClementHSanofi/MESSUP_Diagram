# MESSUP - Endpoints

## 🔐 Authentification

| Méthode | Endpoint              |  Description                         |
|---------|-----------------------|--------------------------------------|
| POST    | `api/auth/login`      | Login (Redirection Azure AD)         |
| POST    | `api/auth/logout`     | Logout                               |
| POST    | `api/auth/token`      | Rafraîchit le token                  |

## 👥 Utilisateurs

| Méthode | Endpoint                        | Description                                     |
|---------|---------------------------------|-------------------------------------------------|
| GET     | `api/users`                     | Liste des utilisateurs                          |
| GET     | `api/users/{id}`                | Détail d’un utilisateur                         |
| GET     | `api/users/me`                  | Détail de l’utilisateur connecté                |
| GET     | `api/users/{id}/tickets`        | Liste des tickets de l’utilisateur connecté     |

## 📋 Tickets

| Méthode | Endpoint                                         | Description                       |
|---------|--------------------------------------------------|-----------------------------------|
| GET     | `api/tickets`                                     | Liste des tickets                |
| GET     | `api/tickets/{id}`                                | Détail d'un tickets              |
| POST    | `api/tickets`                                     | Créer un nouveau ticket          |
| PUT     | `api/tickets/{id}`                                | Modifier un ticket               |
| DELETE  | `api/tickets/{id}`                                | Supprimer un ticket (Archivage)  |
| PATCH   | `api/tickets/{id}/status`                         | Change le status d'un ticket     |
| PATCH   | `api/tickets/{id}/priority`                       | Marque comme prioritaire         |
| PATCH   | `api/tickets/{id}/assign`                         | Assigne le ticket  un utilisateur|
| PATCH   | `api/tickets/{id}/reject`                         | Rejeter un ticket                |
| GET     | `api/tickets?status=receptionne&assigned_to=5`    | Exemple de filtre                |
| GET     | `api/tickets?product_id=1&line_id=3`              | Exemple de filtre                |
| GET     | `api/tickets?search=name&created_after=2025-01-01`| Exemple de filtre                |
| GET     | `api/tickets/my-tickets`                          | Mes tickets                      |
| GET     | `api/tickets/assign-to-me`                        | Mes tickets assignés             |
| GET     | `api/tickets/priority`                            | Voirs tickets prioritaires       |

## 💬 Commentaires
| Méthode | Endpoint                     | Description                            |
|---------|------------------------------|----------------------------------------|
| GET     | `api/tickets/{id}/comments`  | Récupérer les commentaires d'un ticket |
| POST    | `api/tickets/{id}/comments`  | Ajouter un commentaire à un ticket     |
| DELETE  | `api/comments/{id}`          | Supprimer un commentaire (admin)       |