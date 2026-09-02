# Decodificación Operacional del Manuscrito Voynich (MS 408)
> Pipeline computacional para el análisis estocástico y ontológico del corpus EVA aplicado a protocolos farmacoterapéuticos del siglo XV.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22214410.svg)](https://doi.org/10.5281/zenodo.22214410)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Resumen Metodológico
Este repositorio contiene el código fuente y los datasets utilizados para auditar la estructura determinista del Manuscrito Voynich:
- **Entropía de Shannon de 2º orden:** $H_2 = 1.65\text{ bits/carácter}$.
- **Cadenas de Markov:** Verificación empírica de transiciones unigramas/bigramas que demuestran una sintaxis estenográfica formal no aleatoria.
- **Función delimitadora:** Comportamiento de sumidero estocástico del token `daiin` como cierre invariable de prescripción (*tammat*).

## Resultados Clave
El modelo de transición muestra una clara direccionalidad operacional y una fuerte convergencia hacia estados de terminación técnica:

![Matriz de Transición de Markov](figures/markov_transitions.png)

## Reproducibilidad
Para ejecutar los análisis sin dependencias locales, abre el cuaderno en Colab haciendo clic en el botón superior o sigue estos pasos localmente:
```bash
git clone [https://github.com/tu-usuario/voynich-andalusi-pipeline.git](https://github.com/tu-usuario/voynich-andalusi-pipeline.git)
cd voynich-andalusi-pipeline
pip install -r requirements.txt
python -m notebook notebook/voynich_pipeline.ipynb
