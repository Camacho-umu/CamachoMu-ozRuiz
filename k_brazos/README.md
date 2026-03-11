# Parte 1: Problema del Bandido de k-Brazos

## Descripción

Estudio comparativo de tres algoritmos de decisión secuencial — **ε-greedy**, **UCB1** y **Softmax** — aplicados al problema del bandido de k-brazos con distribuciones Normal, Bernoulli y Binomial.

Se analiza el compromiso exploración-explotación y la influencia de los hiperparámetros (ε, c, τ) en el rendimiento de cada algoritmo, medido mediante recompensa promedio, porcentaje de selección del brazo óptimo, regret acumulado y estadísticas por brazo.

## Estructura

```
k_brazos/
├── main.py                               # Función run_experiment y ejecución base
├── estudio_comparativo.ipynb             # Comparativa global: los 3 algoritmos en las 3 distribuciones
├── estudio_comparativo_normal.ipynb      # Estudio detallado con brazos Normal(μ, σ)
├── estudio_comparativo_bernoulli.ipynb   # Estudio detallado con brazos Bernoulli(p)
├── estudio_comparativo_binomial.ipynb    # Estudio detallado con brazos Binomial(n, p)
├── src/
│   ├── algorithms/                       # Implementaciones de los algoritmos
│   │   ├── algorithm.py                  # Clase base Algorithm
│   │   ├── epsilon_greedy.py             # ε-greedy
│   │   ├── ucb1.py                       # UCB1
│   │   └── softmax.py                    # Softmax (Boltzmann)
│   ├── arms/                             # Distribuciones de brazos
│   │   ├── arm.py                        # Clase base Arm
│   │   ├── armnormal.py                  # Brazo Normal
│   │   ├── armbernoulli.py               # Brazo Bernoulli
│   │   ├── armbinomial.py                # Brazo Binomial
│   │   └── bandit.py                     # Clase Bandit (gestiona k brazos)
│   └── plotting/                         # Funciones de visualización
│       └── plotting.py                   # Gráficas comparativas
├── tests/
│   ├── test_task2.py                     # Tests de ε-greedy y run_experiment
│   └── test_task3.py                     # Tests de UCB1 y Softmax
├── docs/                                 # Documentación adicional
└── data/                                 # Datos (si aplica)
```

## Notebooks

| Notebook | Contenido |
|---|---|
| `estudio_comparativo.ipynb` | Comparativa global: barrido de hiperparámetros + comparativa final con los mejores valores para cada distribución |
| `estudio_comparativo_normal.ipynb` | Análisis detallado con brazos Normal: efecto de ε, c y τ; comparativa calibrada |
| `estudio_comparativo_bernoulli.ipynb` | Análisis con brazos Bernoulli: recompensas en {0, 1}, calibración de UCB1 y Softmax |
| `estudio_comparativo_binomial.ipynb` | Análisis con brazos Binomial(n, p): efecto de n en la riqueza de señal, escalado de hiperparámetros |

## Configuración experimental

| Parámetro | Valor |
|---|---|
| Brazos (k) | 10 |
| Pasos (T) | 1000 – 5000 |
| Ejecuciones | 300 – 500 |
| Semilla | 442 |

## Ejecución

### En Google Colab

Los notebooks incluyen las celdas de setup necesarias para clonar el repositorio e importar los módulos.

### En local

```bash
cd k_brazos
pip install numpy matplotlib seaborn
python main.py              # Ejecución base con ε-greedy
jupyter notebook            # Para abrir los estudios comparativos
```

## Algoritmos implementados

- **ε-greedy**: con probabilidad ε explora aleatoriamente; con 1-ε explota el brazo con mayor Q estimado.
- **UCB1**: selecciona el brazo que maximiza $Q(a) + c\sqrt{\frac{\ln t}{N(a)}}$, equilibrando estimación e incertidumbre.
- **Softmax**: selecciona brazos proporcionalmente a $\frac{e^{Q(a)/\tau}}{\sum_b e^{Q(b)/\tau}}$, controlando exploración con la temperatura τ.
