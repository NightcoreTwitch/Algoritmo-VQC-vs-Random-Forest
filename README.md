# ⚛️ Análisis Comparativo: Variational Quantum Classifier (VQC) vs. Random Forest

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Qiskit](https://img.shields.io/badge/Qiskit-Machine%20Learning-purple)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Classic-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📋 Descripción del Proyecto

Este repositorio contiene la implementación y el análisis crítico de un *Clasificador Cuántico Variacional (VQC)* comparado con un algoritmo clásico estándar (*Random Forest*) en un problema de clasificación binaria supervisada.

El proyecto fue desarrollado como parte de la asignatura *Fundamentos de la Computación Cuántica* para evaluar la viabilidad de los algoritmos cuánticos híbridos en la era *NISQ* (Noisy Intermediate-Scale Quantum).

### 🎯 Objetivo
Determinar si un modelo VQC, simulado en hardware clásico y bajo restricciones de datos (Few-Shot Learning), puede competir en precisión y convergencia contra métodos clásicos maduros en datos tabulares reales.

---

## 👥 Autores (Grupo 3)

* *Anaís Del Valle*
* *Gabriel Cruz*
* *Bayron Cruz*

*Institución:* Universidad Católica del Norte (UCN)  
*Asignatura:* Fundamentos de la Computación Cuántica

---

## 📂 Estructura del Repositorio

* notebook_proyecto.ipynb: Jupyter Notebook con todo el código (Preprocesamiento, VQC, RF y Gráficos).
* customers_Tarea8_45a23b390495309b721db16b4bfcd169.csv: Dataset utilizado (Marketing Bancario).
* README.md: Este archivo.

---

## 🛠️ Tecnologías e Implementación

El proyecto utiliza un enfoque híbrido Cuántico-Clásico:

1.  *Preprocesamiento:* * Limpieza de datos con Pandas.
    * Codificación One-Hot y Estandarización.
    * *PCA (Principal Component Analysis):* Reducción de dimensionalidad a 4 componentes para mapeo directo a 4 Qubits.
2.  *Modelo Cuántico (VQC):*
    * Librería: Qiskit Machine Learning.
    * Feature Map: ZZFeatureMap (Entrelazamiento).
    * Ansatz: RealAmplitudes.
    * Optimizador: COBYLA.
3.  *Modelo Clásico:*
    * Algoritmo: RandomForestClassifier de Scikit-Learn.

---

## 📊 Resultados Principales

Se realizó un experimento controlado entrenando ambos modelos con un subconjunto estratificado de *200 muestras* para evaluar la eficiencia de aprendizaje.

| Modelo | Precisión (Accuracy) | Observación |
| :--- | :--- | :--- |
| *Random Forest (Clásico)* | *90%* | Alta convergencia y robustez con pocos datos. |
| *VQC (Cuántico)* | *55%* | Dificultad de entrenamiento debido a Barren Plateaus. |

*Conclusión clave:* El experimento demostró la supremacía actual de los algoritmos clásicos para datos tabulares estructurados. El bajo rendimiento del VQC se atribuye a las limitaciones de optimización en paisajes de costo planos (Mesetas Estériles) y no a la falta de datos.

---

## 🚀 Instrucciones de Ejecución

Para correr este código en tu máquina local o Colab, necesitas las siguientes dependencias:

```bash
pip install qiskit qiskit-machine-learning qiskit-algorithms scikit-learn pandas matplotlib
