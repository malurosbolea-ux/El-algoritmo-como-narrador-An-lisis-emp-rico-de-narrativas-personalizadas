# 🎭 El Algoritmo como Narrador

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange.svg)](https://jupyter.org/)

> **Análisis Empírico de Narrativas Personalizadas en Sistemas de Recomendación**
> 


---

## 📖 Descripción

Este proyecto investiga cómo los algoritmos de recomendación actúan como "narradores" activos, construyendo mundos de contenido personalizados y divergentes para diferentes perfiles de usuario. A través de técnicas avanzadas de Procesamiento del Lenguaje Natural (PLN) y análisis de sentimiento, demuestro empíricamente que estos sistemas no son simples filtros pasivos, sino arquitectos de realidades mediáticas distintas.

### 🎯 Pregunta de Investigación Central

**¿Qué "mundo narrativo" le presenta el algoritmo a un usuario interesado en política frente a uno interesado en estilo de vida?**

---

## ✨ Características Principales

- 📊 **Análisis comparativo** de 209,527 artículos de noticias
- 🤖 **Modelo predictivo** con 93.92% de precisión (Regresión Logística)
- 📈 **Visualizaciones interactivas** desarrolladas con D3.js y Chart.js
- 🎨 **Dashboard analítico** profesional con métricas clave
- 🕸️ **Red de co-ocurrencias** para explorar conexiones narrativas
- 💬 **Análisis de sentimiento** cuantitativo por perfil

---

## 🎨 Visualizaciones Interactivas

### 1. Word Cloud Comparativo
Visualización de las palabras más frecuentes en cada mundo narrativo, mostrando la separación radical entre los vocabularios de Política y Lifestyle.

![Word Cloud](assets/viz_wordcloud.png)

### 2. Dashboard Analítico
Panel interactivo con métricas clave: distribución de sentimiento, palabras más frecuentes, evolución temporal y rendimiento del modelo predictivo.

![Dashboard](assets/viz_dashboard.png)

### 3. Red de Conexiones Narrativas
Grafo interactivo que muestra las co-ocurrencias entre palabras clave, revelando cómo se estructuran semánticamente los dos mundos.

![Red de Narrativas](assets/viz_red.png)

---

## 🛠️ Tecnologías Utilizadas

### Análisis de Datos
- **Python 3.8+**: Lenguaje principal
- **Pandas**: Manipulación de datos
- **NumPy**: Operaciones numéricas
- **Scikit-learn**: Machine Learning y modelado predictivo

### Procesamiento del Lenguaje Natural
- **NLTK**: Tokenización y procesamiento de texto
- **spaCy**: Análisis lingüístico avanzado
- **Gensim**: Modelado de temas (LDA)
- **VADER**: Análisis de sentimiento

### Visualización
- **Matplotlib & Seaborn**: Gráficos estáticos
- **Plotly**: Visualizaciones interactivas
- **D3.js**: Visualizaciones web dinámicas
- **Chart.js**: Gráficos canvas HTML5

### Presentación
- **Tableau**: Dashboards profesionales
- **Figma**: Diseño de presentación interactiva
- **Power BI**: Análisis visual de datos

---

## 📂 Estructura del Proyecto

```
el-algoritmo-como-narrador/
│
├── data/                          # Datasets utilizados
│   ├── news_category_dataset.json # Dataset principal (209,527 artículos)
│   └── youtube_trending.csv       # Dataset secundario (fase 1)
│
├── notebooks/                     # Jupyter Notebooks con análisis
│   ├── 01_exploratory_analysis.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_sentiment_analysis.ipynb
│   ├── 04_topic_modeling.ipynb
│   └── 05_predictive_model.ipynb
│
├── src/                           # Código fuente Python
│   ├── preprocessing.py           # Limpieza y preprocesamiento
│   ├── sentiment.py               # Análisis de sentimiento
│   ├── modeling.py                # Modelos predictivos
│   └── visualization.py           # Utilidades de visualización
│
├── visualizations/                # Visualizaciones interactivas HTML
│   ├── wordcloud_comparativo.html
│   ├── red_narrativas.html
│   └── dashboard_comparativo.html
│
├── assets/                        # Recursos multimedia
│   ├── viz_wordcloud.png
│   ├── viz_dashboard.png
│   └── viz_red.png
│
├── docs/                          # Documentación del proyecto
│   ├── el_algoritmo_como_narrador.docx
│   └── presentacion_figma.pdf
│
├── requirements.txt               # Dependencias Python
├── README.md                      # Este archivo
└── LICENSE                        # Licencia MIT

```

---

## 🚀 Instalación y Uso

### Requisitos Previos
- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Jupyter Notebook (opcional, para explorar los análisis)

### Paso 1: Clonar el Repositorio
```bash
git clone https://github.com/malu-ros/el-algoritmo-como-narrador.git
cd el-algoritmo-como-narrador
```

### Paso 2: Crear Entorno Virtual (Recomendado)
```bash
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

### Paso 3: Instalar Dependencias
```bash
pip install -r requirements.txt
```

### Paso 4: Descargar Recursos NLTK
```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('vader_lexicon')
```

### Paso 5: Ejecutar los Notebooks
```bash
jupyter notebook
```

Navega a la carpeta `notebooks/` y abre los archivos `.ipynb` en orden secuencial.

---

## 📊 Resultados Principales

### 1. Divergencia Temática
Los dos perfiles operan con vocabularios **mutuamente excluyentes**:
- **Política**: Trump, Obama, Senate, Congress, Republicans, Democrats
- **Lifestyle**: Show, Movie, Music, Star, Actor, Season

### 2. Divergencia Emocional
Las atmósferas emocionales son **opuestas**:
- **Política**: 38.3% Negativo | 35.3% Neutral | 26.3% Positivo
- **Lifestyle**: 29.2% Negativo | 35.5% Neutral | 35.4% Positivo

### 3. Prueba Predictiva
El modelo de clasificación alcanzó una **precisión del 93.92%**, demostrando que las narrativas son matemáticamente predecibles.

| Métrica | Política | Lifestyle |
|---------|----------|-----------|
| Precisión | 97.9% | 87.1% |
| Recall | 95.8% | 92.3% |
| F1-Score | 96.8% | 89.6% |

---

## 🎓 Metodología

### Fase 1: Recolección de Datos
- **Dataset**: News Category Dataset (HuffPost)
- **Periodo**: 2012-2022 (10 años)
- **Volumen**: 209,527 artículos
- **Fuente**: Kaggle

### Fase 2: Preprocesamiento
1. Eliminación de duplicados (13 filas)
2. Filtrado de outliers (títulos <3 o >30 palabras)
3. Tokenización y limpieza de texto
4. Lematización con spaCy

### Fase 3: Análisis Exploratorio
- Análisis de distribución de palabras
- Identificación de categorías relevantes
- Validación de calidad del dataset

### Fase 4: Creación de Perfiles
- **Perfil Política**: Categoría POLITICS
- **Perfil Lifestyle**: Categorías ENTERTAINMENT + WELLNESS

### Fase 5: Análisis Comparativo
1. **Análisis de Sentimiento** (VADER)
2. **Modelado de Temas** (LDA con Gensim)
3. **Modelo Predictivo** (Regresión Logística)
4. **Extracción de Características** (TF-IDF)

### Fase 6: Visualización y Comunicación
- Desarrollo de visualizaciones interactivas
- Creación de dashboard analítico
- Elaboración de presentación Figma

---

## 📈 Hallazgos Clave

### 🔍 Hallazgo 1: Separación Lingüística Total
No existe **ninguna palabra** que aparezca significativamente en ambos perfiles. Los algoritmos han aprendido que estos dominios operan con vocabularios mutuamente excluyentes.

### 💭 Hallazgo 2: Ingeniería Emocional Algorítmica
El algoritmo **amplifica** la valencia emocional específica de cada dominio:
- Política → Conflicto, indignación (Negativo: 38.3%)
- Lifestyle → Aspiración, bienestar (Positivo: 36.8%)

### 🎯 Hallazgo 3: Burbujas Predecibles
La precisión del 93.92% demuestra que las burbujas de contenido son **matemáticamente separables** y lingüísticamente predecibles.


---

## 📚 Referencias

1. **Datasnaek.** (2018). *Trending YouTube Video Statistics* [Dataset]. Kaggle. [https://www.kaggle.com/datasets/datasnaek/youtube-new](https://www.kaggle.com/datasets/datasnaek/youtube-new)

2. **O'Neil, C.** (2017). *Armas de destrucción matemática: El poder de los algoritmos en la era de las redes sociales*. Taurus.

3. **Pariser, E.** (2017). *El filtro burbuja: Cómo la red decide lo que leemos y lo que pensamos*. Taurus.

4. **Reuters Institute.** (2021). *Digital News Report*. [https://reutersinstitute.politics.ox.ac.uk/digital-news-report](https://reutersinstitute.politics.ox.ac.uk/digital-news-report)

---

## 👩‍💻 Autora

**María Luisa Ros Bolea **

Data Science & AI | Digital Communication  
Máster en Big Data e Inteligencia Artificial - CEU San Pablo

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maría-luisa-ros-bolea-400780160/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/malurosbolea-ux)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://marialuisarosboleaportfolio.my.canva.site/porfolio-profesional-mar-a-luisa-ros-bolea-actualizado)


---


---


<div align="center">

### ⭐ Si este proyecto te resulta útil o interesante, ¡considera darle una estrella! ⭐

**Construido con ❤️ y ☕ en Madrid, España**

</div>
