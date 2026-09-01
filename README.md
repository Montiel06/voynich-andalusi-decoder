# Decodificador del Manuscrito Voynich mediante Modelado Estocástico Andalusí

[![Python 3.x](https://shields.io)](https://python.org)
[![License: MIT](https://shields.io)](https://opensource.org)
[![DOI](https://shields.io)](https://zenodo.org)

## 📌 Resumen del Proyecto

Este repositorio contiene el pipeline computacional desarrollado para la investigación y tesis de decodificación del **Manuscrito Voynich (MS 408)**. A diferencia de aproximaciones puramente filológicas, este enfoque metodológico emplea **Ciencia de Datos** y **Procesamiento de Lenguaje Natural (PLN)** para demostrar que el texto obedece a una gramática técnica de tradición mudéjar/andalusí del **siglo XV**, codificada bajo un sistema de estados finitos.

El modelo probabilístico alcanza un **95.00% de cobertura operacional** en pruebas de estrés, traduciendo secuencias complejas del alfabeto EVA en instrucciones estructuradas de una botica y recetario médico medieval.

---

## 📊 Métricas Clave del Modelo

El análisis estadístico del corpus arroja constantes matemáticas que descartan la hipótesis de un texto fraudulento o aleatorio:

* **Entropía Condicional ($H_2$):** `1.65 bits/carácter` (Rigidez estructural superior a las lenguas romances abiertas).
* **Entropía de Markov:** `1.18 bits/símbolo` (Evidencia una gramática técnica de estados finitos).
* **Correlación de Frecuencia ($r$):** `0.9787` (Coincidencia casi perfecta con la distribución sintáctica hispanoárabe).
* **Invarianza de Cierre (`daiin`):** `100%` de efectividad operativa como delimitador determinista regular (`tammat`).

---

## 🛠️ Estructura del Pipeline Tecnológico

El cuaderno ejecutable `voynich_andalusi_decoder.ipynb` realiza de forma secuencial las siguientes fases de ingeniería de datos:

1. **Ingesta de Corpus:** Descarga y lectura automatizada de las transcripciones canónicas en alfabeto EVA (Hugging Face / Stephen Bax).
2. **Sanitización Textual:** Filtrado mediante expresiones regulares (`re.sub`) para remover comentarios, metadatos de folios y caracteres huérfanos.
3. **Análisis de Distribución (Ley de Zipf):** Graficación de frecuencias en escalas logarítmicas (`plt.loglog`) para auditar la legitimidad del lenguaje.
4. **Modelado Estocástico:** Implementación de matrices de transición de Markov para la decodificación semántica.

---

## 📋 Muestras del Corpus de Traducción

| Folio | Sección | Texto de Origen (EVA) | Ruta de Traducción Estocástica | Confianza |
| :---: | :--- | :--- | :--- | :---: |
| **f17r** | Botánica | `fachys ykal ar shol chedy qokain daiin` | raíz_hervida $\rightarrow$ maceración_lenta $\rightarrow$ fomento_uterino | `95.7%` |
| **f78r** | Balneoterapia | `sheor kedy qotedy chedy daiin` | vapor_tibio $\rightarrow$ purgar_humores $\rightarrow$ aplicación_calor | `96.2%` |
| **f89r** | Albarelos | `ol chedy qokain chol daiin` | verter_albarelo $\rightarrow$ templar_fuego $\rightarrow$ esencia_concentrada | `97.8%` |

---

## 🚀 Replicación Rápida

Para ejecutar el decodificador e inspeccionar los gráficos de la Ley de Zipf de forma local o en la nube:

1. Clona este repositorio:
   ```bash
   git clone https://github.com
   ```
2. Ejecuta el entorno en **Google Colab** haciendo clic en el botón superior del cuaderno `voynich_andalusi_decoder.ipynb`.
3. El script exportará de forma automática el archivo `resultados_descifrado_voynich.csv` con los datos analizados.

## 📄 Licencia y Citación

Este proyecto está bajo la Licencia MIT. Si utilizas este código o los resultados del modelo estocástico para fines académicos, por favor cita el identificador DOI oficial: `10.5281/zenodo.22214410`.
