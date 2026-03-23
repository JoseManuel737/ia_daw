# Práctica IA (RA4 · f)

## 1) Caso de uso
- Tipo de aplicación:Sistema de recomendación basado en IA.
- Problema:Los usuarios navegan por muchos productos sin encontrar fácilmente lo que realmente les interesa, reduciendo ventas y aumentando el abandono.
- Usuario:Clientes de una tienda online que buscan productos relevantes y personalizados.

## 2) Datos
- Datos:Historial de navegación

Compras anteriores

Productos vistos

Valoraciones y clics

Catálogo de productos (categorías, descripciones, precios)
- Tipo minería:Minería de datos de comportamiento

Minería de texto (descripciones)

Sistemas de recomendación (filtrado colaborativo + contenido)

## 3) Pipeline
- Recogida:Logs del e‑commerce, base de datos de productos, eventos de usuario.
- Limpieza:Eliminación de duplicados, normalización de IDs, tratamiento de valores nulos.
- Transformación:Vectorización de productos (TF‑IDF o embeddings, Matriz usuario‑producto, Escalado y codificación
- Entrenamiento:Modelo híbrido: filtrado colaborativo + similitud de contenido, Validación cruzada
- Predicción:Lista ordenada de productos recomendados para cada usuario
- Uso:Mostrar recomendaciones personalizadas en la web/app en tiempo real

## 4) Integración
- Backend:API REST que recibe el ID del usuario y devuelve recomendaciones, Motor de inferencia en Pytho(FastAPI, Flask)
- Frontend:Módulo de recomendaciones en la página principal y fichas de producto, Actualización dinámica según comportamiento
- Flujo:Usuario navega

Backend registra eventos

API consulta el modelo

Frontend muestra recomendaciones personalizadas

## 5) Valor
- Mejora:Aumento de conversión

Mayor satisfacción del usuario

Reducción del tiempo para encontrar productos
- Sin IA:Recomendaciones genéricas

Menor personalización

Menos ventas cruzadas
- Rentabilidad:Incremento del ticket medio

Más ventas por usuario

Optimización del catálogo

## 6) Diagrama
Usuario → Navegación → Recogida de datos → Limpieza → Transformación
        → Entrenamiento del modelo → API de predicción → Frontend
        → Recomendaciones personalizadas → Usuario

## 7) Riesgos
- Riesgo 1:Sesgos en los datos (recomendar siempre lo mismo).
- Mitigación 1:Diversificación de recomendaciones y revisión periódica del modelo.
- Riesgo 2: Problemas de privacidad por uso de datos personales.
- Mitigación 2: Anonimización, cumplimiento RGPD, consentimiento explícito.

## 8) Fuente
    Documentación general sobre sistemas de recomendación (libros, papers, cursos de ML).

    Experiencia práctica en e‑commerce y machine learning.



