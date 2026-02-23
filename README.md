# Uso de Ecobici en la Ciudad de Buenos Aires


El sistema **Ecobici** en la Ciudad de Buenos Aires genera un volumen masivo de datos transaccionales diariamente. Más allá de ser un servicio de transporte, representa un ecosistema logístico complejo donde la eficiencia operativa (disponibilidad de bicicletas) dicta la calidad del servicio y la satisfacción del usuario.

## Objetivo


El objetivo de este análisis no fue solo visualizar trayectos, sino responder a preguntas críticas de negocio y planificación: ¿Cómo podemos optimizar la distribución de las bicis y sus estaciines? ¿Hay cuellos de botella? ¿Cómo cuantificamos el impacto ambiental para reportes de sustentabilidad (ESG)?

## Solución


Para transformar estos datos en *insights*, se implementó un flujo de análisis integral:

- **Data Cleansing y Transformación (Power BI & Python):** Normalización bases de datos históricas con formatos dispares (2015-2024). Utilicé **Python** para construir lógicas de eventos de entrada/salida y calcular con precisión los "quiebres de stock" (minutos en que una estación permanecía sin bicicletas).  El codigo puede verse en mi github:
- **Modelado de Datos:** Se implementó un esquema de estrella (Star Schema) desnormalizando dimensiones de estaciones para facilitar el análisis geoespacial de origen y destino.
- **Cálculos DAX Avanzados:** Se crearonmedidas personalizadas para calcular tiempos promedio, proyecciones de impacto ambiental (CO2 ahorrado) y conteo dinámico de eventos críticos.
- **Visualización Ejecutiva:** Armado un dashboard interactivo en **Power BI** enfocado en KPIs de disponibilidad, demografía y sustentabilidad.


## Conclusión


 A través del modelo, logramos identificar *insights* accionables para la toma de decisiones:

- 📈 **Detección de Cuellos de Botella:** Se comprobó que el sistema tiene una buena salud general (5 min. promedio sin bicis), pero nodos clave como Constitución y Palermo sufren desabastecimientos críticos (más de 30 minutos), lo que exige una redistribución logística dinámica en esos puntos.

- 🌱 **Cuantificación de Sustentabilidad:** El sistema evitó la emisión de más de 2 millones de Kg de CO2 en un año, equivalente a salvar 96 mil árboles, un dato vital para la justificación de presupuestos de inversión gubernamental o reportes ESG corporativos.

- 🔮 **Visión a Futuro:** Los datos estructurados sientan las bases para implementar modelos predictivos de demanda basados en clima y franjas horarias.

🚀Te invito a pasar por mi portfolio para interactuar con el reporte: https://nahuel-facello.super.site/
