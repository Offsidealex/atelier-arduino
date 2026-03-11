# ⚙️ Atelier Arduino — Lycée Denis Diderot, Belfort

Application web de TP de physique-chimie utilisant des cartes Arduino.  
Fonctionne **sans installation**, directement dans le navigateur via un lien GitHub Pages.

---

## 📺 Modules disponibles

| Module | Description |
|--------|-------------|
| 🧪 **Dosage pH** | pH-mètre temps réel, calibration 2 points, courbe de dosage, point d'équivalence |
| 🎈 **Loi de Mariotte** | Capteur de pression, P×V=cte, régression linéaire, tableur intégré |
| 🌡️ **Température** | Sondes DS18B20, 1 ou 2 voies, enregistrement CSV |
| 📺 **Oscilloscope** | Simulateur de signal sinusoïdal, réglages Volts/div et Temps/div, son |

---

## 🚀 Déploiement sur GitHub Pages (gratuit)

### Étape 1 — Créer un compte GitHub
Rendez-vous sur [github.com](https://github.com) et créez un compte si vous n'en avez pas.

### Étape 2 — Créer un nouveau dépôt
1. Cliquez sur le bouton vert **"New"** (ou **"+"** en haut à droite → *New repository*)
2. Donnez un nom, par exemple : `atelier-arduino`
3. Laissez le dépôt en **Public**
4. Cliquez sur **"Create repository"**

### Étape 3 — Uploader le fichier
1. Dans votre nouveau dépôt, cliquez sur **"uploading an existing file"**
2. **Renommez le fichier** `atelier-arduino.html` → **`index.html`** avant de l'uploader  
   *(le nom `index.html` est obligatoire pour que GitHub Pages fonctionne)*
3. Glissez-déposez le fichier `index.html`
4. Cliquez sur **"Commit changes"**

### Étape 4 — Activer GitHub Pages
1. Allez dans **Settings** (onglet en haut du dépôt)
2. Dans le menu gauche, cliquez sur **Pages**
3. Sous *Source*, sélectionnez **"Deploy from a branch"**
4. Choisissez la branche **`main`** et le dossier **`/ (root)`**
5. Cliquez sur **Save**

### Étape 5 — Accéder à l'application
Après 1 à 2 minutes, votre application est accessible à l'adresse :

```
https://VOTRE-PSEUDO.github.io/atelier-arduino
```

Partagez ce lien avec vos collègues ou élèves — aucune installation requise !

---

## 🌐 Compatibilité navigateur

> ⚠️ **Chrome ou Edge uniquement** pour la connexion Arduino (Web Serial API)

| Navigateur | Connexion Arduino | Simulateur oscilloscope |
|------------|:-----------------:|:-----------------------:|
| Google Chrome ✅ | ✔️ | ✔️ |
| Microsoft Edge ✅ | ✔️ | ✔️ |
| Firefox ❌ | ✗ (non supporté) | ✔️ |
| Safari ❌ | ✗ (non supporté) | ✔️ |

---

## 🔌 Format des données Arduino (port série)

L'application lit les données envoyées par l'Arduino sur le port série à **115 200 bauds**.

### Module pH
```
Voltage: 1234 mV  pH = 7.01
```

### Module Mariotte
```
Pression: 101.3 kPa
```
ou
```
P = 101.3 kPa
```

### Module Température
```
23.5,18.2        ← 2 sondes
23.5             ← 1 sonde
```

---

## 📁 Structure du dépôt

```
atelier-arduino/
└── index.html      ← fichier unique, tout est intégré (HTML + CSS + JS)
```

Pas de dépendances à installer, pas de serveur nécessaire.  
Les bibliothèques (Chart.js, Google Fonts) sont chargées depuis des CDN publics.

---

## ✏️ Modifier l'application

Ouvrez `index.html` avec n'importe quel éditeur de texte (VS Code, Notepad++…).  
Après modification, re-uploadez le fichier sur GitHub : la mise à jour est en ligne en moins d'une minute.

---

## 📄 Licence

Libre d'utilisation et de modification pour un usage pédagogique.  
Lycée Denis Diderot — Belfort — 2026
