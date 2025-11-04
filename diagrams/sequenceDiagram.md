```mermaid
sequenceDiagram
participant U as Utilisateur@{ "type" : "actor" }
participant F as Frontend@{ "type" : "boundary" }
participant B as Backend@{ "type" : "control" }
participant BDD as Base de donnée@{ "type" : "database" }


U->>F: Soumet un ticket
F->>B: Envoie les données du ticket
B->>BDD: Enregistre le ticket
BDD-->>B: Confirmation d'enregistrement
B-->>F: Réponse OK
F-->>U: Ticket créé avec succès
