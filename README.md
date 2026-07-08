# 🛡️ Portfolio Interactif — Ewan Le Neillon

Bienvenue sur le dépôt de mon portfolio professionnel en cybersécurité et sécurité cloud. Ce site présente mon parcours, mes compétences et mes expériences dans le domaine des opérations de sécurité (SecOps) et du durcissement d'infrastructures.

> [!NOTE]  
> Le site est conçu comme une interface interactive inspirée d'un tableau de bord de supervision SOC (Security Operations Center), représentant un cloud vivant sous surveillance continue.

---

## 🚀 Aperçu du Profil

* **Étudiant :** Master 1 Cybersécurité — École IT Valenciennes
* **Spécialité :** Cloud Security & SecOps (durcissement, détection, remédiation)
* **Alternance :** À partir de septembre 2026 chez **Atos / Eviden** (Lille) en Cloud Security (parcours Google Cloud Partner).

---

## 🛠️ Architecture Technique & Fonctionnalités

Le portfolio est optimisé pour être à la fois léger et visuellement immersif :

* **Moteur 3D (Three.js) :** 
  * Un **cœur de cloud organique** en morphing constant calculé par des shaders de bruit Simplex en GLSL (Vertex & Fragment Shaders).
  * Un **champ de particules ambiantes** simulant des flux de télémétrie réseau, qui réagit dynamiquement au déplacement du curseur.
  * Des **plaques de durcissement (Hardening Plates)** et des **anneaux de supervision** simulant un balayage continu et réagissant aux événements de sécurité du tableau de bord.
* **Système de navigation fluide :**
  * Contrôle fluide de la caméra le long d'une courbe de positions clés (Keyframes) selon la progression du défilement.
  * **Scroll Snapping natif :** Alignement automatique et fluide du défilement sur les centres d'intérêt des 8 sections clés, évitant les coupures visuelles.
  * **Optimisation de la fluidité :** Suppression des requêtes de mise en page forcées (*layout thrashing*) via l'écouteur de défilement passif et la mise en cache des dimensions.
* **Intégration de formulaires :**
  * Formulaire de contact sécurisé connecté à l'API **Web3Forms** (clé d'accès anonymisée).

---

## 📂 Structure du Projet

```
portfolio/
├── index.html       # Structure HTML, styles CSS et logique du composant React / Three.js
├── support.js       # Runtime léger d'interprétation des composants (dc-runtime)
├── README.md        # Présentation et documentation du projet
├── LICENSE          # Licence d'utilisation MIT
└── .gitignore       # Fichiers exclus du versionnement
```

---

## ⚙️ Comment lancer le projet en local ?

### 1. Cloner le dépôt
```bash
git clone https://github.com/ewn0/portfolio.git
cd portfolio
```

### 2. Lancer un serveur local
Pour que Three.js charge correctement tous les scripts et s'affiche sans restriction CORS, lancez un serveur HTTP local dans le dossier :

* **Avec Python (Recommandé) :**
  ```bash
  python -m http.server 8000
  ```
  Ouvrez ensuite [http://localhost:8000](http://localhost:8000) dans votre navigateur.

* **Avec Node.js (via npx) :**
  ```bash
  npx serve
  ```

* **Avec VS Code :**
  Utilisez l'extension **Live Server** et cliquez sur "Go Live".

---

## ⚖️ Licence

Ce projet est sous licence [MIT](LICENSE). Vous pouvez librement l'utiliser et l'adapter pour votre propre portfolio.
