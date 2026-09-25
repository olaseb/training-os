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

- Chronomètre de repos : anneau, durées prédéfinies, ±15 s, alerte à 10 s et à 0, écran maintenu allumé
- Cardio en mode **continu** : une durée, une allure, une sonnerie à la fin
- Cardio en mode **fractionné** : blocs modifiables, cycle répétable, quatre modèles, annonces vocales
- **Son de cadence** : un clic au rythme écrit dans l'allure, activable en pleine séance
- **Mesure de cadence** : au toucher, ou par l'accéléromètre du téléphone

**À construire**

- Générateur de séance par durée disponible, avec remplacement et suppression d'exercices
- Bibliothèque d'exercices : animations, vidéos, consignes
- Musculation : inventaire des disques d'haltères et charges réellement montables
- Historique, progression, blocs étalons d'évaluation du niveau
- Synchronisation Firebase

Le cahier des charges complet vit dans le projet Claude « Training-OS ».

## Données

Tout est enregistré dans le navigateur du téléphone (`localStorage`) : réglages, plan de fractionné, thème.
Rien ne part sur un serveur. Effacer les données de Safari efface les réglages.
