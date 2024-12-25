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
- **Format** : `[Type de Dispositif] - [Zone] - [Fonction/Identifiant Spécifique]`
- **Exemples** :
  - `sensor_sejour_temperature` : Capteur mesurant la température dans le séjour.
  - `light_chambre_principale` : Lumière principale dans la chambre.
  - `camera_exterieur_surveillance` : Caméra de surveillance extérieure.

### 1.2 Automatisations
- **Format** : `[Action] - [Catégorie] - [Zone / Entité] - [Texte Libre]`
- **Exemples** :
  - `Allumer - Eclairage - Couloir - si mouvement` : Allume les lumières du couloir lorsqu'un mouvement est détecté.
  - `Regler - cvc - poele - sur mode absent` : Régle le poele en mode absent
  - `Désactiver - Arrosage - Jardin - si pluie detectée` : Désactive l'arrosage du jardin lorsqu'il pleut.

### 1.3 Scripts
- **Format** : `[Zone] - [Catégorie] - [Action] - [Contexte ou Texte Libre]`
- **Exemples** :
  - `chambre_eclairage_diminuer_soiree` : Diminue la luminosité des lumières dans la chambre pour une ambiance soirée.
  - `salon_multimedia_lancer_homecinema_film` : Lance une configuration home cinéma pour regarder un film.
  - `jardin_exterieur_arreter_arrosage_urgence` : Arrête l'arrosage dans le jardin en cas d'urgence.

## 2. Éléments de la convention de nommage

### 2.1 Types de Dispositifs (Entités)
- `sensor_` : Capteurs (température, humidité, mouvement, etc.).
- `switch_` : Interrupteurs.
- `light_` : Lumières.
- `camera_` : Caméras.

### 2.2 Zones
- `maison`
- `cuisine`
- `sejour`
- `garage`
- `salledebain`
- `jardin`
- `chambre`

### 2.3 Catégories (Automatisations et Scripts)
- `eclairage` : Éclairage (allumage, extinction, ajustement de luminosité).
- `securite` : Sécurité (alarmes, verrouillage).
- `cvc` : Chauffage, ventilation et climatisation.
- `notifications` : Alertes et messages envoyés aux utilisateurs.
- `multimedia` : Systèmes audio et vidéo.
- `exterieur` : Gestion extérieure, comme l’arrosage ou les équipements de jardin.

### 2.4 Déclencheurs ou Conditions (Automatisations)
- `mouvement` : Détection de mouvement.
- `planifié` : Déclenchement à une heure ou date planifiée.
- `presence` : Basé sur la présence ou l'absence d’une personne.
- `temperature` : Variation de température.
- `pluie` : Détection de pluie ou météo.

### 2.5 Actions
- `allumer` : Activer une lumière ou un dispositif.
- `eteindre` : Désactiver une lumière ou un dispositif.
- `verrouiller` : Verrouiller une porte ou un mécanisme.
- `diminuer` : Réduire une valeur (ex. luminosité, température).
- `augmenter` : Augmenter une valeur.
- `notifier` : Envoyer une notification.
- `activer` : Lancer une action ou un système.
- `arreter` : Arrêter une action ou un système.

### Contexte ou Texte Libre
Le texte "Libre" permet d’ajouter des informations spécifiques ou des précisions non couvertes par les autres parties de la structure.
`Quand l’utiliser:` Si un scénario ou un script nécessite une distinction particulière.
Exemple :
- Eteindre - Éclairage - Salon - Pendant les vacances (Pour un scénario spécifique aux vacances.)
- Régler - CVC - Bureau - pour l'Hiver (Pour un réglage saisonnier précis.)


