```mermaid
graph LR

    subgraph Gestion des livraisons
        CL[Créer une livraison]
        MC[Consulter livraison]
        ML[Modifier livraison]
        AT[Ajouter tickets]
        CGS[Changer statut]
    end

    subgraph Gestion des tickets
        CT[Créer un ticket]
        VT[Consulter ses tickets]
        VTS[Consulter liste des tickets]
        PJ[Joindre fichier]
        AC[Ajouter commentaire]
        MT[Modifier ticket]
        AST[Assigner ticket]
        PL[Planifier livraison]
        CLT[Clôturer ticket]
        AM[Analyse MES]
    end

    subgraph Gestion admin
        GU[Gérer utilisateurs]
        HS[Consulter historique]
    end
    actorUP((Utilisateur))
    actorSM((Support MES))
    actorAD((Administrateur))

    
   %% Héritage simulé
    actorSM -->|hérite de| actorUP
    actorAD -->|hérite de| actorSM

    %% Utilisateur
    actorUP --> CT
    actorUP --> VT
    actorUP --> AC
    actorUP --> PJ

    %% Support MES - Tickets
    actorSM --> MT
    actorSM --> AST
    actorSM --> VTS
    actorSM --> PL
    actorSM --> CLT
    actorSM --> AM

    %% Support MES - Livraisons
    actorSM --> CL
    actorSM --> MC
    actorSM --> ML
    actorSM --> AT
    actorSM --> CGS

    %% Administrateur
    actorAD --> GU
    actorAD --> HS