# ML-project

#  Radar Signal Classification (UCI Ionosphere Dataset)

Progetto d'esame per il corso di **Machine Learning**. L'obiettivo del progetto è la classificazione binaria dei segnali radar restituiti da un sistema ad alta frequenza basato su un array di antenne situato a Goose Bay, Labrador. I segnali sono classificati in:
* **Good (`g`)**: Segnali che mostrano prove di strutture libere nella ionosfera.
* **Bad (`b`)**: Segnali che non attraversano la ionosfera.

## 🛠️ Tech Stack & Librerie
* **Linguaggio:** Python 3.x
* **Data Manipulation & Viz:** Pandas, NumPy, Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn

## Pipeline del Progetto

1. **Exploratory Data Analysis (EDA) & Preprocessing:**
   * Analisi di 34 feature numeriche continue.
   * Identificazione e rimozione di attributi a varianza zero/costanti (es. `attr_2`).
   * Verifica del bilanciamento delle classi nel dataset target.
   * Normalizzazione e scaling delle feature.

2. **Dimensionality Reduction:**
   * Applicazione della **Principal Component Analysis (PCA)** per ridurre la dimensionalità delle feature mantenendo la maggior parte della varianza spiegata.

3. **Modellazione & Algoritmi:**
   Confronto e valutazione delle prestazioni dei seguenti modelli:
   * Support Vector Machines (SVM)
   * Logistic Regression
   * Perceptron
   * Linear Discriminant Analysis (LDA)
   * Quadratic Discriminant Analysis (QDA)

4. **Validazione e Metriche:**
   * **Stratified K-Fold Cross-Validation** per evitare overfitting e garantire la rappresentatività delle classi nei fold.
   * Valutazione tramite **Accuracy, Precision, Recall (Sensibilità)** e **Matrice di Confusione**.

## 📊 Risultati Principali
* Il modello con le migliori prestazioni generali è stato **[es. SVM con kernel RBF]**, ottenendo un'accuracy del **[es. 89%]** e un'ottima sensibilità nel rilevare la classe target.
