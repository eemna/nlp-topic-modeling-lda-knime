# 🧠 NLP Topic Modeling using LDA with KNIME

Ce projet fait partie d’un travail de **Traitement Automatique du Langage Naturel (NLP)**.  
Il met en œuvre la **modélisation de sujets (Topic Modeling)** à l’aide de **Latent Dirichlet Allocation (LDA)** sur le **BBC News Dataset** en utilisant la plateforme **KNIME Analytics Platform**.

---

## 🎯 Objectif du projet
L’objectif principal est d’extraire automatiquement les **thèmes dominants** à partir d’un grand nombre de documents textuels.  
Grâce à l’algorithme **LDA**, le projet découvre les principaux sujets abordés dans les articles de presse du dataset BBC News.

---

## 🧩 Étapes du Workflow KNIME

### 🔹 1. Acquisition et préparation des données
- **CSV Reader** : importation du dataset BBC News  
- **Case Converter** : conversion du texte en minuscules  
- **Strings to Document** : transformation du texte brut en format document KNIME  
- **Partitioning** : division en 80 % d’entraînement et 20 % de test  

### 🔹 2. Prétraitement NLP
- **Punctuation Erasure** : suppression de la ponctuation  
- **Number Filter** : suppression des chiffres  
- **Stop Word Filter** : suppression des mots vides  
- **Snowball Stemmer** : racinisation des mots  
- **Bag of Words Creator** : représentation vectorielle du texte  

### 🔹 3. Modélisation LDA
- **Topic Extractor (Parallel LDA)** : entraînement du modèle LDA  
  - Nombre de topics : **5**  
  - Seed : **42**  

### 🔹 4. Attribution de labels et regroupement
- **Table Creator + Joiner** : association de labels sémantiques à chaque topic  
- **GroupBy + Sorter** : regroupement et classement des termes dominants  

### 🔹 5. Estimation et évaluation
- **GroupBy + Math Formula** : calcul de la probabilité de chaque topic dans les documents  
- **Scorer** : évaluation du modèle  

### 🔹 6. Visualisation
- **Pie Chart** : répartition globale des topics  
- **Bar Chart** : fréquence des topics par document  
- **Color Manager + Table View** : affichage coloré des résultats  

---

## 📈 Résultats attendus
- Identification automatique de **5 grands thèmes** dans le corpus BBC News.  
- Évaluation de la distribution des topics pour chaque document.  
- Représentation visuelle claire via **diagrammes circulaires et barres**.

---

## 🛠️ Technologies et outils
- **KNIME Analytics Platform**  
- **NLP / Text Mining**  
- **Latent Dirichlet Allocation (LDA)**  
- **BBC News Dataset (CSV)**  

---

## 📂 Structure du projet
