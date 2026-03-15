# Extensiones de Machine Learning — Informe Técnico

## Información

- **Alumnos:** Camacho, Francisco Jesus; Muñoz, Adrian; Ruiz, Rodrigo
- **Asignatura:** Extensiones de Machine Learning
- **Curso:** 2025/2026
- **Grupo:** CamachoMuñozRuiz

## Descripción

Informe técnico de la asignatura Extensiones de Machine Learning del Máster en Inteligencia Artificial (UMU). El trabajo aborda dos grandes bloques:

1. **Problema del Bandido de k-brazos**: estudio comparativo de los algoritmos ε-greedy, UCB1 y Softmax sobre distribuciones Normal, Bernoulli y Binomial.
2. **Aprendizaje en Entornos Complejos**: técnicas tabulares y aproximadas de Aprendizaje por Refuerzo (pendiente de desarrollo).

## Estructura

```
CamachoMuñozRuiz/
├── informe.pdf               # Informe técnico
├── README.md                 # Este fichero
├── k_brazos/                 # Parte 1: Bandido de k-brazos
│   ├── src/                  # Código fuente (.py)
│   │   ├── algorithms/       # Implementación de ε-greedy, UCB1 y Softmax
│   │   ├── arms/             # Distribuciones de brazos (Normal, Bernoulli, Binomial)
│   │   └── plotting/         # Funciones de visualización
│   ├── tests/                # Tests unitarios
│   ├── docs/                 # Documentación adicional
│   ├── data/                 # Datos (si aplica)
│   ├── main.py               # Función run_experiment y ejecución base
│   ├── estudio_comparativo.ipynb           # Comparativa global de los 3 algoritmos
│   ├── estudio_comparativo_normal.ipynb    # Estudio específico: distribución Normal
│   ├── estudio_comparativo_bernoulli.ipynb # Estudio específico: distribución Bernoulli
│   ├── estudio_comparativo_binomial.ipynb  # Estudio específico: distribución Binomial
│   └── README.md
└── Entornos_Complejos/       # Parte 2: Aprendizaje por Refuerzo
    ├── Metodos_aproximados/
    │   ├── videos/
    │   ├── DQN.ipynb
    │   └── SEMIGRADIENTSARSA.ipynb
    ├── Metodos_tabulares/
    │   ├── MonteCarloOn_policyOff_policy_presentacion.ipynb
    │   └── TD_Diferencias_Temporales_presentacion.ipynb
    ├── main.ipynb
    └── README.md  
```

## Instalación y Uso

### Ejecución en Google Colab

Cada notebook incluye las celdas iniciales necesarias para clonar el repositorio e instalar las dependencias automáticamente.


## Tecnologías Utilizadas

- **Lenguaje:** Python 3.10+
- **Librerías principales:** NumPy, Matplotlib, Seaborn
- **Entorno de notebooks:** Jupyter / Google Colab
- **Control de versiones:** Git + GitHub

## Declaración sobre el uso de Inteligencia Artificial

En este proyecto se han utilizado herramientas de Inteligencia Artificial como asistencia técnica para optimizar el flujo de trabajo y la redacción. Detallamos su uso a continuación:

* **Asistencia en programación (GitHub Copilot / LLMs):** Se han utilizado como apoyo durante la escritura de código en Python. Su uso se ha centrado en el autocompletado de estructuras repetitivas, sugerencias de refactorización para mejorar la legibilidad y asistencia en la resolución de errores puntuales (como la prevención de inestabilidad numérica en el algoritmo Softmax).
* **Documentación y maquetación (ChatGPT / Claude / Gemini):** Se han empleado modelos de lenguaje para la revisión ortográfica y gramatical, la estructuración de la documentación en formato Markdown y como soporte para la maquetación del informe técnico final en LaTeX.

Es importante destacar que el uso de estas herramientas se ha limitado estrictamente a labores de asistencia. El diseño experimental, la implementación de la lógica algorítmica, el barrido de hiperparámetros y el análisis crítico de los resultados son trabajo original de los autores. 

Todo el código y texto generado con apoyo de IA ha sido revisado, probado y validado por el equipo, asumiendo la total responsabilidad sobre el correcto funcionamiento y la precisión del resultado final del proyecto.
