# Sistema Híbrido de Recomendación de Recetas Saludables

Este repositorio contiene el desarrollo completo del proyecto descrito en el paper **"Sistemas Híbridos de Recomendación de Recetas Saludables y Personalizadas"**, donde se exploran modelos clásicos, híbridos y de aprendizaje profundo aplicados al dominio culinario, con énfasis en salud, diversidad y personalización.

> ⚠️ Todo el código está preparado para ejecutarse directamente en **Google Colab**, sin necesidad de configuración local.

---

##  Estructura del Repositorio

```
├── analysis/
│   └── main.ipynb
├── baselines/
│   ├── random.ipynb
│   └── KNN_foodcom.ipynb
├── model/
│   ├── lightfm_foodcom.ipynb
│   ├── lightfm_meal.ipynb
│   ├── deepfm_foodcom.ipynb
│   └── v1-v2-v3.ipynb (Experiments)
└── README.md
```

---

## Análisis Inicial (`/analysis/`)

Contiene el notebook `main.ipynb` donde se realiza una exploración comparativa de tres datasets candidatos. A partir de este análisis, se seleccionaron:

- **Food.com**: dataset denso con ratings y metadatos de ingredientes, útil para evaluar modelos colaborativos y modelos profundos como DeepFM.
- **MealRecPlus**: dataset enriquecido con etiquetas nutricionales (FSA, WHO) y semántica de contenido (ingredientes y tags), ideal para LightFM con características híbridas.

---

##  Modelos Base (`/baselines/`)

Implementaciones simples para establecer un punto de referencia:

- `random_predictor.ipynb`: modelo aleatorio.
- `knn_lightfm.ipynb`: filtrado colaborativo basado en vecinos, descartado por bajo rendimiento.

---

## Modelos Avanzados (`/model/`)

Cada notebook es **autosuficiente** y reproduce los experimentos del paper:

- `lightfm_foodcom.ipynb`: LightFM puro y con metadatos en Food.com.
- `lightfm_meal.ipynb`: LightFM con y sin metadatos (FSA/WHO) en MealRecPlus,  incluye recomendación híbrida controlada por tags nutricionales (ej. vegetariano, alto en proteína).
- `deepfm_foodcom.ipynb`: implementación de DeepFM que logra los mejores resultados en precisión.

Cada notebook contiene:

- Métricas: Precision\@K, Recall\@K, Diversity\@K, Novelty\@K.
- Gráficos y análisis de sensibilidad de hiperparámetros.
- Ejemplos de recomendaciones generadas.

---

## Paper Asociado

Este repositorio acompaña el paper **"Sistemas Híbridos de Recomendación de Recetas Saludables y Personalizadas"** (formato ICML 2025). Todo el código es reproducible y está alineado con los resultados presentados.

---
Todos los notebooks pueden ejecutarse directamente desde **Google Colab**. 
---

