# Training-Os

Application personnelle d'entraînement : musculation et cardio, avec des séances adaptées au temps dont je dispose.
Fonctionne dans le navigateur, s'installe sur l'écran d'accueil de l'iPhone, et marche hors connexion.

**Adresse en ligne :** `https://<ton-identifiant>.github.io/training-os/`

## Ce que contient le dépôt

| Fichier | Rôle |
|---|---|
| `index.html` | Toute l'application : structure, styles et code, dans un seul fichier |
| `manifest.webmanifest` | Nom, icône et couleurs de l'app une fois installée |
| `sw.js` | Cache hors connexion. **Incrémenter `VERSION` à chaque mise à jour** |
| `icons/` | Icônes de l'écran d'accueil |
| `.nojekyll` | Demande à GitHub Pages de servir les fichiers tels quels |

## Publier une modification

1. Modifier le fichier (sur github.com, ou dans l'éditeur en ligne en tapant `.` depuis le dépôt).
2. Si `index.html`, `sw.js` ou le manifeste a changé : ouvrir `sw.js` et passer `training-os-v1` à `v2`, `v3`, etc.
3. Valider (« Commit changes »). Le site est à jour en une à deux minutes.
4. Sur l'iPhone : fermer complètement l'app puis la rouvrir pour récupérer la nouvelle version.

## État du projet

**Construit**

- Générateur de séance : durée disponible, forme du jour, gêne du jour, corps entier
- Déroulé guidé : séries, repos automatique, étalonnage, saisie des répétitions réelles
- Progression automatique : deux séances réussies font monter les répétitions puis la charge
- Records personnels par exercice
- Fiches : carte musculaire annotée face/dos, vidéo de démonstration, consignes et erreurs
- Musculation : 23 exercices, charges limitées aux crans réels de l'haltère
- Chronomètre de repos autonome
- Cardio continu et fractionné, son de cadence, mesure de cadence au toucher ou par l'accéléromètre
- Niveau cardio : endurance et plafond, allures de fractionné déduites
- Historique : séances, détail des séries, effort ressenti, volume hebdomadaire
- Poids et tour de taille, une fois par mois

**À construire**

- Sauvegarde hors du téléphone (export de fichier ou synchronisation Firebase)
- Semaine allégée périodique
- Graphiques de progression par exercice

Le cahier des charges complet vit dans le projet Claude « Training-OS ».

## Données

Tout est enregistré dans le navigateur du téléphone (`localStorage`) : réglages, plan de fractionné, thème.
Rien ne part sur un serveur. Effacer les données de Safari efface les réglages.
