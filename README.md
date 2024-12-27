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


### 2.4 Condition
#### Note sur la construction d'une condition

La construction d'une condition dans les automatisations repose sur la combinaison de **préfixes**, **conditions unitaires** et **opérateurs logiques** pour exprimer des scénarios simples ou complexes. Cette structure permet de définir précisément les déclencheurs ou les contraintes des automatisations.

#### **Structure générale**
- **Préfixes :** Spécifient le contexte logique ou temporel de la condition (ex. `Si_`, `Dans_`, etc.).
- **Conditions unitaires :** Désignent les états ou événements qui déclenchent ou restreignent l’automatisation (ex. `Mouvement`, `Nuit`, `Vent`).
- **Opérateurs logiques :** Permettent de combiner plusieurs conditions :
  - `_et_` : Les deux conditions doivent être vraies.
  - `_ou_` : Une ou les deux conditions doivent être vraies.

#### Conditions
- `Mouvement` : Mouvement détecté par un capteur PIR.
- `Interrupteur` : Utilisation d’un interrupteur (activé ou désactivé).
- `AccesOuverture` : Changement d’état d’une porte ou d’une fenêtre (ouvert ou fermé).
- `Heure` : Déclenchement basé sur une heure spécifique.
- `Presence` : Présence détectée dans une zone ou à domicile.
- `Absence` : Absence détectée dans une zone ou à domicile.
- `Temperature` : État du capteur de température (ex. supérieure ou inférieure à un seuil).
- `Humidite` : État du capteur d'humidité (ex. supérieure ou inférieure à un seuil).
- `EtatCapteur` : État générique d’un capteur personnalisé (ex. ouvert, fermé, activé, etc.).
- `Nuit` : Exécution limitée à la nuit.
- `Jour` : Exécution limitée au jour.
- `Weekend` : Exécution limitée aux week-ends.
- `JourFerie` : Condition basée sur le jour férié (est ou n'est pas un jour férié).
- `SoleilHaut` : Le soleil est au-dessus de l’horizon.
- `SoleilBas` : Le soleil est en dessous de l’horizon.
- `ChangementDeZone` : Une personne change de zone (entre ou sort d’une zone spécifique).
- `Pluie` : État du capteur indiquant de la pluie (donnée météorologique ou capteur physique).
- `Vent` : État du capteur indiquant du vent au-dessus d’un seuil.
- `QualiteAir` : État du capteur de qualité de l'air (ex. PM2.5, CO2, etc.).
- `AlerteMeteo` : Détection d’une alerte météorologique (tempête, orage, neige, etc.).

##### Préfixes
- `Si_` : Pour exprimer une logique conditionnelle claire.
- `Lorsque_` : Pour refléter des événements déclencheurs ponctuels.
- `Dans_` : Pour des états ou contextes géographiques/temporaux (zones, périodes, etc.).
- `Pendant_` : Pour des durées ou périodes spécifiques.
- `Apres_` : Pour indiquer des actions après un événement ou un délai.
- `Avant_` : Pour indiquer des actions avant un événement ou une limite temporelle.

### Contexte ou Texte Libre
Le texte "Libre" permet d’ajouter des informations spécifiques ou des précisions non couvertes par les autres parties de la structure.
`Quand l’utiliser:` Si un scénario ou un script nécessite une distinction particulière.



