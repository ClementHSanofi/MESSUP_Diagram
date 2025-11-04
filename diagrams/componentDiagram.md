```mermaid
graph TD
    
    subgraph Utilisateur
        Client["Client Web (Navigateur)"]
    end

    subgraph Frontend [Frontend]
        UI["Interface utilisateur (React + Vite)"]
    end

    subgraph Backend [Backend]
        API["API REST (FastAPI)"]
        Auth["Service Authentification (Azure AD)"]
        Mailer[Service de notification par mail]
    end

    subgraph Database [Base de données]
        DB[(PostgreSQL)]
    end

    Client --> UI
    UI --> API
    API -- Communication avec ORM SQLAlchemy --> Database 
    API --> Auth
    API --> Mailer