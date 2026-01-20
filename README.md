# Title: Learning Probability Density Function using Roll-Number-Parameterized Non-Linear Model

---

## 1. Methodology

Data Collection → Data Pre-processing → Non-Linear Transformation →  
Parameter Estimation → PDF Modeling → Result Analysis

---

## 2. Description

- Dataset Used: India Air Quality Dataset
- Dataset Source: Kaggle
- Dataset Link: https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data
- Feature Selected: NO₂ concentration
- Data Cleaning: Missing values removed
- Transformation: Roll-number-based non-linear sine transformation
- Model Used: Gaussian-like Probability Density Function

---

## 3. Input / Output

### Input
- Raw NO₂ values from air quality dataset

### Output
- Transformed variable z
- Learned probability density function
- Estimated parameters

| Variable | Description |
|--------|------------|
| x | Original NO₂ value |
| z | Transformed value |
| p̂(z) | Predicted probability |

---

## 4. Mathematical Formulation

### Non-Linear Transformation

z = x + aᵣ sin(bᵣ x)

where  
aᵣ = 0.05 × (r mod 7)  
bᵣ = 0.3 × (r mod 5 + 1)  

r is the university roll number.

---

### Probability Density Function

p̂(z) = c · exp(−λ (z − μ)²)

---

## 5. Result Table

| Parameter | Meaning | Value |
|---------|--------|-------|
| μ | Mean of transformed data | Computed |
| λ | Spread parameter | Computed |
| c | Normalization constant | Computed |

---

## 6. Result Graph

A histogram of the transformed variable z is plotted along with the learned probability density function. The graph shows a close fit between the empirical distribution and the learned model.

---

## 7. Observations

- Non-linear transformation increases data variability
- Learned PDF successfully models the transformed data
- Roll-number parameterization ensures uniqueness

---

## 8. Conclusion

This assignment demonstrates the application of non-linear transformations and probabilistic modeling to learn a valid probability density function from real-world air quality data.

---

## 9. Tools Used

- Google Colab  
- Python  
- NumPy  
- Pandas  
- Matplotlib  

---

## 10. Repository Structure

Assignment03  
│── Learn_PDF_using_Nonlinear_Model.ipynb  
│── README.md  
│── india_air_quality_data.csv  

---

## 11. Execution Platform

- Google Colab
- GitHub
