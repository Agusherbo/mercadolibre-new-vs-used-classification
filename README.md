# Mercado Libre - New vs Used Item Classification  
<img src="Assets/ml_foto_1.png" alt="Mercado Libre" width="200"/> 

## Descripción

Este proyecto aborda el desafío de Mercado Libre de construir un modelo de Machine Learning capaz de predecir si un producto publicado en el marketplace es **"new" (nuevo)** o **"used" (usado)**, a partir de un dataset de publicaciones.

## Estructura del Repositorio

```
mercadolibre-new-vs-used-classification/

├── Assets/
│   └── ml_foto_1
├── DataSets/
│   └── MLA_100k_train_32_fields.xlsx
├── Diccionario de datos/
│   └── Diccionarios.xlsx
├── Informe/
│     └── Informe Final.pdf
├── Notebooks/
│   └── Notebook_Full_Project.ipynb
│   └── Feature Criteria Selection
├── outputs/
│   ├── classification_report.jpg
│   ├── confusion_matrix.png
│   └── feature_importance.png
├── Raw_data/
│   └── MLA_100k_checked_v3.jsonlines
│   └── new_or_used.py
├── README.md
└── requirements.txt
```

## Cómo Ejecutar la Solución

1. **Clonar el Repositorio:**

```bash
git clone https://github.com/AgusHerbo/mercadolibre-new-vs-used-classification.git
cd mercadolibre-new-vs-used-classification
```

2. **Instalar Dependencias:**

```bash
pip install -r requirements.txt
```

3. **Ejecutar el Notebook Principal:** Abrir el archivo `Notebook_Full_Project.ipynb` en JupyterLab o VSCode y seguir la secuencia de celdas.

## Resultados Obtenidos

* **Accuracy (Test Set):** 86.8%
* **F1-Score (Weighted):** 86.7%
* **Modelo Utilizado:** XGBoostClassifier

Los resultados completos se encuentran en:

* `outputs/classification_report.txt`
* `outputs/confusion_matrix.png`
* `outputs/feature_importance.png`

## Feature Engineering

* Variables numéricas: `sold_quantity`, `base_price`, `price`, etc.
* Variables categóricas: `listing_type_id`, `seller_profile_type`, `buying_mode`.
* Variables textuales: TF-IDF sobre `title`.
* Creación de columnas derivadas: `is_official_store`, `has_used_in_title`, entre otras.

## Secondary Metric: F1-Score (Weighted)

Se seleccionó el **F1-Score (Weighted Average)** como métrica secundaria por su capacidad de balancear precisión y recall, clave en un contexto donde predecir incorrectamente la condición del producto puede impactar la experiencia de usuario.

## Herramientas Utilizadas

* Python 3.12
* XGBoost
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn
* JupyterLab

## Resumen Ejecutivo

Ver el archivo `Informe/Informe_Final.pdf` para una explicación detallada de la solución, criterios de selección de features, justificación de la métrica secundaria y resultados obtenidos.

## Contacto

Agustín Herbozo. \[heerbozo@gmail.com]

---

**Nota:** Los datos completos no han sido subidos por razones de confidencialidad. El pipeline está preparado para recibir datasets en formato JSONLines.
