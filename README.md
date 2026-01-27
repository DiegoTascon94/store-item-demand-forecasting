# Store & Item Demand Forecasting

## 📌 Contexto del negocio
En entornos de retail y consumo masivo, una predicción inexacta de la demanda puede generar quiebres de stock, sobreinventario y pérdidas operativas. Este proyecto aborda el problema de **pronosticar la demanda diaria por tienda y producto**, con el objetivo de apoyar decisiones de planeación, abastecimiento y optimización operativa.


## 🎯 Objetivo del proyecto
Desarrollar un modelo de predicción de demanda confiable y estable que permita:
- Anticipar el comportamiento de ventas a nivel tienda–producto.
- Reducir la incertidumbre en la planificación de inventarios.
- Facilitar decisiones de negocio basadas en datos históricos y patrones temporales.


## 📊 Principales insights del análisis
- La demanda presenta una **alta concentración en pocas tiendas y productos**, confirmando un patrón tipo Pareto.
- Existen productos con **alta variabilidad**, lo que requiere estrategias diferenciadas de reposición.
- La demanda se mantiene **estable a lo largo de la semana**, sin sesgos significativos en fines de semana.
- El error del modelo se mantiene bajo incluso en periodos de mayor volumen de ventas.


## 🤖 Modelo y métricas
Se entrenó un modelo de **Random Forest Regressor** utilizando variables temporales, rezagos y promedios móviles.

**Resultados principales:**
- Demanda diaria promedio: **52.25 unidades**
- MAE (Error promedio): **6.26 unidades**
- RMSE: **8.15 unidades**
- Error relativo estimado: **≈12%**

El 95% de las predicciones se mantiene por debajo de una desviación de 16.5 unidades, evidenciando un desempeño consistente y confiable.


## 📈 Impacto en decisiones de negocio
A partir del análisis y el modelo desarrollado, este proyecto permite:
- Ajustar inventarios de forma proactiva según la demanda esperada.
- Identificar productos críticos que requieren mayor control operativo.
- Reducir costos asociados a sobrestock y quiebres de inventario.
- Brindar soporte analítico a equipos de operaciones, supply chain y planificación comercial.


## 🛠️ Tecnologías utilizadas
- Python
- Pandas & NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook


## 📂 Estructura del repositorio
```
store-item-demand-forecasting/
│
├── data/               # Datos de entrada (Kaggle)
├── notebooks/          # Análisis y modelado
├── src/                # Funciones auxiliares (opcional)
├── README.md           # Documentación del proyecto
├── requirements.txt    # Librerías utilizadas
└── .gitignore
```

## 🚀 Conclusión
El proyecto demuestra cómo un enfoque analítico sólido y orientado al negocio puede transformar datos históricos en **insights accionables**, permitiendo mejorar la toma de decisiones y fortalecer la eficiencia operativa en entornos de retail y consumo masivo.

