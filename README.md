# dentix_mora_xgboost

Repositorio con el flujo completo para modelar mora crediticia ≥30 días con XGBoost, incluyendo limpieza, análisis multivariado, PCA, KMeans, LDA y calibración de umbrales.

---

## Carpetas del proyecto

### 1) limpieza_y_datos
Esta carpeta contiene la base original tal como se recibió y el notebook donde se generó la base limpia final.

Contenido:
- Base_Dentix_anonimizada.xlsx  → datos brutos sin procesar
- limpieza_codificación.ipynb   → limpieza, tratamiento, codificación y generación de BD_numericas.xlsx
- .gitkeep

Desde aquí se realizó el preprocesamiento inicial.

---

### 2) modelado_y_experimentos
Aquí se trabaja únicamente con la base final ya procesada.  
No es necesario limpiar ni transformar nuevamente.

Contenido:
- BD_numericas.xlsx  → dataset limpio listo para modelar
- 3_analisis.ipynb  → correlaciones, covarianzas y PCA
- 4_5_6_modelo_inicial.ipynb  → modelos base (Logística, Árbol de decisión)
- Parte_7_8_9_XGBoost_Kmeans_LDA.ipynb  → modelo XGBoost calibrado + KMeans + LDA
- XGBOOST_modelo_prueba.ipynb  → uso experimental del algoritmo
- .gitkeep

---

## Flujo recomendado de uso

1. Si se quiere replicar la generación del dataset limpio:
   Ejecutar `limpieza_codificación.ipynb` desde la carpeta `limpieza_y_datos`.

2. Si ya se va directo a modelar:
   Usar `BD_numericas.xlsx` en la carpeta `modelado_y_experimentos`
   y ejecutar los notebooks en orden natural (primero análisis → luego modelos).

---

El repositorio permite reproducir todo el pipeline:  
datos crudos → limpieza → estructura numérica → análisis → modelado → calibración → segmentación e interpretación.
