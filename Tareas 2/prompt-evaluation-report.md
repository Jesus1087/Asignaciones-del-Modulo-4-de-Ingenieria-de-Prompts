# Prompt Evaluation Report

---

# Información General

| Campo | Valor |
|--------|-------|
| Estudiante | |
| Fecha | |
| Versión del Prompt | |
| Tipo de Prompt | ☐ Resumen ☐ Clasificación ☐ Extracción |
| Dominio | |
| Modelo utilizado | ☐ ChatGPT ☐ Claude ☐ Gemini ☐ Otro |
| Objetivo del Prompt | |

---

# Descripción del Prompt

Copie la versión del prompt que será evaluada.

> Puede pegar el prompt completo o indicar el archivo correspondiente dentro de la carpeta `prompts/`.

---

```text
(Pegar aquí el prompt utilizado)
```

---

# Objetivo de la Evaluación

Describa brevemente qué desea comprobar durante la ejecución de las pruebas.

Ejemplo:

- Verificar que el prompt detecta información faltante.
- Evaluar la consistencia de las respuestas.
- Comprobar que no inventa información.
- Analizar si identifica contradicciones.

---

**Respuesta**

```
____________________________________________________

____________________________________________________

____________________________________________________
```

---

# Casos de Prueba

## Caso 1

### Documento utilizado

```
sample-data/hr/cv-backend-good.md
```

### Objetivo

Verificar el comportamiento esperado utilizando un documento completo.

---

### Resultado obtenido

```
(Escriba un resumen de la respuesta obtenida)
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 1 2 3 4 5 |
| Completitud | 1 2 3 4 5 |
| Consistencia | 1 2 3 4 5 |
| Claridad | 1 2 3 4 5 |
| Relevancia | 1 2 3 4 5 |

---

### Problemas encontrados

```
____________________________________________________

____________________________________________________
```

---

### Observaciones

```
____________________________________________________

____________________________________________________
```

---

## Caso 2

### Documento utilizado

```
sample-data/hr/cv-backend-incomplete.md
```

### Objetivo

Verificar el manejo de información incompleta.

---

### Resultado obtenido

```
____________________________________________________
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 1 2 3 4 5 |
| Completitud | 1 2 3 4 5 |
| Consistencia | 1 2 3 4 5 |
| Claridad | 1 2 3 4 5 |
| Relevancia | 1 2 3 4 5 |

---

### Problemas encontrados

```
____________________________________________________
```

---

### Observaciones

```
____________________________________________________
```

---

## Caso 3

### Documento utilizado

```
sample-data/hr/cv-backend-contradictory.md
```

### Objetivo

Verificar la detección de inconsistencias.

---

### Resultado obtenido

```
____________________________________________________
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 1 2 3 4 5 |
| Completitud | 1 2 3 4 5 |
| Consistencia | 1 2 3 4 5 |
| Claridad | 1 2 3 4 5 |
| Relevancia | 1 2 3 4 5 |

---

### Problemas encontrados

```
____________________________________________________
```

---

### Observaciones

```
____________________________________________________
```

---

## Caso 4

### Documento utilizado

```
sample-data/hr/cv-backend-irrelevant-information.md
```

### Objetivo

Evaluar la capacidad del prompt para filtrar información irrelevante.

---

### Resultado obtenido

```
____________________________________________________
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 1 2 3 4 5 |
| Completitud | 1 2 3 4 5 |
| Consistencia | 1 2 3 4 5 |
| Claridad | 1 2 3 4 5 |
| Relevancia | 1 2 3 4 5 |

---

### Problemas encontrados

```
____________________________________________________
```

---

### Observaciones

```
____________________________________________________
```

---

## Caso 5

### Documento utilizado

```
sample-data/hr/cv-backend-unstructured.md
```

### Objetivo

Evaluar el comportamiento frente a documentos sin estructura.

---

### Resultado obtenido

```
____________________________________________________
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 1 2 3 4 5 |
| Completitud | 1 2 3 4 5 |
| Consistencia | 1 2 3 4 5 |
| Claridad | 1 2 3 4 5 |
| Relevancia | 1 2 3 4 5 |

---

### Problemas encontrados

```
____________________________________________________
```

---

### Observaciones

```
____________________________________________________
```

---

# Resumen de Resultados

| Caso | Exactitud | Completitud | Consistencia | Claridad | Relevancia |
|------|:---------:|:-----------:|:------------:|:--------:|:----------:|
| Caso 1 | | | | | |
| Caso 2 | | | | | |
| Caso 3 | | | | | |
| Caso 4 | | | | | |
| Caso 5 | | | | | |

---

# Hallazgos Principales

Después de ejecutar todos los casos de prueba, responda las siguientes preguntas.

## ¿Cuál fue el principal problema identificado?

```
____________________________________________________

____________________________________________________
```

---

## ¿Qué caso produjo la peor respuesta?

```
____________________________________________________
```

---

## ¿Qué mejoras considera necesarias?

```
____________________________________________________

____________________________________________________
```

---

# Plan de Mejora

Indique las modificaciones que realizará sobre el prompt antes de generar una nueva versión.

| Mejora propuesta | Justificación |
|------------------|---------------|
| | |
| | |
| | |

---

# Conclusión

Complete la siguiente reflexión.

> Después de ejecutar los cinco casos de prueba, considero que el prompt desarrollado:

☐ Está listo para utilizarse.

☐ Requiere mejoras menores.

☐ Requiere una revisión importante antes de utilizarse.

Justifique su respuesta.

```
____________________________________________________

____________________________________________________

____________________________________________________
```