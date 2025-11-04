```mermaid 
stateDiagram-v2
    [*] --> Réceptionné: Création ticket

    Réceptionné --> Analysé: Demande complète
    Réceptionné --> À_compléter: Besoin clarification

    À_compléter --> Analysé: Informations fournies
    À_compléter --> Rejeté: Non recevable

    Analysé --> En_cours: Début traitement
    Analysé --> Rejeté: Non applicable

    En_cours --> Clôturé: Livraison effectuée
    En_cours --> À_compléter: Besoin info supplémentaire

    Clôturé --> [*]
    Rejeté --> [*]

    note right of Analysé
        Association à une livraison
        (ID + version)
    end note

    note right of En_cours
        Développement et
        tests en cours
    end note