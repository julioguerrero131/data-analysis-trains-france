# 🚅 Análisis de Eficiencia Operativa: Red Ferroviaria Francesa

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Status](https://img.shields.io/badge/Status-Completado-green)
![Libraries](https://img.shields.io/badge/Librerías-Pandas%20%7C%20Seaborn%20%7C%20Matplotlib-orange)

## 📋 Descripción del Proyecto
Este proyecto realiza un **Análisis Exploratorio de Datos (EDA)** sobre el tráfico ferroviario en Francia (SNCF). El objetivo principal fue diagnosticar las causas raíz de los retrasos y cancelaciones, así como identificar cuellos de botella en la infraestructura para proponer puntos de mejora operativa.

Se analizaron datos históricos que incluyen rutas, tiempos de viaje, causas de retraso y volumen de pasajeros.

## 🛠️ Tecnologías Utilizadas
* **Python**: Lenguaje principal. Entorno Google Colab.
* **Pandas**: Limpieza y manipulación de datos (Data Wrangling).
* **Matplotlib & Seaborn**: Visualización de datos y storytelling.

## 📂 Acceso al Dataset
* **Fuente:** Kaggle - Public transport traffic data in France
* **Descarga:** [Link Kaggle](https://www.kaggle.com/datasets/gatandubuc/public-transport-traffic-data-in-france)

## 📊 Metodología
1.  **Preprocesamiento:**
    * Limpieza de valores nulos.
    * Conversión de tipos de datos (Fechas, Flotantes).
    * Ingeniería de características: Creación de métricas como *Tasa de Cancelación* e *Índice de Severidad*.
2.  **Análisis de Correlación:** Descarte de hipótesis nulas sobre saturación de tráfico.
3.  **Análisis Temporal:** Detección de estacionalidad en retrasos.
4.  **Auditoría de Causas:** Clasificación de incidencias (Internas vs. Externas).

## 🔍 Hallazgos Clave (Business Insights)

### 1. El mito de las Causas Externas
Contrario a la creencia popular, el **73.3% de los retrasos** son responsabilidad directa de la gestión interna (Infraestructura, Material Rodante, Gestión de tráfico). Solo el 26.7% se debe a factores externos (clima, huelgas).

### 2. Rigidez del Sistema ("Efecto Bola de Nieve")
Se descubrió que la red carece de elasticidad. Los datos muestran que **un tren que sale tarde, llega aún más tarde**. No existe capacidad de recuperación de tiempo durante el trayecto.

### 3. Cuellos de Botella Críticos
Las estaciones **Paris Lyon** y **Paris Montparnasse** acumulan más del triple de incidencias que cualquier otra estación, actuando como embudos que afectan a toda la red nacional.

> ![Top Estaciones](images/pregunta1.png)
> *Gráfica 1: Estaciones con mayor tasa de cancelación.*

## 🚀 Cómo ejecutar este proyecto
### Opción 1: Google Colab (Recomendado)
1. Haz clic en el botón **"Open in Colab"** de arriba.
2. Descarga el archivo `Regularities_by_liaisons_Trains_France.csv` desde el link o del repositorio.
3. En Colab, ve al panel izquierdo (Archivos) y sube el CSV a la sesión.
4. Ejecuta todas las celdas.

### Opción 2: Localmente
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/julioguerrero131/data-analysis-trains-france.git](https://github.com/julioguerrero131/data-analysis-trains-france.git)
2. Instalar dependencias:
    ```bash
    pip install -r requirements.txt
3. Coloca el archivo CSV descargado en la carpeta `data/`.
4. Abre el notebook con Jupyter.
