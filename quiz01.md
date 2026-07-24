# Actividad de Clase: Analizando Agentes de IA con Hugging Face Spaces

## Objetivo

Explorar aplicaciones reales de Inteligencia Artificial en **Hugging
Face Spaces** y analizarlas desde la perspectiva de los **agentes
racionales**.

Al finalizar la actividad, los estudiantes deberán ser capaces de:

-   Identificar los componentes **PEAS** de un agente.
-   Clasificar las propiedades del entorno.
-   Proponer qué tipo de programa de agente podría implementarse detrás
    del sistema.
-   Justificar sus respuestas.

------------------------------------------------------------------------

## Instrucciones

1.  Ingresen a **https://huggingface.co/spaces**.
2.  Exploren diferentes Spaces.
3.  Seleccionen uno que les parezca interesante.
4.  Interactúen con el sistema durante algunos minutos.
5.  Completen la siguiente ficha de análisis.

------------------------------------------------------------------------

# Ficha de análisis

## 1. Nombre del Space

**Nombre:** Santiago Vásquez Arboleda

**Enlace:** https://huggingface.co/spaces/mrfakename/Z-Image-Turbo

------------------------------------------------------------------------

## 2. ¿Qué hace el agente?

Describa en dos o tres líneas cuál es la función del sistema:

El sistema recibe una entrada de texto de una imagen que se desee generar, ademas hay otras entradas que se catalogan como avanzadas que serían el alto y ancho de la imagen y tambien unos "pasos de inferencia"

------------------------------------------------------------------------

## 3. Análisis PEAS

  Elemento          Respuesta
  ----------------- ----------------------------------------------------
  **Performance**   ¿Qué significa que el agente haga bien su trabajo? El agente hace bien su trabajo si efectivamente genera una imagen acorde a lo que se le solicitó y no divaga creando imagenes que no tienen que ver con lo estrictamente especificado.
  **Environment**   ¿Con qué interactúa el agente? La interfaz gráfica y los modelos usados para la generación.
  **Actuators**     ¿Qué acciones produce? Genera una imagen que emula la situación del texto ingresado.
  **Sensors**       ¿Qué información recibe como entrada? La entrada de texto, ancho y alto de la imagen y pasos de inferencia.

------------------------------------------------------------------------

## 4. Clasificación del entorno

Complete la siguiente tabla y justifique brevemente cada respuesta.

  Propiedad      Clasificación     Justificación
  -------------- ----------------- -----------------------------------------------------------------------------------------------------------------
  Observable     Parcial           La estructuración de los modelos usados no es conocida por lo menos en esta interfaz.
  Determinista   No                Bajo un mismo prompt se cosigue una imagen distinta.
  Episódico      Sí                Por lo menos desconociendo como opera en principio solo hace una tarea a la vez que es generar la imagen.
  Estático       No                Cuando cambia la imagen ejecutando de nuevo el prompt puede que genere una mejor imagen que el anterior o no.
  Discreto       Sí                El texto no es continuo.
  Conocido       Sí                Tal cual porque el agente rige bajo los modelos del entorno y estre no tiene comportamientos por fuera de estos 

------------------------------------------------------------------------

## 5. ¿Qué tipo de programa de agente creen que es?

Seleccione la opción que consideren más adecuada y explique por qué.

-   Agente de reflejo simple
-   Agente basado en modelo
-   Agente basado en objetivos
-   **Agente basado en utilidad**
-   Agente con aprendizaje

> **Importante:** No existe una única respuesta correcta. Lo importante
> es justificar la elección a partir del comportamiento observado.

Justificación: El agente busca generar la imagen y ese es su único objetivo, sin embargo tener una métrica dicotómica cierra demasiado las posibilidades, pues se puede establecer un orden de que tanto se cumplió el objetivo mas que solo decir si se cumplió o no.

------------------------------------------------------------------------

# Discusión en clase

Después de las presentaciones, discutiremos preguntas como:

-   ¿Dos Spaces diferentes pueden compartir el mismo tipo de entorno?
-   ¿Es posible saber con certeza qué tipo de agente implementa un Space
    únicamente observándolo?
-   ¿Qué diferencia existe entre el comportamiento observable de un
    agente y su implementación interna?

------------------------------------------------------------------------

# Reto adicional

Encuentre un Space que pueda clasificarse como:

1.  **Totalmente observable, determinista y episódico.** https://huggingface.co/spaces/webml-community/bonsai-webgpu-kernels Es un bonsai que se comportará siempre de la misma forma siempre que la interacción sea igual.
2.  **Parcialmente observable, estocástico y secuencial.** https://huggingface.co/spaces/r3gm/wan2-2-fp8da-aoti-preview-2c Generador de videos a partir de una imagen. Parcialmente observable porque no se conocen la estructuración de los modelos usados. Estocástico porque con la misma imagen no siempre generará el mismo video y secuencial porque simultaneamente hace varias tareas como crear audio a la vez que crea varios fotogramas simultáneamente.

Justifique su respuesta.

------------------------------------------------------------------------

# Rúbrica (10 puntos)

| Criterio | Puntos |
|-----------|:------:|
| Descripción correcta del Space | 2 |
| Identificación de PEAS | 3 |
| Clasificación del entorno | 3 |
| Justificación del tipo de agente | 2 |
| **Total** | **10** |

------------------------------------------------------------------------


