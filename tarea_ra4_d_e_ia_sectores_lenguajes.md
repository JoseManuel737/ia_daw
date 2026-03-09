# Práctica IA (RA4 · d+e) — Sectores con implantación relevante y lenguajes de programación en IA

## 1) Introducción
- Objetivo de la práctica:Conocer en qué sectores se aplica la IA, qué lenguajes se usan y cómo se relaciona con el desarrollo de software (DAW/DAM).
- Relación con DAW/DAM:La IA se integra en aplicaciones web y de escritorio/móvil, por lo que es clave que perfiles DAW/DAM entiendan qué tecnologías, lenguajes y patrones se usan para diseñar, consumir y desplegar servicios de IA.

## 2) Sectores con implantación relevante de IA

### Sector 1
- Nombre del sector:Sanidad / Salud digital
- Tipo de empresa/servicio:Hospitales, clínicas, empresas de telemedicina
- Aplicación de IA:Sistemas de apoyo al diagnóstico (imágenes médicas, análisis de datos clínicos)
- Qué tarea mejora o automatiza:Detección temprana de enfermedades, clasificación de imágenes (radiografías, TAC, etc.)
- Por qué la IA tiene implantación relevante en este sector:Maneja grandes volúmenes de datos médicos y ayuda a reducir errores humanos y tiempos de diagnóstico.
- Beneficios que aporta:Mayor precisión diagnóstica, reducción de costes, mejor atención al paciente y priorización de casos urgentes.

### Sector 2
- Nombre del sector:Banca y finanzas
- Tipo de empresa/servicio:Bancos, fintech, aseguradoras
- Aplicación de IA:Detección de fraude, scoring de riesgo, chatbots para atención al cliente
- Qué tarea mejora o automatiza:Análisis de transacciones, evaluación de solvencia, respuesta automática a consultas frecuentes
- Por qué la IA tiene implantación relevante en este sector:El sector maneja datos sensibles y transacciones masivas donde la detección rápida de anomalías es crítica.
- Beneficios que aporta:Menos fraude, decisiones de crédito más rápidas, mejor experiencia de usuario y optimización de procesos internos.

### Sector 3
- Nombre del sector:Comercio electrónico / Retail online
- Tipo de empresa/servicio:Tiendas online, marketplaces, plataformas de servicios
- Aplicación de IA:Sistemas de recomendación, personalización de contenido, predicción de demanda
- Qué tarea mejora o automatiza:Recomendación de productos, segmentación de clientes, gestión de inventario
- Por qué la IA tiene implantación relevante en este sector:La personalización aumenta ventas y fidelización, y la predicción mejora la logística y el stock.
- Beneficios que aporta:Incremento de ventas, mejor experiencia de compra, reducción de roturas de stock y optimización de campañas de marketing.

## 3) Lenguajes de programación en IA

### Lenguaje 1
- Nombre: Python
- Uso principal en IA:Machine learning, deep learning, ciencia de datos, prototipado rápido
- Ventajas:Gran ecosistema de librerías (TensorFlow, PyTorch, scikit-learn), comunidad enorme, sintaxis sencilla
- Ejemplos de uso:Modelos de clasificación, redes neuronales, APIs de IA integradas en aplicaciones web.

### Lenguaje 2
- Nombre:R
- Uso principal en IA:Análisis estadístico, modelos predictivos, visualización de datos
- Ventajas:Muy fuerte en estadística, muchas librerías para análisis de datos, integración con entornos de investigación
- Ejemplos de uso:Modelos de regresión, análisis exploratorio de datos, informes de datos para negocio.

### Lenguaje 3
- Nombre:Java
- Uso principal en IA:Integración de modelos en sistemas empresariales, aplicaciones backend escalables
- Ventajas:Rendimiento, robustez, multiplataforma, usado en grandes empresas; existen librerías de ML (DL4J, Weka)
- Ejemplos de uso:Sistemas de recomendación en grandes plataformas, motores de decisión integrados en microservicios.

### Lenguaje 4
- Nombre:JavaScript / TypeScript
- Uso principal en IA:Integración de IA en aplicaciones web y front-end, consumo de APIs de IA
- Ventajas:Corre en el navegador y en el servidor (Node.js), ideal para DAW, fácil integración con servicios REST/GraphQL
- Ejemplos de uso:Chatbots en páginas web, paneles que consumen modelos de IA vía API, interfaces interactivas para modelos de recomendación.

## 4) Relación entre sectores, tipo de IA y lenguaje
Sector	Aplicación de IA	Tipo de IA/técnica	Lenguaje recomendado	Justificación
Sanidad	Diagnóstico por imagen	Deep learning, visión por computador	Python	Amplio soporte en librerías de visión y redes neuronales.
Banca y finanzas	Detección de fraude y scoring	Machine learning supervisado	Python / Java	Python para modelado; Java para integración en sistemas críticos.
Comercio electrónico	Recomendación de productos y personalización	Sistemas de recomendación, ML	Python / JavaScript	Python para entrenar modelos; JS para integrarlos en la web (DAW).

## 5) Diagrama (ASCII o Mermaid)
flowchart LR
    A[Datos del sector] --> B[Entrenamiento modelo IA]
    B --> C[Modelo desplegado en servidor]
    C --> D[Aplicación DAW/DAM]
    D --> E[Usuario final]

    subgraph Lenguajes
        P[Python: entrenamiento]
        J[Java/JS: integración]
    end

    B --- P
    C --- J


## 6) Riesgos y mitigación
- Riesgo 1:Sesgos en los datos que generan decisiones injustas (por ejemplo, en banca o sanidad).
- Mitigación 1:Auditoría de datos, revisión ética, uso de métricas de equidad y validación por equipos multidisciplinares.
- Riesgo 2:Falta de transparencia y comprensión del modelo (caja negra).
- Mitigación 2:Uso de técnicas de explicabilidad (XAI), documentación clara, límites de uso y supervisión humana en decisiones críticas.

## 7) Conclusión
- Qué sectores destacan más:Sanidad, finanzas y comercio electrónico concentran gran parte de las aplicaciones prácticas de IA hoy en día.
- Qué lenguajes aparecen con más frecuencia:Python es el más dominante en IA, complementado por Java, R y JavaScript según el contexto.
- Qué importancia tiene esto para DAW/DAM: Los desarrolladores deben saber consumir APIs de IA, integrar modelos en aplicaciones web/escritorio y entender las limitaciones y riesgos para diseñar soluciones responsables y útiles.

## 8) Fuentes oficiales (mín. 2)
- Fuente 1 (sectores / aplicación IA):Comisión Europea — informes sobre adopción de IA en sectores económicos
OCDE (OECD) — estudios sobre impacto de la IA en sanidad, finanzas y servicios.
- Fuente 2 (lenguajes / ecosistema técnico):Documentación oficial de Python (python.org) y PyTorch/TensorFlow.
Documentación de Java (Oracle) y Node.js/JavaScript (ECMAScript, MDN) para integración de servicios de IA.