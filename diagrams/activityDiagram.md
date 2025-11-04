```mermaid
flowchart TD
    Start([Start])
    Step1[Étape 1 : Créer ticket]
    Step2[Étape 2 : Analyse ticket]
    Decision{Ticket complet ?}
    Step3[Étape 3 : Traitement]
    Step4[Étape 4 : Livraison]
    End([Fin])

    Start --> Step1 --> Step2 --> Decision
    Decision -- Oui --> Step3 --> Step4 --> End
    Decision -- Non --> Step1