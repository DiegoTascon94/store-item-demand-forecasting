# 📈 Predicción de Demanda: Optimización de Inventarios en Retail

## 🎯 Contexto del Negocio
En el sector de consumo masivo, una predicción inexacta de la demanda genera costos ocultos masivos: quiebres de stock que resultan en ventas perdidas y sobreinventario que inmoviliza capital. Este proyecto aborda el desafío de **pronosticar la demanda diaria para 50 productos en 10 tiendas distintas**, permitiendo una planificación logística de precisión.

## 🚀 Objetivo del Proyecto
Desarrollar un modelo de Machine Learning capaz de anticipar el comportamiento de ventas a nivel tienda–producto para:
- Optimizar los ciclos de reabastecimiento.
- Reducir la incertidumbre operativa en la cadena de suministro.
- Maximizar la disponibilidad de producto en anaquel.

## 📊 Alcance del Análisis
* **Datos:** 5 años de registros históricos de transacciones diarias.
* **Feature Engineering:** Creación de variables temporales (día de la semana, mes, año), rezagos (lags) y promedios móviles para capturar la estacionalidad.
* **Granularidad:** Análisis detallado por SKU y ubicación geográfica.

## 💡 Principales Insights (EDA)
* **Patrón de Pareto:** Alta concentración del volumen de ventas en un grupo selecto de tiendas y productos críticos.
* **Estabilidad Semanal:** La demanda no presenta sesgos extremos en fines de semana, lo que facilita una logística de reposición lineal.
* **Variabilidad por Categoría:** Se identificaron SKUs con alta volatilidad que requieren un "stock de seguridad" mayor que el promedio.

## 🛠️ Enfoque Analítico y Modelo
Se implementó un modelo de **Random Forest Regressor**, seleccionado por su capacidad para manejar relaciones no lineales y su robustez ante valores atípicos.
* **Métricas de Rendimiento:**
  - **MAE (Error Medio Absoluto):** 6.26 unidades (Precisión excepcional frente a una media de 52).
  - **RMSE:** 8.15 unidades.
  - **Error Relativo:** ≈12%.
  - **Confiabilidad:** El 95% de las predicciones tienen una desviación menor a 16.5 unidades.

## 🧠 Impacto en Decisiones de Negocio
* **Planificación Proactiva:** El modelo permite pasar de una logística reactiva a una basada en demanda esperada.
* **Reducción de Costos:** Minimización de costos de almacenamiento por exceso de stock.
* **Soporte Comercial:** Herramienta clave para los equipos de compras y planificación de la demanda (Demand Planning).

## 💻 Tecnologías y Herramientas
* **Lenguaje:** Python
* **ML Stack:** Scikit-learn, Pandas, NumPy.
* **Visualización:** Matplotlib, Seaborn.

## 📂 Estructura del Repositorio
```text
├── data/               # Datasets históricos (Train/Test)
├── notebook/           # Análisis exploratorio y entrenamiento del modelo
├── README.md           # Documentación estratégica
└── requirements.txt    # Dependencias del entorno
```

## ▶️ Cómo Ejecutar el Proyecto
* **Clonar el repositorio:** git clone [https://github.com/DiegoTascon94/store-item-demand-forecasting.git](https://github.com/DiegoTascon94/store-item-demand-forecasting.git)

* **Instalar dependencias:** pip install -r requirements.txt

* **Explorar el modelo:** Abrir notebook/ para revisar el proceso de entrenamiento y validación.

## 📝 Conclusiones
Este proyecto demuestra cómo el Machine Learning puede transformar datos históricos en una ventaja competitiva, reduciendo el error humano en la previsión y asegurando que el producto correcto esté en el lugar correcto en el momento adecuado.

## 🔮 Próximos Pasos / Mejoras Futuras
* **Modelos Avanzados:** Implementar algoritmos de Gradient Boosting (XGBoost o LightGBM) para mejorar la captura de tendencias a largo plazo y estacionalidades complejas.
* **Incorporación de Exógenos:** Integrar datos de feriados, eventos climáticos y promociones para refinar la precisión en fechas especiales.