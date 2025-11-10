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

| Méthode | Endpoint                                          | Description                        |
|---------|---------------------------------------------------|------------------------------------|
| GET     | `api/tickets`                                     | Liste des tickets                  |
| GET     | `api/tickets/{id}`                                | Détail d'un tickets                |
| POST    | `api/tickets`                                     | Créer un nouveau ticket            |
| PUT     | `api/tickets/{id}`                                | Modifier un ticket                 |
| DELETE  | `api/tickets/{id}`                                | Supprimer ticket (admin &rchivage) |
| PATCH   | `api/tickets/{id}/status`                         | Change le status d'un ticket       |
| PATCH   | `api/tickets/{id}/priority`                       | Marque comme prioritaire           |
| PATCH   | `api/tickets/{id}/assign`                         | Assigne le ticket  un utilisateur  |
| PATCH   | `api/tickets/{id}/reject`                         | Rejeter un ticket                  |
| GET     | `api/tickets?status=receptionne&assigned_to=5`    | Exemple de filtre                  |
| GET     | `api/tickets?product_id=1&line_id=3`              | Exemple de filtre                  |
| GET     | `api/tickets?search=name&created_after=2025-01-01`| Exemple de filtre                  |
| GET     | `api/tickets/my-tickets`                          | Mes tickets                        |
| GET     | `api/tickets/assign-to-me`                        | Mes tickets assignés               |
| GET     | `api/tickets/priority`                            | Voirs tickets prioritaires         |

## 💬 Commentaires
| Méthode | Endpoint                     | Description                                    |
|---------|------------------------------|------------------------------------------------|
| GET     | `api/tickets/{id}/comments`  | Récupérer les commentaires d'un ticket         |
| POST    | `api/tickets/{id}/comments`  | Ajouter un commentaire à un ticket             |
| DELETE  | `api/comments/{id}`          | Supprimer un commentaire (admin & archivage)   |

## 💥 Impact
| Méthode | Endpoint                               | Description                            |
|---------|----------------------------------------|----------------------------------------|
| GET     | `api/tickets/{id}/impact`              | Récupérer les impacts d'un ticket      |
| POST    | `api/tickets/{id}/impact`              | Ajouter un impact à un ticket          |
| DELETE  | `api/ticket/{id}/impact/{impact_id}`   | Retirer un impact d'un ticket          |

## 📎Pièces jointes
| Méthode | Endpoint                        | Description                              |
|---------|---------------------------------|------------------------------------------|
| GET     | `api/tickets/{id}/attachments`  | Récupérer les pièces jointes d'un ticket |
| POST    | `api/tickets/{id}/attachments`  | Ajouter une pièce jointe à un ticket     |
| GET     | `api/attachments/{id}/download` | Télécharger une pièce jointe             |
| DELETE  | `api/attachments/{id}`          | Supprimer une pièce jointe (admin?)      |

## 📊 Analyse
| Méthode | Endpoint                        | Description                              |
|---------|---------------------------------|------------------------------------------|
| GET     | `api/tickets/{id}/analysis`     | Récupérer l'analyse d'un ticket          |
| POST    | `api/tickets/{id}/analysis`     | Ajouter l'analyse d'un ticket            |
| PUT     | `api/analysis/{id}`             | Modifier l'analyse d'un ticket           |
| POST    | `api/analysis/{id}/flag`        | Ajouter un flag à une analyse            |
| PUT     | `api/analysis/{id}/flag`        | Modifier un flag à une analyse           |

## 📦 Livraisons

| Méthode | Endpoint                                    | Description                              |
|---------|---------------------------------------------|------------------------------------------|
| GET     | `api/deliveries`                            | Récupérer la liste des livraisons        |
| GET     | `api/deliveries/{id}`                       | Détail d'une livraison                   |
| POST    | `api/deliveries`                            | Créer une livraison                      |
| PUT     | `api/deliveries/{id}`                       | Modifier une livraison                   |
| DELETE  | `api/deliveries/{id}`                       | Supprimer livraison (admin & archivage)  |
| GET     | `api/deliveries/{id}/tickets`               | Récupérer les tickets d'une livraison    |
| POST    | `api/deliveries/{id}/tickets`               | Associer des tickets à une livraison     |
| DELETE  | `api/deliveries/{id}/tickets/{ticket_id}`   | Retirer un ticket d'une livraison        |
| PATCH   | `api/deliveries/{id}/status`                | Mettre à jour le status d'un ticket      |
| PATCH   | `api/deliveries/{id}/deploy`                | Définir comme déployée                   |

## 📜 Historique

| Méthode | Endpoint                        | Description                              |
|---------|---------------------------------|------------------------------------------|
| GET     | `api/tickets/{id}/history`      | Récupérer l'historique d'un ticket       |
| GET     | `api/delivery/{id}/history`     | Récupérer l'historique d'une livraison   |
| GET     | `api/history/{id}`              | Détail d'une entrée d'historique         |

## 🎯 Objets MES

| Méthode | Endpoint                        | Description                              |
|---------|---------------------------------|------------------------------------------|
| GET     | `api/object`                    | Récupérer la liste des objets            |
| GET     | `api/object{id}`                | Détail d'un objet                        |
| POST    | `api/object`                    | Créer un objet                           |
| PUT     | `api/object/{id}`               | Modifier un objet                        |
| GET     | `api/object/{id}/deliveries`    | Liste des livraisons lié à un objet      |
| DELETE  | `api/object/{id}`               | Supprimer un objet (admin & archivage)   |

## Feedback
| Méthode | Endpoint                     | Description                                  |
|---------|------------------------------|----------------------------------------------|
| GET     | `api/feedback`               | Récupérer la liste des feedback              |
| GET     | `api/tickets/{id}/feedback`  | Feedback d'un tickets                        |
| GET     | `api/users/{id}/feedback`    | Feedback des ticket résolu par un membre MES |
| POST    | `api/tickets/{id}/feedback`  | Ajouter un feedback                          |

## 📊 Reporting & Statistiques
<!-- TODO A définir -->
| Méthode | Endpoint                                 | Description                          |
|--------|-------------------------------------------|--------------------------------------|
| GET    | `/api/stats/tickets-by-status`            | Répartition par statut               |
| GET    | `/api/stats/tickets-by-product`           | Répartition par produit              |
| GET    | `/api/stats/tickets-by-line`              | Répartition par ligne                |
| GET    | `/api/stats/average-resolution-time`      | Temps moyen de résolution            |
| GET    | `/api/stats/workload`                     | Charge de travail par utilisateur    |
| GET    | `/api/stats/deliveries`                   | Statistiques des livraisons          |

## 📤 Export

| Méthode | Endpoint                                                  | Description     |
|--------|------------------------------------------------------------|-----------------|
| GET    | `/api/reports/tickets/export?format=excel`                 | Export Excel    |
| GET    | `/api/reports/tickets/export?format=pdf`                   | Export PDF      |

## 🏷️ Données de référence

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/products`                | Liste des produits                |
| POST   | `api/products`                | Créer un produit (admin)          |
| PUT    | `api/products/{id}`           | Modifier un produit (admin)       |

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/lines`                   | Liste des lignes                  |
| POST   | `api/lines`                   | Créer une ligne (admin)           |
| PUT    | `api/lines/{id}`              | Modifier une ligne (admin)        |

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/roles`                   | Liste des rôles                   |

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/departments`             | Liste des départements            |
| POST   | `api/departments`             | Créer un départements             |
| PUT    | `api/departments/{id}`        | Modifier un départements (admin)  |

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/ticket-sources`          | Liste des sources de ticket       |
| POST   | `api/ticket-sources`          | Créer une sources de ticket       |
| PUT    | `api/ticket-sources/{id}`     | Modifier une sources de ticket    |

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/modification-types`      | Liste des types de modification   |
| POST   | `api/modification-types`      | Créer un type de modification     |
| PUT    | `api/modification-types/{id}` | Modifier un type de modification  |

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/object-types`            | Liste des types d'objet           |
| POST   | `api/object-types`            | Créer un type d'objet             |
| PUT    | `api/object-types/{id}`       | Modifier un type d'objet          |

| Méthode | Endpoint                     | Description                       |
|--------|-------------------------------|-----------------------------------|
| GET    | `api/impact-types`            | Liste des types d'impact          |
| POST   | `api/impact-types`            | Créer un type d'impact            |
| PUT    | `api/impact-types/{id}`       | Modifier un type d'impact         |

## 🔧 Administration

| Méthode | Endpoint                          | Description                      |
|--------|------------------------------------|----------------------------------|
| POST   | `/api/admin/users`                 | Créer un utilisateur             |
| PUT    | `/api/admin/users/{id}`            | Modifier un utilisateur          |
| DELETE | `/api/admin/users/{id}`            | Désactiver un utilisateur        |
| PATCH  | `/api/admin/users/{id}/role`       | Changer le rôle                  |
| GET    | `/api/admin/config`                | Configuration système            |
| PUT    | `/api/admin/config`                | Modifier la configuration        |

## 🔗 Intégrations externes 
<!-- TODO  Azure & Veeva-->

