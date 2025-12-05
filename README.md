# dentix_mora_xgboost
Repositorio con scripts de análisis, PCA, clustering, calibración de umbrales, LDA, KMeans y modelo XGBoost optimizado para predicción de mora crediticia.

Este repositorio contiene el desarrollo completo para predecir mora >30 días, incluyendo limpieza de datos, análisis multivariado, modelado supervisado, segmentación y calibración.

## Carpetas

### limpieza_y_datos
Contiene la base original sin procesar:
- Base_Dentix_anonimizada.xlsx

Desde aquí se realizó la depuración y transformación de datos para generar la base numérica usada posteriormente.

### modelado_y_experimentos
Carpeta donde se ejecuta todo el modelado.
Incluye la base ya lista para usar y los notebooks del proyecto:

- BD_numericas.xlsx (dataset limpio final)
- 3_analisis.ipynb
- 4_5_6_modelo_inicial.ipynb
- Parte_7_8_9_XGBoost_Kmeans_LDA.ipynb
- XGBOOST_modelo_prueba.ipynb

## Uso

1. Si se requiere repetir la limpieza, usar la base cruda en `limpieza_y_datos/`.
2. Para correr modelos directamente, cargar `BD_numericas.xlsx` desde `modelado_y_experimentos/` y ejecutar los notebooks.
