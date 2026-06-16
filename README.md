# Comparación de Modelos de Aprendizaje Automático: Clasificación de Salud Fetal

## 📄 Descripción del Proyecto
Este proyecto tiene como objetivo analizar y comparar diferentes algoritmos de Machine Learning aplicados a la clasificación del estado de salud fetal (Normal, Sospechoso o Patológico). Basándonos en datos extraídos mediante cardiotocografía (CTG), buscamos determinar cuál de los modelos predice con mayor exactitud y eficacia la salud del feto, facilitando así una posible intervención médica oportuna para prevenir la mortalidad materno-fetal.

El estudio compara el rendimiento del algoritmo base seleccionado en Kaggle (**Random Forest Classifier**) frente a dos modelos alternativos: **K-Nearest Neighbors (KNN)** y el potente ensamble **XGBoost Classifier**.

## 📂 Estructura del Proyecto
```text
ai-fetal-health-actividad12/
├── main.ipynb                              # 🌟 Notebook principal con la solución y resultados solicitados en la actividad
├── main2.ipynb                             # Notebook extendido que incluye gráficos y Análisis Exploratorio de Datos (AED)
├── fetal_health.csv                        # Dataset original extraído de Kaggle
├── fetal-health-classification.ipynb       # Notebook de referencia del autor original
├── Quispe Bartolo - (09-2) Actividad...    # Rúbrica e instrucciones de la Actividad 12
├── test_models.py                          # Script de prueba rápida de los modelos
└── README.md                               # Este archivo de documentación
```
> **Nota Importante:** El archivo `main.ipynb` es el documento central que contiene la **solución del proyecto**. Allí se responde a todas las preguntas de la rúbrica y se encuentra la ejecución y el análisis comparativo de los tres algoritmos.

## 🚀 Instalación y Configuración del Entorno (con `uv`)

Este proyecto utiliza **`uv`**, un empaquetador y gestor de proyectos de Python extremadamente rápido escrito en Rust. A continuación, se detalla paso a paso cómo instalarlo y configurarlo en el proyecto.

### 1. Instalar `uv`
Abre tu terminal (PowerShell en el caso de Windows) y ejecuta el siguiente comando:

- **En Windows (PowerShell):**
  ```powershell
  irm https://astral.sh/uv/install.ps1 | iex
  ```
- **En macOS o Linux:**
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

### 2. Crear el Entorno Virtual
Navega a la carpeta raíz del proyecto (`ai-fetal-health-actividad12`) en tu terminal y crea un entorno virtual aislado para el proyecto:
```bash
uv venv
```
*(Esto generará una carpeta oculta llamada `.venv` donde se alojará tu instalación de Python).*

### 3. Activar el Entorno Virtual
Para utilizar e instalar paquetes en el entorno recién creado, debes activarlo:
- **En Windows:**
  ```powershell
  .venv\Scripts\activate
  ```
- **En macOS o Linux:**
  ```bash
  source .venv/bin/activate
  ```

### 4. Instalar las Dependencias Necesarias
Con tu entorno virtual activado (notarás que dice `(.venv)` al inicio de tu línea de comandos), instala todas las librerías requeridas mediante el gestor de paquetes veloz de uv:
```bash
uv pip install pandas scikit-learn xgboost matplotlib seaborn jupyter ipykernel
```

**Lista de dependencias y su utilidad en el proyecto:**
- `pandas` y `numpy` : Manipulación, lectura del CSV y estructuración de datos.
- `scikit-learn` : Creación de Pipelines, algoritmos base (KNN, Random Forest), escalado de características y cálculo de métricas (Accuracy, F1-Score).
- `xgboost` : Provee el poderoso algoritmo Gradient Boosting Extremo.
- `matplotlib` y `seaborn` : Creación de matrices de confusión, mapas de calor y gráficos de barras (presentes en `main2.ipynb`).
- `jupyter` e `ipykernel` : Soporte necesario para visualizar y ejecutar de manera iterativa los archivos `.ipynb` en el editor.

### 5. Ejecutar los Notebooks
Una vez instalado todo, puedes abrir `main.ipynb` desde Visual Studio Code u otro editor y ejecutar las celdas asegurándote de seleccionar el **Kernel de Python** alojado en `.venv`.

Alternativamente, si prefieres lanzar Jupyter desde la línea de comandos, usa:
```bash
uv run jupyter notebook
```