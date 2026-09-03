# 🎨 Switch Splash Screen & Switch Boot Logo

<p align="center">
  <img src="https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows" />
  <img src="https://img.shields.io/badge/macOS-000000?style=for-the-badge&logo=apple&logoColor=white" alt="macOS" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Nintendo_Switch-E60012?style=for-the-badge&logo=nintendo-switch&logoColor=white" alt="Nintendo Switch" />
</p>

Suite de **deux applications distinctes** avec interface graphique permettant de personnaliser l'affichage au démarrage de votre Nintendo Switch sous **Atmosphère** et **Hekate** :
* **Switch Boot Logo** : Personnalisation du logo de démarrage initial (patch IPS au format `308x350`).
* **Switch Splash Screen** : Personnalisation des écrans de chargement Hekate et Atmosphère (`1280x720`).

---

## ⚙️ Modes de fonctionnement

Les deux applications prennent en charge deux modes d'exécution (avec détection automatique) :

* **Mode Interne** : L'application est exécutée directement depuis la carte MicroSD de la console.
* **Mode Externe** : L'application est exécutée sur un ordinateur (PC/Mac/Linux) et cible la carte SD de la Switch connectée en USB.

---

## ✨ Fonctionnalités Principales

### 🖼️ Personnalisation du Boot Logo
* **Génération automatique de patchs IPS** compatibles avec toutes les versions d'Atmosphère.

### 🚀 Personnalisation du Splash Screen
* **Bootlogo Hekate** : Génération directe du fichier `bootlogo.bmp` dans le dossier `bootloader/res/`.
* **Bootlogo Atmosphère** : Injection automatique du logo personnalisé directement dans le fichier `atmosphere/package3`.

### 🛠️ Éditeur Graphique & Composition
* **Drag & Drop** : Glissez-déposez une ou plusieurs images directement dans l'application (format `.png` détouré conseillé pour un meilleur rendu).
* **Cadrage & Placement automatique** : 
  * Les images importées s'ajustent automatiquement en hauteur ou en largeur pour un cadrage optimal.
  * Les images aux dimensions natives standards (`1280x720`, `1920x1024`, etc.) sont directement positionnées au bon format sans manipulation requise.
* **Formats d'images pris en charge** : Importation de vos fichiers au format `.png`, `.jpg`, `.jpeg`, `.bmp`, `.tga` et `.webp`.
* **Manipulation dynamique des images** :
  * **Zoom / Dézoom** à la molette de la souris pour ajuster la taille.
  * **Déplacement libre** des éléments par glisser-déplacer sur la zone de travail.
* **Gestion multi-calques** : Superposez plusieurs images/textes et gérez l'ordre d'affichage (premier plan / arrière-plan).
* **Éditeur de texte avancé** : Choix des polices système, de la taille et sélection de la couleur.
* **Suppression de fond (Chroma Key)** : Outil pour rendre transparente une couleur unie sur vos images.
* **Langages** : Prise en charge multilingue (Français, Anglais, etc.) avec détection automatique du système et menu de changement rapide.

---

## 🚀 Démarrage selon votre OS

Connectez la Switch en USB via Hekate (`Tools` > `USB Tools` > `SD Card`).

Extrayez le dossier `CUSTOMISATION` depuis l'archive ZIP :
* **En Mode Interne** : Placez le dossier `CUSTOMISATION` **à la racine de votre carte MicroSD**.
*(Auto-détecté sur la SD)* : Écriture directe sur la carte MicroSD insérée

```text
💾 Carte SD (Racine)
 ├── 📁 CUSTOMISATION/        <-- Emplacement du dossier en Mode Interne
 ├── 📁 atmosphere/
 │    ├── 📄 package3         <-- Splash screen Atmosphère (injecté automatiquement)
 │    └── 📁 exefs_patches/   <-- Emplacement des patchs IPS générés pour le Boot Logo
 └── 📁 bootloader/
      └── 📁 res/             <-- Emplacement du bootlogo.bmp pour Hekate
```

* **En Mode Externe** : le dossier `CUSTOMISATION` **sur votre ordinateur** ou vous le souhaitez.
*(Auto-détecté sur PC)* : Sélectionnez le point de montage de votre carte SD (`SWITCH SD`) dans le menu déroulant (utilisez 🔄 pour rafraîchir).

### 🪟 Windows
1. Ouvrez le dossier `CUSTOMISATION`.
2. Lancez l'application souhaitée (`.exe`).
> ⚠️ **Faux positif Antivirus** : L'exécutable étant compilé localement, Windows Defender ou votre antivirus peut afficher une alerte. Cliquez sur **"Plus d'informations"** puis **"Exécuter quand même"**.

### 🍏 macOS
1. Ouvrez le dossier `CUSTOMISATION`.
2. Lancez d'abord le script d'activation (`Activer ... .app`). Il configure les autorisations de sécurité (Gatekeeper) et ouvre les réglages **Prise de vue de l'écran** (**Réglages Système > Confidentialité et sécurité**) nécessaires au fonctionnement du **glisser-déposer (Drag & Drop)**.
3. Lancez ensuite l'application principale (`.app`).

### 🐧 Linux
1. Ouvrez le dossier `CUSTOMISATION`.
2. Lancez l'application de votre choix.
> 💡 Si le lancement direct échoue, ouvrez un terminal dans le dossier et lancez le script d'activation via la commande `bash` (consultez le fichier `.txt` explicatif inclus).


---

## 🛠️ Utilisation de l'application

Une fois l'application lancée (**Boot Logo** ou **Splash Screen**), le processus est identique :
   * Préparez votre visuel
   * Cliquez sur **Générer**. L'application se charge de placer automatiquement les fichiers modifiés aux bons endroits.

---

## 📸 Capture d'écran

<p align="center">
  <a href="screenshots/SWITCH_BOOT_LOGO.jpg" target="_blank">
    <img src="screenshots/SWITCH_BOOT_LOGO.jpg" width="320" style="max-width:100%; border-radius:6px; box-shadow: 0 4px 8px rgba(0,0,0,0.2); margin: 5px;" alt="Cliquez pour agrandir l'aperçu"/>
  </a>
  <a href="screenshots/SWITCH-SPLASH-SCREEN.jpg" target="_blank">
    <img src="screenshots/SWITCH-SPLASH-SCREEN.jpg" width="320" style="max-width:100%; border-radius:6px; box-shadow: 0 4px 8px rgba(0,0,0,0.2); margin: 5px;" alt="Cliquez pour agrandir l'aperçu"/>
  </p>