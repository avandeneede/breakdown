# repartition

App HTML qui décompose un montant selon une **clé de répartition** avec ordre de priorité. Pensée pour les chefs d'entreprise, comptables et particuliers qui veulent répartir revenus, budgets ou frais avec rigueur.

**Live :** https://avandeneede.github.io/repartition/

## Fonctionnalités

- **3 types de clés par ligne**
  - Montant fixe (€, $, £, ¥, etc.)
  - Pourcentage du total
  - Pourcentage de ce qui reste après les clés de priorité supérieure
- **Ordre de priorité** — les clés du haut sont servies en premier si le montant ne suffit pas
- **Multi-profils** — un profil par cas d'usage (paie, chiffre d'affaires, budget projet, charges à répartir)
- **~45 devises** internationales (EUR, USD, GBP, CHF, JPY, CNY, CAD, AUD, INR, BRL, MXN, ZAR, AED, etc.)
- **100+ icônes business** (finance, équipe, documents, tech, immobilier, transport, énergie, industrie, services…)
- **12 couleurs** système iOS pour personnaliser chaque clé
- **Multilingue** EN / FR / NL avec détection automatique (français par défaut si langue non supportée)
- **Thème clair / sombre** automatique (suit le système)
- **Saisie du montant par pas de 50** sur les flèches (clavier + spinner)
- **100 % local** — stockage `localStorage`, aucun serveur, aucune donnée envoyée
- **Mobile-first** — s'ajoute à l'écran d'accueil iOS/Android comme une app native

---

## Guide rapide

### 1. Définir le montant

Tapez le montant à répartir en haut de l'écran. Les flèches ↑/↓ du clavier et les boutons spinner incrémentent par pas de **50**. Touchez le symbole de devise pour ouvrir le sélecteur (toutes les devises internationales).

### 2. Ajouter des clés

1. Touchez `+` dans la section « Clés de répartition »
2. Choisissez une **icône** parmi 100+ (maison, voiture, briefcase, mégaphone, équipe, nuage, panneau solaire, graphique, etc.) et une **couleur**
3. Donnez un nom (ex. « Loyer », « Salaires », « Marketing », « Réserve »)
4. Entrez la valeur puis choisissez :
   - `€` (ou devise du profil) pour un **montant fixe**
   - `%` `Du total` pour un **pourcentage du montant total**
   - `%` `Du reste` pour un **pourcentage de ce qui reste** après les clés de priorité supérieure

### 3. Ordre de priorité

Les clés sont traitées **de haut en bas**. Si le montant ne suffit pas à couvrir toutes les clés, celles du haut sont servies en premier ; les suivantes reçoivent ce qui reste.

Pour réorganiser, ouvrez une clé et utilisez `↑ Monter` / `↓ Descendre`.

**Exemple.** Montant 5 000 €.
- Priorité 1 — Loyer 1 800 € (fixe)
- Priorité 2 — Salaires 40 % du total
- Priorité 3 — Réserve 20 % du reste

→ Loyer reçoit 1 800 €, Salaires 2 000 €, Réserve 240 € (20 % de 1 200), libre 960 €.

### 4. Plusieurs profils

En haut à droite, tapez sur le nom du profil. Créez un profil par cas d'usage. Chaque profil a ses **propres clés, montant et devise** — utile pour séparer « paie personnelle », « chiffre d'affaires », « budget projet X », « charges à partager entre associés », etc.

### 5. Langue et devise

- **Langue** : détectée automatiquement depuis le système. Si la langue de l'appareil n'est pas supportée (EN / FR / NL), l'app utilise le **français par défaut**. Pour changer manuellement : **Données → Langue**.
- **Devise** : par profil. Touchez le symbole à gauche du montant ou passez par **Données → Devise**.

---

## Exporter / Importer

Les données vivent uniquement dans le navigateur de l'appareil. Pour sauvegarder ou transférer :

### Exporter ses profils

1. Section **Données** → **Exporter mes profils**
2. Un fichier `repartition-YYYY-MM-DD.json` est téléchargé contenant tous vos profils, clés, devises et langue
3. Sauvegardez-le (iCloud Drive, Dropbox, Google Drive, email…) ou envoyez-le vers un autre appareil via AirDrop

### Importer sur un autre appareil

1. Ouvrez l'app sur le nouvel appareil (ou un nouveau navigateur)
2. Section **Données** → **Importer un fichier**
3. Choisissez le fichier JSON exporté
4. Confirmez — toutes les données actuelles sont remplacées par le contenu du fichier

> ⚠️ L'import **remplace** toutes les données actuelles de l'app. Si vous voulez les conserver, exportez-les d'abord.

---

## Installer sur iPhone

1. Ouvrez l'URL dans Safari
2. Bouton Partager → **« Sur l'écran d'accueil »**
3. L'app s'ouvre ensuite en plein écran, comme une app native

## Utilisation locale

Ouvrez simplement `index.html` dans un navigateur — aucune installation requise.

## Activer GitHub Pages

Settings → Pages → Source : branch `main`, dossier `/` (root) → Save.
