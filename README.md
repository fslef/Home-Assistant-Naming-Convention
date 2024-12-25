# Convention de Nommage pour les Scripts et les Automatisations

## Introduction

Ce document présente une convention de nommage claire et cohérente pour les scripts et automatisations dans Home Assistant. Il vise à faciliter la gestion, la lisibilité et l'organisation des configurations, tout en permettant des ajouts futurs avec une logique simple.

---

## 1. Règles de Nommage pour les Scripts

### Structure

**[Catégorie] - [Action] - [Contexte] - [Libre]**

Cette structure permet de catégoriser chaque script en fonction de son but principal (catégorie), de l'action qu'il effectue, du contexte dans lequel il est utilisé, et d'une description personnalisée (champ libre).

### Liste des Éléments

#### Catégories

- **Éclairage** : Pour tout ce qui concerne les lumières.
- **Sécurité** : Scripts liés aux alarmes, caméras ou tout dispositif de sécurité.
- **CVC** : Gestion de la température et du chauffage (chauffage / ventilation / clim).
- **Volets** : Gestion des stores, volets roulants, ou rideaux motorisés.
- **Multimédia** : Contrôle des appareils multimédias comme les télévisions ou enceintes.
- **Routine** : Scripts pour les routines ou actions programmées (matin, soir, départ, etc.).
- **Divers** : Catégorie générique pour des scripts non catégorisables.

#### Actions

Avec l'introduction de fonctionnalités comme les `trigger_id`, il est désormais possible de créer des automatisations capables de gérer des actions inverses (comme allumer ou éteindre une lumière) dans un seul flux logique. Voici les actions principales, combinant les valeurs classiques et les nouvelles logiques :

- **Allumer** : Active un appareil ou une lumière.
- **Éteindre** : Désactive ou éteint un appareil.
- **Basculer** : Gère les états on/off dans une seule logique (ex : basculer une lumière allumée/éteinte).
- **Régler** : Ajuste une intensité, une température ou une valeur spécifique.
- **Exécuter** : Déclenche une action particulière sans ambiguïté d'état.
- **Ouvrir** : Commande pour ouvrir un volet ou une porte.
- **Fermer** : Commande pour fermer un volet ou une porte.
- **Changer** : Modifie un état ou une configuration (ex : changer une couleur ou un mode).
- **Baisser** : Diminue une intensité (ex : température ou lumière).
- **Augmenter** : Augmente une intensité.
- **Ajuster** : Permet de gérer des augmentations et diminutions dynamiques dans une seule logique.

#### Libre

- **Description personnalisée** : Ce champ est utilisé pour ajouter une description libre qui permet d'expliquer une condition particulière ou un détail spécifique.

### Exemples

- `Éclairage - Salon - Luminaire - Soirée - Allumer` : Automatisation pour allumer le luminaire dans le salon pour une ambiance de soirée.
- `Sécurité - Jardin - Caméra - Activer - Nuit` : Active les caméras de surveillance dans le jardin la nuit.
- `Volets - Chambre - Volets - Fermer - Routine Matin` : Ferme les volets de la chambre comme partie de la routine matinale.
- `CVC - Maison - Chauffage - Baisser - Absence` : Diminue le chauffage dans toute la maison en cas d'absence.

---

## 2. Règles de Nommage pour les Automatisations

### Structure

**[Catégorie] - [Zone] - [Appareil] - [Libre] - [Action]**

Cette structure organise les automatisations en fonction de leur but principal (catégorie), de la zone où elles sont actives, de l'appareil concerné, d'une description libre pour plus de détails, et de l'action effectuée.

### Liste des Éléments

#### Catégories

- **Éclairage** : Automatisations liées aux lumières.
- **Sécurité** : Automatisations pour les alarmes, caméras, détecteurs.
- **CVC
