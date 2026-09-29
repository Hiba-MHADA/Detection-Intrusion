# 🛡️ Détection d'intrusions réseau par apprentissage automatique

Projet de fin d'études (Licence Sciences Mathématiques et Informatique, FSBM, Université Hassan II de Casablanca), soutenu le 16 juin 2025.

**Auteures :** Hiba Mhada & Zaineb Youmouloud
**Encadrement :** Pr. Faouzia Benabbou (encadrante), Dr. Chaimae Zaoui et Pr. Nabil Aharrane (co-encadrants)

## 🎯 Objectif
Comparer plusieurs algorithmes d'apprentissage supervisé pour détecter les intrusions dans le trafic réseau, puis déployer les modèles dans une application Streamlit.

## 🔬 Démarche
- Données : jeu **UNSW-NB15** (trafic réseau normal et attaques simulées)
- Prétraitement, équilibrage des classes et sélection des variables
- Modèles comparés : Random Forest, Decision Tree, Régression logistique, Naive Bayes, XGBoost, LightGBM
- Évaluation : précision, rappel, matrices de confusion, temps d'exécution
- Déploiement : interface **Streamlit** (prédiction manuelle et prédiction sur fichier CSV)

## 📊 Résultats
Random Forest et Decision Tree sont les modèles les plus performants. Avec les matrices de confusion normalisées, XGBoost classe correctement 99,46 % des flux normaux et 96,98 % des attaques, LightGBM 99,56 % et 97,14 %.

## 🗂️ Contenu du dépôt
```
code de visu-pretr-entr.ipynb     notebook : visualisation, prétraitement, entraînement
interface.zip                     application Streamlit (detection.py) et modèles entraînés
PFE  Detection d_intrusion.docx   rapport du PFE
PFE detection d_intrusion.pptx    présentation de la soutenance
```

## ⚙️ Utilisation
1. Installer les bibliothèques : `pip install streamlit pandas numpy scikit-learn xgboost lightgbm imbalanced-learn joblib matplotlib seaborn`
2. Dézipper `interface.zip`.
3. Dans `interface/detection.py`, adapter la variable `MODELS_PATH` au dossier où se trouvent les modèles sur votre machine.
4. Lancer : `streamlit run detection.py`

## 📚 Données
Le dataset UNSW-NB15 (156 Mo compressé) n'est pas inclus dans ce dépôt : https://research.unsw.edu.au/projects/unsw-nb15-dataset

## 🛠️ Technologies
Python · scikit-learn · XGBoost · LightGBM · imbalanced-learn · Streamlit · Pandas · Matplotlib
