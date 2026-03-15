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
