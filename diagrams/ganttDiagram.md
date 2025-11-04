```mermaid
gantt 
    title Développement application MESSUP v1
    dateFormat DD-MM-YYYY

    section Préparation
        Demande d'accès                     :c1, 22-09-2025, 63d
        Cahier des charges                  :c2, 07-10-2025, 20d
        UML + définition endpoints API      :c3, 27-10-2025, 14d
        Users Stories                       :after c3, 7d
        Maquettage                          :after c4, 31-12-2025
        Mise en place des environnements    :c5, 27-10-2025, 35d

    section Développement 
        Apprentissage Python & FastAPI      :d1, 13-10-2025, 31-12-2025
        Apprentissage TypeScript & React    :d2, 15-11-2025, 31-01-2026
        API                                 :d3, 01-01-2026, 31-03-2026
        Documentation endpoint API          :d4, 01-03-2026, 30d
        FrontEnd                            :d5, 15-03-2026, 31-05-2026
        Documentation utlisateur            :d6, 01-05-2026, 30d
        Documentation technique             :d7, 01-01-2026, 31-05-2026

    section Tests & Validation
        Tests utilisateurs                  :tv1, 01-06-2026, 35d
        Corrections                         :tv2, 08-06-2026, 28d
        Optimisations                       :tv3, 22-06-2026, 14d

    section Déploiement & mise en production
        CI/CD (API)                         :dm1, 01-01-2026, 14d
        CI/CD (Front)                       :dm2, 01-04-2026, 14d
        Mise en production                  :dm3, 06-07-2026, 31-07-2026
        Recettage                           :dm4, 20-07-2026, 31-07-2026