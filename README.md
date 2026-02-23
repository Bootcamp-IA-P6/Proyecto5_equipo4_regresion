## 🩺 Simulador Integrado de Esperanza de Vida: Un Enfoque Multimodelo

¿Es posible predecir cuántos años viviremos basándonos en factores socioeconómicos y de salud? Este proyecto nace de esa pregunta, utilizando los datos globales de la Organización Mundial de la Salud (OMS) para construir una herramienta analítica capaz de simular diversos escenarios demográficos.

### 📖 La Historia del Proyecto

Nuestro equipo se enfrentó al desafío de analizar un dataset complejo con variables que van desde el PIB de un país hasta sus tasas de vacunación de Polio. Para abordar este reto, dividimos la investigación en 4 bloques estratégicos:

- Colaboración Modular: Cada integrante del equipo asumió la responsabilidad de responder a 2 preguntas de investigación específicas del dataset.

- Análisis Individual (EDA): Se realizaron limpiezas y análisis exploratorios personalizados en notebooks independientes (partially), asegurando que cada variable fuera comprendida a fondo.

- Modelado y Pickling: Cada bloque de análisis culminó en un modelo de regresión entrenado, los cuales fueron exportados mediante joblib en formato .pkl para su reutilización.

- La Gran Integración: Finalmente, unimos todas las piezas en un cerebro central: version_completed.ipynb, donde reside nuestra lógica de predicción y el simulador interactivo.

### 🛠️ Arquitectura del Repositorio

Para mantener la escalabilidad y facilitar la futura dockerización, hemos seguido una estructura de carpetas limpia y profesional:

```
PROYECTO_ML/
├── data/               # Ciclo de vida del dato
│   ├── processed/      # Dataset limpio listo para modelos
│   └── raw/            # Datos originales de la OMS (Kaggle)
├── models/             # Cerebros del proyecto (archivos .pkl)
│   ├── modelo_q1..q4.pkl
│   └── models_metadata.pkl
├── notebooks/          # Laboratorio de experimentación
│   ├── complete/       # Notebook final integrado (version_completed.ipynb)
│   └── partially/      # EDAs individuales por integrante
├── src/                # Scripts de soporte (lógica modular)
├── .python-version     # Gestión de versión con UV
├── pyproject.toml      # Configuración de dependencias
├── uv.lock             # Bloqueo de dependencias para reproducibilidad
└── README.md           # Estás aquí
```

### 🚀 El Producto Final: El Simulador

Nuestra calculadora no es un modelo estático; es una herramienta de simulación orientada al cliente.

Características principales:
- Selección de Modelo: Permite elegir entre modelos específicos (ej. Random Forest) o una visión integrada.
- Ajuste en Tiempo Real: Mediante sliders y filtros, el usuario puede modificar variables como el Gasto en Salud, PIB per cápita, o Años de Escolaridad.
- Predicción Dual: Capacidad de contrastar resultados entre diferentes algoritmos con un solo clic.

### ⚙️ Configuración y Uso

Gestión de Entorno con UV
Este proyecto utiliza UV para una gestión de paquetes ultrarrápida. Para replicar el entorno:

Instala UV si no lo tienes.

Sincroniza el entorno:
```Bash
uv sync
```

Activa el entorno virtual:
```Bash
source .venv/bin/activate  # En Linux/Mac
.venv\Scripts\activate     # En Windows
```

### 🧪 Tecnologías Utilizadas

- Lenguaje: Python
- Gestión de Dependencias: UV
- Análisis de Datos: Pandas, Numpy
- Visualización: Matplotlib, Seaborn
- Machine Learning: Scikit-learn, Joblib (para persistencia de modelos)
- Notebooks: Jupyter

---
### Colaboradores: 
- Joaquin Lazaro
- Iris Amorim
- Isabel Rodriguez
- Mar Izquierdo
