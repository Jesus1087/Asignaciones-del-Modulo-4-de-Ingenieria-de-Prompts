# Laboratorio 1
## Construcción Iterativa de un Prompt Profesional

**Clase:** 1

**Duración:** 20 minutos

**Modalidad:** Guiado por el docente

---

# Objetivo

Diseñar un prompt profesional aplicando una metodología iterativa basada en componentes arquitectónicos (rol, contexto, objetivo, restricciones y formato).

Al finalizar este laboratorio el estudiante será capaz de:

- Identificar las limitaciones de un prompt improvisado.
- Mejorar progresivamente un prompt mediante iteraciones.
- Comparar resultados entre diferentes versiones.
- Comprender cómo las decisiones de diseño modifican el comportamiento del modelo.

---

# Caso de estudio

La empresa **TechSolutions S.A.** recibe aproximadamente **300 solicitudes diarias** en su mesa de ayuda.

Actualmente un operador humano clasifica manualmente cada solicitud para determinar:

- categoría;
- prioridad;
- departamento responsable.

La empresa desea automatizar este proceso utilizando un modelo de lenguaje.

---

# Material proporcionado

## Solicitud recibida

**Asunto**

No puedo acceder al sistema

**Mensaje**

Buenos días.

Desde esta mañana intento ingresar al sistema ERP, pero aparece el mensaje **Error 500**.

Necesito emitir facturas hoy mismo.

Muchas gracias.

---

# Paso 1 — Prompt inicial

Sin utilizar ningún patrón de diseño, escriba el primer prompt que utilizaría para resolver el problema.

**Tiempo sugerido:** 3 minutos.

Ejemplo:

```text
Clasifica este correo electrónico.
```

---

## Reflexión

Discuta con su grupo:

- ¿Qué información falta?
- ¿Puede otra persona reutilizar este prompt?
- ¿Obtendrán todos los usuarios exactamente la misma respuesta?

---

# Paso 2 — Agregar un Rol

Ahora incorpore un rol profesional.

Ejemplo:

```text
Actúa como un analista senior de soporte técnico.
```

Ejecute nuevamente el prompt.

---

## Reflexión

¿Qué cambió respecto a la primera versión?

---

# Paso 3 — Agregar Contexto

Incorpore información relevante sobre el proceso organizacional.

Ejemplo:

```text
La empresa recibe aproximadamente 300 solicitudes de soporte diariamente.
Todas deben clasificarse antes de asignarlas al departamento correspondiente.
```

Ejecute nuevamente el prompt.

---

# Paso 4 — Definir el Objetivo

Especifique claramente qué espera obtener.

Ejemplo:

```text
Clasifica la solicitud indicando:

- categoría
- prioridad
- departamento responsable
- justificación
```

---

# Paso 5 — Incorporar Restricciones

Agregue reglas que limiten el comportamiento del modelo.

Ejemplo:

```text
No inventes información.

Utiliza únicamente las categorías definidas.

Si la información es insuficiente, indícalo explícitamente.
```

---

# Paso 6 — Definir el Formato

Solicite un formato estructurado.

Ejemplo:

```json
{
    "categoria":"",
    "prioridad":"",
    "departamento":"",
    "justificacion":""
}
```

Ejecute nuevamente el prompt.

---

# Comparación de resultados

Complete la siguiente tabla.

| Versión | ¿Qué mejoró? |
|----------|--------------|
| Prompt inicial |1 |
| Con rol | 2|
| Con contexto | 3|
| Con objetivo |4 |
| Con restricciones |5 |
| Con formato |10 |

---

# Discusión

Responda junto con su grupo:

1. ¿Qué componente produjo la mayor mejora?
La mejora la produjo el contexto ya que la IA no sabia donde se iba a usar este prompt y con el contexto empezo a encaminarse en el objetiv0.

2. ¿Cuál fue el más difícil de definir?
Las restricciones, ya que casi nunca las utilizamos o poenemos limites a las ordenes dadas a la IA.

3. ¿Qué componente considera indispensable?
El contexto y el formato

No existe una única respuesta correcta.

El objetivo es analizar el impacto de cada decisión de diseño.

---

# Conclusiones

Complete las siguientes afirmaciones.

**Antes del laboratorio pensaba que...**
Que escribir prompts para las IA era solo simplemente dar una orden sencilla sin ningun tipo de contexto ni restricciones y que ella diera el formato a la informacion solicitada.
_____________________________________________________

**Después del laboratorio considero que...**

_Es importante y sumamente util es escribir correctamente y con este orden dado en clase los prompts para que als IAS puedan dar mejores resultados. De aqui en adelante escribire mis prompts asignando un rol, dando contexto, especificando el objeto, aplicando restricciones y por ultimo introduciendo el formato deseado____________________________________________________

---

# Entregable

Cada grupo entregará:

- El prompt inicial.Clasifica este correo electrónico.

- El prompt final.
Pensamiento completado
Aquí tienes la secuencia completa de tus instrucciones (prompts) desde que asignaste el rol hasta que definiste el formato de salida:
Asignación de rol:
"Actúa como un analista senior de soporte técnico."
Contexto del escenario:
"La empresa recibe aproximadamente 300 solicitudes de soporte diariamente.
Todas deben clasificarse antes de asignarlas al departamento correspondiente."
Campos requeridos:
"Clasifica la solicitud indicando:
categoría
prioridad
departamento responsable
justificación"
Restricciones estrictas:
"No inventes información.
Utiliza únicamente las categorías definidas.
Si la información es insuficiente, indícalo explícitamente.
"

5. **Formato de salida solicitado:**  
   "```json  
   {  
       "categoria":"",  
       "prioridad":"",  
       "departamento":"",  
       "justificacion":""  
   }  
   ```"

---

**Nota:** Hasta este punto, **no has incluido el texto del correo** que necesita ser clasificado. Si deseas que ejecute la tarea con estas reglas exactas, por favor proporciona el contenido del correo ahora.

- Una breve explicación de las decisiones de diseño adoptadas.
Aquí tienes las decisiones de diseño clave de forma breve:
Rol y Contexto: Asignar un perfil "Senior" y un volumen alto (300/día) obliga al modelo a priorizar la eficiencia, la estandarización y el pensamiento estructurado (SLAs, triaje) sobre respuestas genéricas.
Restricciones Negativas: La regla "no inventes información" y "indica si es insuficiente" actúa como un mecanismo de control de alucinaciones, garantizando la fiabilidad y honestidad del resultado.
Formato Estructurado (JSON): Exigir JSON asegura que la salida sea machine-readable, facilitando su integración automática con sistemas de gestión de tickets (APIs, scripts).
Prompt Chaining (Encadenamiento): Construir la instrucción por capas (rol → contexto → campos → restricciones → formato) reduce la ambigüedad y afina el comportamiento del modelo antes de procesar el dato real.
