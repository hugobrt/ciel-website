# Site vitrine de Ciel

Page de présentation et de téléchargement pour l'application météo **Ciel**.
Statique (HTML/CSS/JS), responsive, prête pour **GitHub Pages**.

```
ciel-site/
├─ index.html        ← la page
├─ assets/
│  ├─ icon.png       ← logo / favicon (512)
│  ├─ favicon.png    ← favicon (180)
│  └─ og.png         ← image de partage (réseaux sociaux)
├─ .nojekyll
└─ README.md
```

## 1. Personnaliser les liens

Ouvre `index.html` et, tout en bas dans le `<script>`, remplace par ton dépôt :

```js
const GITHUB_USER = "votre-pseudo";
const GITHUB_REPO = "ciel";
```

Tous les boutons (Télécharger l'APK, Code source, Versions, Issues) se mettent à jour
automatiquement. Le bouton **« Télécharger l'APK »** pointe vers
`.../releases/latest` : pense à publier ton APK dans une **Release** GitHub.

## 2. Publier sur GitHub Pages

Deux options.

**Option A — un dépôt dédié au site**
1. Crée un dépôt (ex. `ciel-site`) et pousses-y le contenu de ce dossier.
2. Repo ▸ **Settings ▸ Pages** ▸ Source : **Deploy from a branch** ▸ branche `main` ▸ dossier `/ (root)`.
3. Quelques minutes plus tard, le site est en ligne sur `https://votre-pseudo.github.io/ciel-site/`.

**Option B — le site dans le dépôt de l'app**
1. Place ce dossier dans `docs/` à la racine du dépôt `ciel`.
2. Settings ▸ Pages ▸ branche `main` ▸ dossier **`/docs`**.
3. En ligne sur `https://votre-pseudo.github.io/ciel/`.

## 3. Publier l'APK (pour que le bouton fonctionne)

1. Construis l'APK (voir le README du projet `ciel-app`).
2. Sur GitHub : onglet **Releases ▸ Draft a new release**, crée un tag (ex. `v1.0.0`),
   et **glisse ton fichier `.apk`** dans les *assets* de la release.
3. Le bouton « Télécharger l'APK » du site mène vers cette dernière release.

## Personnaliser le contenu

Tout est dans `index.html` : couleurs (variables CSS en haut), textes, et les
maquettes de téléphone (recréées en HTML/CSS, faciles à ajuster). Pour changer
l'image de partage, remplace `assets/og.png` (1200×630).
