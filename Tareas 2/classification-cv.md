# Summarize Candidate CV

> **Versión:** 1.0  
> **Estado:** Activo  
> **Proceso:** Reclutamiento y Selección de Personal  
> **Responsable:** Equipo de Recursos Humanos  
> **Patrones utilizados:** Persona Pattern, Template Pattern, Output Schema Pattern

---

# Objetivo

Generar un resumen de clasificacion de una hoja de vida para facilitar la evaluación inicial de candidatos durante un proceso de selección.

La clasificacion debe ser con base en las categorias y subcategorias que la organizacion maneja.

---

# Contexto de Uso

Este prompt forma parte del proceso de reclutamiento.

Se ejecuta **después de realizar el paso de summarize** y **antes de evaluacion**.

```text
Recepción CV

↓

Resumen Ejecutivo

↓

Clasificación

↓

Evaluación

↓

Entrevista
```

---

# Entradas


| Variable | Descripción | Ejemplo |
|----------|-------------|----------|
| rol | Rol asumido por el modelo | Analista de Recursos Humanos |
| tipo_documento | Documento que será analizado | Curriculum Vitae |
| objetivo | Propósito de la clasificación | Identificar el nivel del candidato |
| categorias | Categorías posibles | Junior, Semi Senior, Senior |
| criterios | Aspectos que deben evaluarse | Experiencia, tecnologías, liderazgo |
| idioma | Idioma de salida | Español |

---

# Variables Recomendadas

| Variable | Valor sugerido |
|------------|---------------|
| rol | Analista Senior de Recursos Humanos |
| audiencia | Gerente de Tecnología |
| categorias | Junior, Semi-Senior, Senior  |
| criterios | Años de experiencia, liderazgo técnico, tecnologías utilizadas| 
| idioma | Español |
| longitud | 150 palabras |

---

# Prompt

```text
Actúa como {{rol}}.

Analiza el siguiente {{tipo_documento}}.

El objetivo del análisis es:

{{objetivo}}

Clasifica el documento utilizando únicamente las siguientes categorías:

{{categorias}}

La clasificación debe basarse exclusivamente en:

{{criterios}}

No inventes información.

Si la información disponible no es suficiente para determinar una categoría, indícalo explícitamente.

Presenta el resultado siguiendo el formato especificado.

Utiliza el documento adjunto.

```

---

# Restricciones

El modelo debe:

- utilizar únicamente información presente en el documento;
- mantener un tono profesional;
- conservar nombres propios;
- evitar opiniones personales;
- no realizar recomendaciones de contratación.

---

# Formato Esperado


```markdown
### Clasificación
...

### Categoría:
...

### Subcategoría:
...

### Nivel de confianza:
...

### Justificación:
...

### Evidencias encontradas:

### Observaciones:
...
```

---

# Ejemplo de Entrada

```text
Ingeniero de Sistemas con ocho años de experiencia en desarrollo Backend utilizando .NET, SQL Server y Azure.

Participó en proyectos financieros y de telecomunicaciones.

Cuenta con certificaciones Microsoft Azure Fundamentals y Scrum Master.
```

---

# Ejemplo de Salida

```markdown
### Clasificación

### Categoría:
Senior

### Subcategoría:
Backend .NET

### Nivel de confianza:
95%

### Justificación:
El candidato posee más de ocho años de experiencia, liderazgo técnico y experiencia en arquitecturas empresariales.

### Evidencias encontradas:

- Más de ocho años de experiencia.
- Desarrollo con ASP.NET Core.
- Arquitecturas de microservicios.
- Azure DevOps.
- Docker.
- Kubernetes.

### Observaciones:
Perfil adecuado para posiciones Senior Backend.
```

---

# Patrones Aplicados

| Patrón | Propósito |
|----------|-----------|
| Persona Pattern | Definir el rol del analista |
| Template Pattern | Reutilizar el prompt |
| Output Schema Pattern | Estructurar el resultado |

---

# Calidad Esperada

El resultado debe cumplir los siguientes criterios.

- La información corresponde exactamente al documento.
- No existen datos inventados.
- El resumen mantiene un lenguaje profesional.
- Se respetan las restricciones de longitud.
- El formato es consistente.

---

# Integración

Este prompt puede integrarse con:

- Microsoft Power Automate
- n8n
- Zapier
- LangChain
- Prompt Flow
- APIs de OpenAI

---

# Dependencias

Este prompt utiliza la plantilla:

```text
templates/summary-template.md
```

Puede formar parte del proceso:

```text
processes/recruitment.md
```

---

# Historial de Cambios

| Versión | Fecha | Descripción |
|----------|--------|-------------|
| 1.0 | 2026-07-21 | Versión inicial |