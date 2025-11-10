# 📋 User Stories - Application de Support MES

## 👤 Utilisateur

### Création et suivi des tickets

**US-01** : En tant qu'utilisateur, je veux pouvoir créer un ticket pour signaler une anomalie dans un dossier de lot électronique.

**US-02** : En tant qu'utilisateur, je veux pouvoir joindre des captures d'écran à mon ticket pour illustrer le problème rencontré.

**US-03** : En tant qu'utilisateur, je veux pouvoir consulter l'état d'avancement de mes tickets pour suivre leur traitement.

**US-04** : En tant qu'utilisateur, je veux recevoir des notifications lorsque le statut de mon ticket change pour être informé de son évolution.

**US-05** : En tant qu'utilisateur, je veux pouvoir ajouter des commentaires à mes tickets pour apporter des précisions.

**US-06** : En tant qu'utilisateur, je veux pouvoir filtrer mes tickets par statut, date ou priorité pour retrouver facilement une demande.

### Clarification et compléments

**US-07** : En tant qu'utilisateur, je veux être notifié lorsque le support MES demande des informations complémentaires pour pouvoir y répondre rapidement.

**US-08** : En tant qu'utilisateur, je veux pouvoir compléter un ticket marqué "à compléter" pour fournir les informations demandées.

### Consultation

**US-09** : En tant qu'utilisateur, je veux pouvoir consulter l'historique complet d'un ticket pour comprendre son évolution. <!-- TODO Revoir ce qui est non sensible -->

**US-10** : En tant qu'utilisateur, je veux pouvoir voir quand ma demande sera livrée pour planifier mon travail en conséquence.

## 👨‍💻 Support MES

### Gestion des tickets

**US-11** : En tant que support MES, je veux pouvoir visualiser tous les tickets en attente pour organiser mon travail.

**US-12** : En tant que support MES, je veux pouvoir assigner un ticket à un membre de l'équipe pour répartir la charge de travail.

**US-13** : En tant que support MES, je veux pouvoir changer le statut d'un ticket pour refléter son avancement.

**US-14** : En tant que support MES, je veux pouvoir demander des compléments d'information à l'utilisateur lorsque la demande n'est pas claire.

**US-15** : En tant que support MES, je veux pouvoir prioriser certains tickets pour traiter d'abord les plus urgents.

### Analyse et traitement

**US-16** : En tant que support MES, je veux pouvoir documenter l'analyse d'un ticket pour garder une trace des décisions prises.

**US-17** : En tant que support MES, je veux pouvoir associer un ticket à une livraison pour planifier son déploiement.

**US-18** : En tant que support MES, je veux pouvoir catégoriser l'impact MES d'un ticket pour faciliter son traitement.

**US-19** : En tant que support MES, je veux pouvoir évaluer la charge de travail d'un ticket pour mieux planifier les livraisons.

**US-20** : En tant que support MES, je veux pouvoir indiquer si un ticket a un impact qualité pour respecter les exigences réglementaires.

### Livraisons

**US-21** : En tant que support MES, je veux pouvoir créer une livraison pour regrouper plusieurs tickets.

**US-22** : En tant que support MES, je veux pouvoir planifier une date de livraison pour informer les utilisateurs.

**US-23** : En tant que support MES, je veux pouvoir marquer une livraison comme déployée pour clôturer automatiquement les tickets associés.

**US-24** : En tant que support MES, je veux pouvoir documenter les modifications apportées dans une livraison pour assurer la traçabilité.

### Reporting

**US-25** : En tant que support MES, je veux pouvoir visualiser la répartition des tickets par catégorie pour identifier les problèmes récurrents.

**US-26** : En tant que support MES, je veux pouvoir exporter les données des tickets au format Excel pour créer des rapports personnalisés.


### Suivi et planification

**US-27** : En tant que support MES, je veux pouvoir consulter l'ensemble des tickets pour avoir une vision globale des demandes.

**US-28** : En tant que support MES, je veux pouvoir filtrer les tickets par impact pour identifier les évolutions stratégiques.

**US-29** : En tant que support MES, je veux pouvoir consulter le planning des livraisons pour coordonner mon travail.

### Création de tickets

**US-30** : En tant que support MES, je veux pouvoir créer des tickets d'évolution pour améliorer le système MES.

**US-31** : En tant que support MES, je veux pouvoir associer des références GxP à un ticket pour assurer la conformité réglementaire.

## 👮‍♂️ Administrateur

### Gestion des utilisateurs

**US-32** : En tant qu'administrateur, je veux pouvoir gérer les droits des utilisateurs pour contrôler l'accès à l'application.


### Configuration du système

**US-33** : En tant qu'administrateur, je veux pouvoir configurer les catégories de tickets pour adapter l'application aux besoins du site.

**US-34** : En tant qu'administrateur, je veux pouvoir configurer les produits et lignes de production pour refléter l'organisation du site.

**US-35** : En tant qu'administrateur, je veux pouvoir consulter l'historique pour assurer la traçabilité des actions.

## 🔄 Intégrations

### Veeva
<!-- TODO Vérifier -->
**US-36** : En tant qu'utilisateur support MES, je veux pouvoir liée une déviation Veeva à un ticket pour assurer la conformité qualité.

**US-37** : En tant qu'utilisateur, je veux pouvoir consulter le statut d'une déviation Veeva liée à mon ticket pour suivre sa résolution.

### Notifications

**US-38** : En tant qu'utilisateur, je veux recevoir des notifications par email lors des changements importants sur mes tickets.

**US-39** : En tant qu'utilisateur, je veux recevoir une demande de feedback par mail lors de la conclusion de mon ticket afin de donner mon avis.

## 📱 Expérience utilisateur

### Interface

**US-40** : En tant qu'utilisateur, je veux une interface responsive pour pouvoir utiliser l'application sur différents appareils.

**US-41** : En tant qu'utilisateur, je veux un tableau de bord personnalisé affichant mes tickets récents et les actions en attente.

**US-42** : En tant qu'utilisateur, je veux pouvoir rechercher rapidement un ticket par son numéro ou son titre.

**US-43** : En tant qu'utilisateur, je veux une interface intuitive avec des codes couleur pour identifier facilement le statut des tickets.

### Performance

**US-44** : En tant qu'utilisateur, je veux que l'application charge rapidement même avec un grand nombre de tickets.

**US-45** : En tant qu'utilisateur, je veux pouvoir paginer les résultats de recherche pour améliorer les performances.