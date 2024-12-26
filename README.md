# Convention de Nommage Home Assistant

## Objectif

Ce guide définit une méthodologie claire pour standardiser la configuration de Home Assistant, simplifiant la gestion et l'évolution du système. En établissant des conventions de nommage uniformes pour les entités, automatisations et scripts, il vise à rendre la configuration plus lisible, cohérente et maintenable.

### Principes Directeurs
- **Lisibilité** : Les noms doivent être clairs, explicites et faciles à comprendre pour tous les utilisateurs.
- **Cohérence** : Une structure uniforme doit être appliquée pour garantir une logique homogène dans l'ensemble du système.
- **Clarté** : Chaque élément doit indiquer clairement sa fonction, son contexte et son objectif.
- **Extensibilité** : Les conventions doivent permettre des ajouts futurs sans compromettre la structure existante.

## 1. Structure Générale

### 1.1 Entités
TBD

### 1.2 Automatisations
- **Format** : `[Catégorie] - [Action] - [Cible] - [texte libre] - [Déclencheur]`
- **Exemples** :
  - `Confort - Allumer eclairage couloir sur mouvement` : Allume les lumières du couloir lorsqu'un mouvement est détecté.
  - `Confort - Regler poele en absence` : Régle le poele en mode absent
  - `Confort - Désactiver arrosage jardin si pluie detectée` : Désactive l'arrosage du jardin lorsqu'il pleut.

### 1.3 Scripts
TBD

## 2. Éléments de la convention de nommage
### 2.1 Catégories (Automatisations et Scripts)
Identifie le domaine fonctionnel principal de l’automatisation.

- **Liste standardisée des catégories** :
  - **Confort** : Routines liées à l’éclairage, à la température, ou à d'autres éléments de confort.
  - **Sécurité** : Alarmes, serrures, caméras, et détection d’intrusion.
  - **Énergie** : Automatisations visant l’économie d’énergie et la gestion des ressources.
  - **Technique** : Pour les ellements internes servant au bon fonctionnement de home assistant

  Le prefix _Dev ou _Tst peuvent être utiliser pour les automatisations en cours de developpement

### 2.2 Action/Scénario (Obligatoire)
Décrit ce que fait l’automatisation. Cette section doit être descriptive mais concise.

- **Liste standardisée pour les actions** :
  - `Allumer`
  - `Éteindre`
  - `Régler`
  - `Activer`
  - `Désactiver`
  - `Synchroniser`
  - `Réinitialiser`
  - `Detecter`
  - `Suivre`
  - `Lancer` 

### 2.3 Cible
Précise la localisation ou le contexte dans lequel l’automatisation s’applique.
- **Une entité spécifique** :
  - `Salon`, `Chambre`, `Cuisine`, `Salle_de_bain`, `Garage`, `Jardin`, `Entrée`, `Extérieur`.
- **Une Zone** :
  - `Maison`, `RDC`, `Cuisine`, `WC`,`Couloir`,`Buanderie`,`SDB`,  `Extérieur`, `Toutes_zones`.


### 2.4 Déclencheur
Identifie la condition ou l’événement qui active l’automatisation.

- **Liste standardisée pour les déclencheurs basés sur des capteurs** :
  - `Sur_mouvement` : Mouvement détecté par un capteur PIR.
  - `Sur_ouverture` : Ouverture d’une porte ou d’une fenêtre détectée.
  - `Sur_detection` : Autres types de detection
  - `Sur_température` : Une température spécifique est atteinte.
  - `Sur_qualité_air` : Détection d’une mauvaise qualité de l’air.

- **Liste standardisée pour les déclencheurs temporels** :
  - `Au_coucher_soleil` : Basé sur le coucher du soleil.
  - `Au_levé_soleil` : Basé sur le lever du soleil.
  - `Planifié` : Programmation à une heure précise ou déclenchement périodique.

- **Liste standardisée pour les déclencheurs liés à la présence ou l’état** :
  - `En_absence` : Lorsque personne n’est détecté dans la maison.
  - `En_présence` : Lorsque quelqu’un est détecté.
  - `Sur_mode_vacances` : Lorsque le mode "vacances" est activé.
  - `Sur_mode_nuit` : Lorsqu’un mode nuit est activé.

- **Liste standardisée pour les déclencheurs spécifiques aux appareils** :
  - `Sur_appareil_on` : Lorsqu’un appareil est allumé.
  - `Sur_fin_cycle` : Lorsque le cycle d’un appareil est terminé (ex. lave-linge).

### Contexte ou Texte Libre
Le texte "Libre" permet d’ajouter des informations spécifiques ou des précisions non couvertes par les autres parties de la structure.
`Quand l’utiliser:` Si un scénario ou un script nécessite une distinction particulière.



