# Réseau de Neurones Convolutif (CNN) - Classification d'Images (CIFAR-10)

## Description
Ce projet présente l'utilisation d'un **réseau de neurones convolutif (CNN)** avec **TensorFlow/Keras** pour classifier des **images en couleur** parmi **10 catégories d'objets** (avions, voitures, oiseaux, chats, cerfs, chiens, grenouilles, chevaux, bateaux, camions) à partir du jeu de données **CIFAR-10**.
Le notebook montre l'ensemble du processus de modélisation en vision par ordinateur sur un jeu de données plus complexe que MNIST (images couleur), avec un CNN à plusieurs couches convolutives.

---

## Objectifs
* Charger et explorer le jeu de données CIFAR-10 (60 000 images couleur 32x32 pixels, 10 classes).
* Normaliser les pixels des images et encoder les labels en one-hot avec **to_categorical**.
* Construire un CNN à deux couches de convolution/pooling avec **Keras**.
* Entraîner le modèle avec un callback **EarlyStopping**.
* Évaluer les performances par classe et tester la prédiction sur une image individuelle.

---

## Technologies utilisées
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow / Keras

---

## Structure du projet
```
.
├── CNN_CIFAR10.ipynb
└── README.md
```
*(le jeu de données CIFAR-10 est chargé directement via `tensorflow.keras.datasets`)*

---

## Résultats
* Le CNN (deux couches de convolution à 32 filtres avec MaxPooling, puis couches denses) est entraîné jusqu'à 15 épochs avec arrêt anticipé (EarlyStopping, patience = 2).
* Le modèle atteint une **précision d'environ 68,7 %** sur l'ensemble de test, un résultat cohérent compte tenu de la complexité supérieure des images couleur par rapport à MNIST.
* Le rapport de classification montre des performances hétérogènes selon les classes : très bonnes pour les voitures et les bateaux (precision ≈ 0,80), plus faibles pour les chats (0,52) et les cerfs (0,53), catégories visuellement plus proches les unes des autres.
* Le modèle prédit correctement la classe d'une image de test individuelle choisie au hasard.

---

## Lancement
1. Cloner le dépôt ou télécharger le notebook.
2. Installer les dépendances :
```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow
```
3. Ouvrir le notebook `CNN_CIFAR10.ipynb`.
4. Exécuter les cellules dans l'ordre.

---

## Auteur
Emmanuel YOHORE
