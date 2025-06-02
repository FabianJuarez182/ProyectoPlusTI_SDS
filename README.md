# ProyectoPlusTI_SDS

# 💳 Detección de Fraude en Comercios con Baja Frecuencia de Transacciones

## 🎯 Objetivo

Optimizar la detección de fraudes en comercios con baja actividad (pocas transacciones), lo cual representa un desafío por la escasez de datos y la dificultad para identificar patrones consistentes.

Este proyecto forma parte del curso **Security Data Science**, y se enfoca en diseñar funciones de evaluación personalizadas para modelos de clasificación con LightGBM, priorizando la reducción de falsos positivos manteniendo alta la capacidad de detección.

---

## 🧠 Metodología

1. **Análisis exploratorio de datos (EDA)**: evaluación del desbalance, distribución de variables, y comportamiento por comercio.
2. **Ingeniería de características**: creación de nuevas variables que capturen patrones de fraude, con énfasis en los comercios poco activos.
3. **Modelo base con LightGBM**: entrenamiento inicial para establecer una línea base de rendimiento.
4. **Diseño de funciones personalizadas (`feval`)**: definición e implementación de tres métricas distintas centradas en la mejora de detección en comercios con baja frecuencia.
5. **Evaluación final**: comparación de las métricas propuestas, justificación de la función seleccionada y análisis del tradeoff entre detección y falsos positivos.

---

## 📁 Estructura del Proyecto

    📦 proyecto-fraude/
    │
    ├── 📓 PlusTI.ipynb # Notebook principal con todo el análisis
    ├── 📊 dataset_feature_engineering.csv # Dataset enriquecido con nuevas variables
    ├── 📄 README.md # Este archivo

## ⚙️ Requisitos

- Python 3.8+
- Jupyter Notebook
- Bibliotecas:
  - pandas
  - numpy
  - seaborn
  - matplotlib
  - scikit-learn
  - lightgbm

Instalación:
```bash
pip install -r requirements.txt
```

📌 Resultados Relevantes
    
    ⚠️ Desbalance extremo de clases: solo ~0.52% de las transacciones son fraude.
    🏪 Comercios con < 100 transacciones tienen alta proporción de falsos positivos.
    📈 Métrica personalizada permitió mejorar el recall de fraudes en comercios de baja actividad sin sacrificar excesivamente la precisión.

📍 Conclusión
    
    Este proyecto demuestra cómo adaptar la evaluación de modelos para escenarios difíciles, como detectar fraude en comercios poco frecuentes. La clave está en diseñar funciones de evaluación que reflejen objetivos reales del negocio.

👨‍💻 Autor
    
    Fabian Juarez Curso: Security Data Science · 2025