```mermaid
sequenceDiagram
participant U as Utilisateur
participant F as Frontend
participant B as Backend
participant BDD as Base de donnée


U->>F: Soumet un ticket
F->>B: Envoie les données du ticket
B->>BDD: Enregistre le ticket
BDD-->>B: Confirmation d'enregistrement
B-->>F: Réponse OK
F-->>U: Ticket créé avec succès
