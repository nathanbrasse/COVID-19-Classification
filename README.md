# COVID-19-Classification

## 🎯 Project Overview

This project develops a machine learning model to predict COVID-19 infection based on self-reported symptoms and risk factors. Using a decision tree classifier, the model analyzes 20 different features including symptoms (fever, dry cough, breathing problems) and behavioral risk factors (travel history, large gatherings, mask wearing) to determine the likelihood of a positive COVID-19 test.

**Key Features:**
- Binary classification (COVID-19 Positive/Negative)
- Interpretable decision tree model with clear decision paths
- Comprehensive analysis of symptom importance
- 94.29% accuracy on test data
- Balanced dataset handling for unbiased predictions

## 📊 Dataset

- **Source:** Crowdsourced COVID-19 Symptom Dataset (Kaggle)*
- **Size:** 5,434 observations
- **Features:** 20 input features + 1 target variable
- **Data Type:** Binary categorical (Yes/No) for all features
- **Collection Period:** Early COVID-19 pandemic phase
- **Split:** 80% training, 20% testing

*Note: Dataset link updated due to original removal - current version is a verified copy*

### Key Features Categories

**Symptoms (13 features):**
- Respiratory: Breathing problems, Dry cough, Running nose
- General: Fever, Headache, Fatigue, Sore throat
- Gastrointestinal symptoms
- Pre-existing conditions: Asthma, Chronic lung disease, Heart disease, Diabetes, Hypertension

**Risk Factors (7 features):**
- Travel abroad
- Contact with COVID-19 patient
- Attended large gathering
- Visited public exposed places
- Family working in public exposed places
- Wearing masks
- Sanitization practices

## 🔧 Technical Stack

- **Language:** Python 3.8+
- **Core Libraries:** 
  - Data Processing: Pandas, NumPy
  - Visualization: Matplotlib, Seaborn
  - Machine Learning: Scikit-learn
  - Model Evaluation: Classification metrics, Confusion matrix

## 🌳 Model Architecture

### Decision Tree Classifier
- **Algorithm:** Decision Tree (Scikit-learn)
- **Max Depth:** 5 (optimized for best performance)
- **Criterion:** Gini impurity
- **Data Handling:** Under-sampling of majority class for balance

### Why Decision Tree?
- **Perfect fit for binary categorical data:** All features are Yes/No responses
- **High interpretability:** Clear decision paths showing symptom combinations
- **Effective pattern recognition:** Captures complex relationships between symptoms
- **Clinical relevance:** Mirrors diagnostic decision-making process

## 📈 Results

### Model Performance
- **Overall Accuracy:** 94.29%
- **Statistical Significance:** p-value < 2.2e-16
- **Training/Test Split:** 80/20

### Confusion Matrix Results
| Actual/Predicted | Negative | Positive |
|------------------|----------|----------|
| **Negative** | 1,051 | 0 |
| **Positive** | 120 | 931 |

### Key Performance Insights
- **True Negatives:** 1,051 (perfect negative prediction)
- **True Positives:** 931 (high positive detection)
- **False Positives:** 0 (no false alarms)
- **False Negatives:** 120 (missed positive cases)

## 🔍 Feature Importance & Decision Paths

### Most Important Features (in order):
1. **Travel Abroad** - Primary decision node (early pandemic indicator)
2. **Attended Large Gathering** - Secondary risk factor
3. **Breathing Problems** - Critical symptom indicator
4. **Sore Throat** - Key symptom correlation
5. **Dry Cough** - Distinctive COVID-19 symptom

### Decision Tree Logic:
```
Root: Travel Abroad?
├── Yes → High risk path → Additional symptom checks
└── No → Large Gathering?
    ├── Yes → Breathing Problems? → Classification
    └── No → Symptom-based evaluation
```

## 🎯 Key Findings

### Clinical Insights
- **Travel history** was the strongest predictor during early pandemic phases
- **Respiratory symptoms** (breathing problems, dry cough) showed high correlation
- **Behavioral factors** (large gatherings) significantly impact transmission risk
- **Sore throat** emerged as an important distinguishing symptom

### Model Insights
- **Zero false positives** indicates conservative prediction approach
- **120 false negatives** suggest some asymptomatic or mild cases missed
- **Perfect negative classification** shows strong ability to rule out COVID-19
- **High statistical significance** confirms robust pattern recognition

## ⚠️ Important Disclaimers

**This model is for educational and research purposes only. It should NOT be used for medical diagnosis or replace professional medical consultation.**

### Limitations
- Based on **self-reported symptoms** without clinical verification
- **Early pandemic data** may not reflect current COVID-19 variants
- **Limited demographic diversity** in crowdsourced dataset
- **No clinical validation** in healthcare settings
- **Missing asymptomatic cases** due to symptom-based approach

### Ethical Considerations
- Model should supplement, not replace, medical testing
- Results require medical professional interpretation
- Potential for health anxiety if used inappropriately
- Privacy considerations for health data

## 📚 Technical Details

### Data Preprocessing
- **Class imbalance handling:** Under-sampling majority class
- **Feature encoding:** Binary categorical (0/1) conversion
- **No missing values:** Complete dataset integrity
- **Feature correlation analysis:** Identified key symptom relationships

### Model Validation
- **Cross-validation:** Ensured model generalization
- **Hyperparameter tuning:** Optimized tree depth and criteria
- **Statistical testing:** Confirmed significance of results

## 🔮 Future Enhancements

- Integration with current COVID-19 variant symptoms
- Addition of demographic features (age, gender, location)
- Ensemble methods for improved accuracy
- Real-time symptom tracking interface
- Integration with health monitoring devices

## 📚 References

1. Original Kaggle Dataset: "Symptoms COVID-19 using 7 Machine Learning 98%"
2. WHO COVID-19 Symptom Guidelines
3. CDC COVID-19 Risk Factors Documentation
4. Early COVID-19 Symptom Research Papers

