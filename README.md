# 🧬 Cancer Treatment ML  
**Predizione del Cancro mediante Analisi Genetica con tecniche di Machine Learning**

Questo progetto mira a sviluppare modelli di *Machine Learning* capaci di prevedere l’impatto clinico di mutazioni genetiche, combinando dati genomici e testuali.  
L’obiettivo è supportare l’oncologia di precisione, favorendo la personalizzazione dei trattamenti in base al profilo genetico del paziente.

---

## 📖 Descrizione del Progetto

### 🎯 Research Question
> È possibile sviluppare un modello di *Machine Learning* in grado di prevedere l’impatto clinico di una mutazione genetica utilizzando un’analisi combinata di dati genetici e descrittivi?

### 📊 Dataset
Il progetto utilizza il **dataset MSKCC**, composto da:
- **ID**, **Gene**, **Variante**, **Classe**, **Testo descrittivo**
- 9 classi che rappresentano diverse tipologie di impatto genetico:
  1. Aumento  
  2. Probabile aumento  
  3. Perdita  
  4. Probabile perdita  
  5. Neutro  
  6. Probabile neutro  
  7. Cambio  
  8. Probabile cambio  
  9. Inconclusivo  

---

## ⚙️ Pipeline del Progetto

### 1. **Pre-processing**
- Pulizia e normalizzazione del testo (rimozione punteggiatura, lowercasing, stopwords).
- Conversione dei testi in rappresentazioni numeriche mediante **TF-IDF**.

### 2. **Feature Engineering**
- Unione di variabili testuali e genetiche (`Gene`, `Variant`, `Text`).
- Riduzione dimensionale per ottimizzare il training.

### 3. **Bilanciamento del Dataset**
- Gestione dello sbilanciamento delle classi tramite **SMOTE (Synthetic Minority Over-sampling Technique)**.

### 4. **Partizionamento**
- Suddivisione del dataset:
  - `80%` training  
  - `20%` test

### 5. **Modellazione e Training**
Sono stati testati diversi algoritmi di classificazione:
- **Random Forest**
- **K-Nearest Neighbors**
- **XGBoost**

L’ottimizzazione degli iperparametri è stata effettuata tramite *Grid Search*.

---

## 📈 Risultati

| Modello           | Dataset Originale | Dataset Bilanciato |
|-------------------|------------------:|-------------------:|
| Random Forest     | 63.6%             | **77.1%**          |
| K-Nearest Neighbors | 61.0%           | 73.3%              |
| XGBoost           | 65.3%             | **77.0%**          |

Il bilanciamento ha migliorato significativamente le prestazioni, in particolare per **XGBoost** e **Random Forest**.  

### 🔍 Metriche di Valutazione
- *Accuracy*
- *Precision*
- *Recall*
- *F1-score*
- Matrici di confusione per analisi dettagliata delle classi.

---

## 🧠 Conclusioni
- La **qualità dei dati** influisce fortemente sulle prestazioni del modello.  
- L’approccio **TF-IDF + riduzione dimensionale** si è dimostrato efficace per il trattamento di testi scientifici.  
- L’uso combinato di dati genetici e testuali fornisce una visione più completa del fenomeno.

---

## 🚀 Sviluppi Futuri
- Estensione del modello per prevedere la **risposta personalizzata ai trattamenti oncologici**.  
- Sviluppo di un’interfaccia *user-friendly* per il supporto clinico.  
- Applicazione del framework ad altre **malattie genetiche non oncologiche** (es. SLA, Sclerosi Multipla).

---

## 🧰 Tecnologie Utilizzate

| Categoria | Tecnologie |
|------------|-------------|
| **Linguaggio** | Python 3 |
| **Librerie principali** | `pandas`, `numpy`, `scikit-learn`, `xgboost`, `imbalanced-learn` |
| **Elaborazione del testo** | `nltk`, `tf-idf` |
| **Visualizzazione** | `matplotlib`, `seaborn` |
| **Gestione dataset** | `SMOTE` per oversampling |
| **Ottimizzazione** | `GridSearchCV` per tuning iperparametri |

---


## 👤 Autore
**Diego Scirocco**  
Laureando in Ingegneria Informatica  
Università degli Studi di Roma "Tor Vergata"  
A.A. 2023–2024  

Relatore: **Prof. Giuseppe Sansonetti**

---

📌 *“L’intelligenza artificiale come supporto alla medicina personalizzata: dall’analisi genetica alla predizione del cancro.”*


