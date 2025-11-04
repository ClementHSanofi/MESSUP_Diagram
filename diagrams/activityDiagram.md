```mermaid
flowchart TD
Start([Début]) --> Create[Utilisateur crée un ticket]
Create --> Notify1[Notification Support MES]
Notify1 --> Review{Revue initiale}

Review -->|Incomplet| Clarify[Demande clarification]
Clarify --> Wait[Attente réponse utilisateur]
Wait --> Response[Utilisateur répond]
Response --> Review

Review -->|Complet| Analyze[Analyse et évaluation du ticket]
Analyze --> Associate[Association à une livraison]
Associate --> Plan{Planification}

Plan -->|Urgent| Priority[Traitement prioritaire]
Plan -->|Normal| Queue[File d'attente normale]

Priority --> Dev[Développement]
Queue --> Dev

Dev --> Test[Tests]
Test --> Deploy{Déploiement OK?}

Deploy -->|Non| Dev
Deploy -->|Oui| Deploy2(Déploiement)

Deploy2 --> Fin([Fin])