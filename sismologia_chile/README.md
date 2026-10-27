# Análises y Modelamiento de Sismología en Chile (CSN)

**Carrera / Área:** Escuela de Informática y Telecomunicaciones — Duoc UC  
**Track:** Ciencia de Datos — CITT  
**Repositorio:** `track-ciencia-datos-citt`  
**Directorio de Proyecto:** `sismologia_chile/`  

---

## 📌 Descripción del Proyecto

Este proyecto aborda la extracción, procesamiento, análisis exploratorio (EDA) y modelamiento predictivo de la actividad sismológica en Chile, utilizando como fuente primaria los registros del **Centro Sismológico Nacional (CSN)** de la Universidad de Chile (`evtdb.csn.uchile.cl`).

El objetivo principal es identificar patrones espacio-temporales en la magnitud y profundidad de los eventos telúricos, así como aplicar técnicas de regresión (incluyendo modelamiento polinomial) para analizar la relación entre las variables geográficas y la magnitud de los sismos.

---

## 🎯 Hipótesis y Objetivos

* **Hipótesis:** Existe una correlación no lineal entre la profundidad sísmica, la ubicación geográfica (latitud/longitud en la zona de subducción) y la magnitud de los eventos registrados en el territorio chileno.
* **Objetivo General:** Desarrollar un pipeline modular de datos en Python que automatice desde la extracción web (*scraping*) hasta el entrenamiento de modelos descriptivos/predictivos.
* **Objetivos Específicos:**
  1. Extraer de forma automatizada y estructurada el histórico de eventos del portal del CSN.
  2. Implementar un almacenamiento estandarizado bajo reglas de gobernanza CITT (`data/raw/`).
  3. Realizar un análisis exploratorio de datos (EDA) para limpiar imprecisiones y evaluar distribuciones.
  4. Entrenar modelos de regresión lineal y polinomial evitando el fuga de datos (*data leakage*).

---

## 🛠️ Estructura del Proyecto (Gobernanza CITT)

El repositorio sigue la plantilla estandarizada de proyectos para el track de Ciencia de Datos:

```text
sismologia_chile/
├── data/
│   ├── raw/          <- Datos crudos extraídos directamente mediante Web Scraping (sismos_csn_raw.csv)
│   ├── processed/    <- Datos limpios y transformados listos para análisis
│   └── final/        <- Datasets finales consumidos por los modelos
├── notebooks/        <- Jupyter Notebooks versionados (ej. 1.0-eda.ipynb)
├── src/              <- Scripts modulares en Python (.py) para extracción y procesamiento
├── references/       <- Diccionarios de datos y documentación técnica complementaria
└── README.md         <- Documentación general del proyecto y resultados
