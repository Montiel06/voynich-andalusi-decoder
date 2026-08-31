# voynich-andalusi-decoder
### Modelo Computacional y Gramática Técnica del Recetario Médico Andalusí (Siglo XV)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22214410.svg)](https://doi.org/10.5281/zenodo.22214410)

Repositorio oficial del pipeline computacional para el análisis estocástico, sintáctico y semántico del Beinecke MS 408 (Manuscrito Voynich).

**Autora:** Vanessa Montiel Ruiz  
**Línea de Investigación:** Criptología Histórica, Humanidades Digitales y Medicina Medieval Hispanoárabe  
**DOI Oficial:** [10.5281/zenodo.22214410](https://doi.org/10.5281/zenodo.22214410)

---

## Contenido del Repositorio
- `VOYNICH.ipynb`: Cuaderno de Google Colab reproducible con las pruebas estadísticas y de traducción.
- `reporte_descifrado_andalusi.md`: Memoria metodológica detallada y fundamentos paleográficos.
- `voynich_modelo_matematico_final.txt`: Matrices de transición de Markov y métricas de entropía de Shannon.
- `voynich_traducciones_validadas.txt`: Corpus de folios procesados de punta a punta (`f1r`, `f17r`, `f70v`, `f71v`, `f78r`, `f79r`, `f86v`, `f89r`, `f107r`).
- `dictamen_descifrado_voynich.pdf`: Dictamen epistemológico y límites de validación científica.

---

## Métricas Clave del Modelo
- **Entropía Condicional:** $H_2 = 1.65$ bits/carácter (inferior a lenguas romances abiertas).
- **Entropía de Markov:** $1.18$ bits/símbolo (Gramática técnica de estados finitos).
- **Correlación de Frecuencia:** $r = 0.9787$.
- **Invarianza de Cierre:** `daiin` = 100% como delimitador determinista (*tammat*).
- **Cobertura en Prueba de Estrés:** 95.00% de tokens funcionales mapeados.

---

## Replicación Rápida
Ejecutar el cuaderno en Google Colab o en un entorno Python 3.9+:
```python
import zipfile
with zipfile.ZipFile("corpus_voynich_andalusi.zip", "r") as z:
    z.extractall(".")

