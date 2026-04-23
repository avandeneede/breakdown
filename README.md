# repartition

Petite app HTML pour décomposer un montant selon une **clé de répartition**. Chaque ligne peut être un montant fixe (€) ou un pourcentage (%) du total, et les clés sont traitées selon un **ordre de priorité**.

**Live :** https://avandeneede.github.io/repartition/

## Fonctionnalités

- Décomposition d'un montant par clé de répartition
- Valeurs absolues (€) ou relatives (%) mélangées librement
- Ordre de priorité — les clés du haut sont servies en premier si le montant ne suffit pas
- Plusieurs profils (un par cas d'usage)
- Thème clair / sombre automatique (suit le système)
- 100 % local — données dans `localStorage`, aucun serveur
- Mobile-first — s'ajoute à l'écran d'accueil iOS/Android

---

## Guide rapide

### 1. Définir le montant

Tapez le montant à répartir en haut de l'écran. Tapez sur le symbole de devise pour changer (€, $, £, CHF, kr).

### 2. Ajouter des clés

1. Touchez `+` dans la section « Clés de répartition »
2. Choisissez un emoji et un nom (ex. « Loyer »)
3. Entrez la valeur puis choisissez `€` (montant fixe) ou `%` (pourcentage du total)

### 3. Ordre de priorité

Les clés sont traitées **de haut en bas**. Si le montant ne suffit pas à couvrir toutes les clés, celles du haut sont servies en premier, et les suivantes reçoivent ce qui reste.

Pour réorganiser, ouvrez une clé et utilisez `↑ Monter` / `↓ Descendre`.

**Exemple.** Montant 2 000 €.
- Priorité 1 — Loyer 900 € (fixe)
- Priorité 2 — Épargne 20 % du total
- Priorité 3 — Imprévus 300 € (fixe)

→ Loyer reçoit 900 €, Épargne 400 €, Imprévus 300 €, libre 400 €.

### 4. Plusieurs profils

En haut à droite, tapez sur le nom du profil. Créez un profil par cas d'usage (paie personnelle, charges à répartir entre projets, etc.). Chaque profil a ses propres clés.

---

## Exporter / Importer

Les données vivent uniquement dans le navigateur de l'appareil. Pour sauvegarder ou transférer vers un autre appareil :

### Exporter

1. Section **Données** → **Exporter mes profils**
2. Un fichier `repartition-YYYY-MM-DD.json` est téléchargé
3. Sauvegardez-le (iCloud Drive, Dropbox, email...) ou envoyez-le vers l'autre appareil via AirDrop

### Importer

1. Ouvrez l'app sur l'autre appareil (ou un nouveau navigateur)
2. Section **Données** → **Importer un fichier**
3. Choisissez le fichier JSON exporté

> ⚠️ L'import **remplace** toutes les données actuelles de l'app. Exportez d'abord si vous voulez les conserver.

---

## Installer sur iPhone

1. Ouvrez l'URL dans Safari
2. Bouton Partager → **« Sur l'écran d'accueil »**
3. L'app s'ouvre ensuite en plein écran, comme une app native

## Utilisation locale

Ouvrez simplement `index.html` dans un navigateur — aucune installation requise.

## Activer GitHub Pages

Settings → Pages → Source : branch `main`, dossier `/` (root) → Save.
