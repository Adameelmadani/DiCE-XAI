# Mini-projet XAI — DiCE (Diverse Counterfactual Explanations)

**Projet :** Contrefactuels Divers  
**Étudiant :** Adam El Madani  

---

## Description du Projet

Ce projet explore et implémente la méthode **DiCE (Diverse Counterfactual Explanations)** pour l'explicabilité de l'intelligence artificielle (XAI). 

Contrairement aux méthodes d'explicabilité classiques (comme LIME ou SHAP) qui se concentrent sur l'importance des caractéristiques, DiCE répond à une question orientée vers l'action :
> *"Que faudrait-il changer minimalement dans mes caractéristiques pour obtenir une décision différente du modèle ?"*

L'objectif est de générer un ensemble de **contre-factuels diversifiés** pour proposer plusieurs options réalistes à un utilisateur (par exemple, comment obtenir un prêt bancaire après un refus).

## Contexte & Motivation

### Le Problème
Lorsqu'un modèle "boîte noire" prend une décision négative (ex: refus de crédit), l'utilisateur a besoin de savoir comment changer ce résultat. Cependant, une seule explication peut être inutile si elle suggère des changements impossibles (ex: changer d'âge ou de race).

### La Solution DiCE
DiCE génère **k** contre-factuels qui optimisent trois critères :
1.  **Validité** : Le contre-factuel doit aboutir à la classe souhaitée (ex: "Accepté").
2.  **Proximité** : Les changements doivent être minimes par rapport au profil original.
3.  **Diversité** : Les solutions proposées doivent être variées pour offrir de vrais choix (différentes combinaisons de changements).

## Stack Technique

* **Langage** : Python 3
* **Bibliothèque XAI** : `dice-ml`
* **Machine Learning** : `scikit-learn` (Random Forest Classifier), `xgboost`, `lightgbm`
* **Manipulation de données** : `pandas`, `numpy`
* **Visualisation** : `matplotlib`, `seaborn`

## Installation

Pour exécuter ce projet, installez les dépendances nécessaires via pip :

```bash
pip install dice-ml scikit-learn pandas numpy matplotlib seaborn
```

## Presentation:
https://docs.google.com/presentation/d/1P-NMMUDN9FcCRl8hoAV2SAcDsIpvdAkkwu2tMGo8Oyo/edit?usp=sharing
