# Práctica IA (RA4 · b+c) — Big Data, análisis, rentabilidad y valoración IA

## 1) Caso y objetivo de negocio
- Empresa/sector (real o ficticia):Cadena de comercio electrónico de moda (“FashionNow”, e-commerce internacional).
- Problema a resolver:Baja tasa de conversión y muchas visitas que no terminan en compra.
- Objetivo de negocio (rentabilidad):Aumentar ventas y valor medio del carrito mediante recomendaciones personalizadas y optimización de precios. 

## 2) Big Data: recogida masiva de datos
Describe por qué es Big Data (volumen, velocidad, variedad).
- Fuente 1:Logs de navegación web y app (páginas vistas, clics, tiempo en página, búsquedas internas).
- Fuente 2:Historial de compras, devoluciones y tickets de soporte.
- Fuente 3:Datos externos: campañas de marketing, redes sociales, datos agregados de tendencias.
- Volumen/velocidad (estimación):Decenas de millones de eventos al día, datos en tiempo casi real (segundos/minutos).
- Formatos (texto, eventos, series temporales, imágenes, etc.):Eventos de clic (series temporales), texto (búsquedas, reseñas), tablas transaccionales, imágenes de productos.

## 3) Tratamiento/análisis: pipeline de datos
Explica el flujo de forma ordenada:
- Ingesta (captura/eventos):Captura de eventos de navegación mediante trackers en web/app y conectores a la base de datos transaccional y CRM.
- Limpieza/normalización:Eliminación de duplicados, corrección de formatos de fecha, unificación de identificadores de usuario/dispositivo, tratamiento de valores nulos.
- Almacenamiento (data lake/warehouse):Data lake en almacenamiento en la nube (parquet/objetos) y data warehouse columnar para analítica y reporting.
- Preparación de variables (features):Cálculo de recencia, frecuencia y valor (RFM), categorías favoritas, sensibilidad al precio, probabilidad de abandono, contexto (dispositivo, hora, país).
- Análisis/BI (opcional):Cuadros de mando de ventas, funnels de conversión, análisis de cohortes y segmentación de clientes.

## 4) IA aplicada: modelo y decisión
- Tipo de IA/técnica (clasificación, predicción, recomendación, anomalías, NLP...):Sistema de recomendación (modelos de recomendación híbridos) y modelo de predicción de probabilidad de compra.
- Entrada del modelo (qué datos usa):Historial de navegación, compras anteriores, características de los productos, contexto (hora, dispositivo, canal), segmentación del cliente.
- Salida del modelo (qué produce):Lista ordenada de productos recomendados y probabilidad de compra o de clic para cada usuario en cada sesión.
- Decisión que habilita (qué hace la empresa con esa salida):Decisión que habilita (qué hace la empresa con esa salida):Personalizar la página de inicio, el carrusel de productos, los emails y las notificaciones push para mostrar los productos con mayor probabilidad de conversión.

## 5) Rentabilidad: KPIs antes/después (mínimo 3)
KPI 1 (ingresos/coste/eficiencia):
- Antes:2,0 % de las sesiones terminan en compra.
- Después:2,8 % de las sesiones terminan en compra.
- Por qué mejora la rentabilidad:Con el mismo tráfico se generan más pedidos, aumentando los ingresos sin incrementar proporcionalmente el gasto en marketing.

KPI 2:
- Antes:45 € por pedido.
- Después:52 € por pedido.
- Por qué mejora la rentabilidad:Las recomendaciones cruzadas (cross-selling) y complementarias (upselling) hacen que el cliente añada más productos o de mayor precio.

KPI 3:
- Antes:Alto CAC porque se depende mucho de campañas de pago para captar nuevos clientes.
- Después:CAC efectivo menor gracias a mayor recurrencia y mejor monetización de clientes existentes.
- Por qué mejora la rentabilidad:Se aprovecha mejor cada cliente captado, aumentando el LTV (valor de vida del cliente) y reduciendo la presión sobre el presupuesto de marketing.



## 6) Diagrama del pipeline (ASCII o Mermaid)
flowchart LR
    A[Usuarios web/app] --> B[Ingesta de eventos<br/>logs de clics, vistas, búsquedas]
    C[Base de datos transaccional<br/>compras, devoluciones] --> B
    B --> D[Limpieza y normalización]
    D --> E[Data Lake]
    E --> F[Data Warehouse / ETL]
    F --> G[Feature Engineering<br/>RFM, segmentos, contexto]
    G --> H[Modelo IA<br/>Recomendación y predicción]
    H --> I[API de recomendaciones]
    I --> J[Front web/app<br/>página personalizada]
    F --> K[BI / Dashboards<br/>KPIs de negocio]


## 7) Riesgos y mitigación
Riesgo 1:Dependencia excesiva de datos personales y posible incumplimiento de privacidad (RGPD).
- Mitigación 1:Aplicar anonimización y seudonimización, minimizar datos, obtener consentimientos claros, auditorías de cumplimiento y políticas de retención de datos.

Riesgo 2:Sesgos en las recomendaciones (sobreexposición de ciertos productos o marcas, burbuja de contenido).
- Mitigación 2:Monitorizar la diversidad de recomendaciones, introducir reglas de negocio (exploración), revisar periódicamente el modelo y combinar métricas de negocio con métricas de equidad.

## 8) Valoración (criterio c): importancia presente y futura de la IA (10–15 líneas)
- Importancia actual (hoy):Hoy la IA en e-commerce es un factor diferencial clave: permite personalizar la experiencia, mejorar la conversión y competir frente a grandes plataformas globales. Las empresas que no usan IA en recomendaciones, segmentación o pricing suelen quedar en desventaja.
- Importancia futura (3–5 años):En los próximos años la IA será todavía más central, con modelos más contextuales y multimodales (texto, imagen, voz) que integrarán todo el recorrido del cliente. La frontera ya no será “usar o no IA”, sino la calidad de los datos, la rapidez de despliegue y la capacidad de integrar IA en todos los procesos.
- Condiciones/limitaciones (datos, costes, regulación, ética, seguridad, empleo):El éxito depende de disponer de datos suficientes, de calidad y bien gobernados. Los costes de infraestructura en la nube y de talento especializado pueden ser elevados, especialmente para pymes. Además, la regulación (como el RGPD y futuras normas de IA) exigirá transparencia, explicabilidad y seguridad. Éticamente, habrá que evitar manipulación excesiva, respetar la privacidad y gestionar el impacto en el empleo, orientando a los equipos hacia tareas de mayor valor añadido.
- Conclusión razonada:La IA aplicada al Big Data en este caso no es solo una mejora técnica, sino una palanca estratégica de competitividad y rentabilidad. Las empresas que inviertan en datos, modelos y gobernanza responsable podrán ofrecer experiencias más relevantes, optimizar recursos y adaptarse mejor a un entorno cambiante. Quedarse fuera de esta transformación implicará perder cuota de mercado frente a competidores más data-driven.



## 9) Fuentes oficiales (mín. 2)
- Big Data/analítica (enlace oficial):https://www.ibm.com/analytics/big-data-analytics (ibm.com in Bing)
https://data.europa.eu
- IA/técnica/modelo (enlace oficial):https://developers.google.com/machine-learning/recommendation (developers.google.com in Bing)
https://openai.com/research (investigación general en modelos de IA)

