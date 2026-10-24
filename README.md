# Movilidad urbana y productividad económica en ciudades de LATAM

Análisis realizado en el curso de Análisis de Datos de TripleTen (Sprint 5: *Prepara y estructura datos con Python*).

El objetivo es responder: **¿qué relación existe entre la movilidad urbana (congestión, tiempos de viaje) y la productividad económica (PIB per cápita) en ciudades de Latinoamérica?**

## 📂 Contenido del repositorio

```
everpeak-analysis/
├── notebooks/
│   └── latam_mobility_analysis.ipynb   # Notebook principal del análisis
└── README.md
```

## ▶ Cómo abrir el notebook en Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/katerinemoronb/everpeak-analysis/blob/main/notebooks/latam_mobility_analysis.ipynb)

O bien:

1. Abre `notebooks/latam_mobility_analysis.ipynb` en GitHub.
2. Haz clic en **Open in Colab**.

## 🗃️ Datos utilizados

- **tomtom_traffic.csv**: más de 1 millón de registros de tráfico (retraso por congestión, índice de tráfico, tiempos de viaje por cada 10 km).
- **oecd_city_economy.csv**: indicadores económicos por ciudad (PIB per cápita, desempleo, PM2.5 y población).

> Los datasets pertenecen a la plataforma de TripleTen y no se incluyen en este repositorio. El notebook conserva las salidas de cada celda para poder revisar el análisis sin volver a ejecutarlo.

## 🛠️ Metodología

1. Carga y exploración de ambos datasets (`info()`, `head()`).
2. Estandarización de nombres de columnas a snake_case.
3. Conversión de fechas a `datetime` y limpieza de valores numéricos (separadores, comas decimales, `%`).
4. Filtro del año 2024 y promedios de tráfico por ciudad.
5. Unión INNER de tráfico y economía por `city` y `year`.
6. Visualizaciones: boxplot de congestión, histograma del PIB per cápita y gráfico de barras comparativo.
7. Exportación del dataset final `ladb_mobility_economy_2024_clean.csv` y resumen ejecutivo.

## 🧠 Hallazgos principales

- Se analizaron **15 ciudades de 7 países** con datos de 2024.
- No se observa una relación clara entre PIB per cápita y congestión: Ciudad de México combina PIB alto con la mayor congestión, mientras que Montevideo y Buenos Aires tienen PIB alto y congestión baja o moderada.
- **Bogotá** aparece como ciudad prioritaria para inversión en infraestructura de transporte: congestión alta y el PIB per cápita más bajo entre Bogotá, Lima y Buenos Aires.

## 🧰 Herramientas

Python · pandas · NumPy · matplotlib · seaborn · Google Colab
