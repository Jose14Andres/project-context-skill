---
name: project-context
description: Inspecciona un repositorio para documentar su contexto, entorno y estado, funcionalidades y alcance, convenciones de estructura y configuración, y restricciones del proyecto. Úsala al comenzar trabajo en un proyecto, antes de planificar cambios o cuando el usuario pida entender cómo está organizado o qué permite hacer.
---

# Contexto del proyecto

Construye una descripción útil y verificable del proyecto antes de planificar o modificarlo. Usa el repositorio y el entorno disponibles como fuente principal. Distingue los hechos observados de las inferencias y de la información que todavía falta.

## Inspección

1. Identifica la raíz del repositorio y revisa las instrucciones existentes, como `CLAUDE.md`, `AGENTS.md` y documentación principal.
2. Reconoce los lenguajes, frameworks y herramientas a partir de archivos reales: manifiestos de dependencias, archivos de bloqueo, configuración del compilador, build, lint, pruebas, contenedores y CI. Sigue la estructura de directorios para entender paquetes, aplicaciones y límites entre componentes.
3. Resume el entorno y su estado actual con evidencia disponible: sistema y herramientas relevantes, dependencias instaladas si se pueden comprobar, rama y cambios locales de Git, y estado de build o ejecución solo si existe evidencia directa. No ejecutes servicios, instalaciones, migraciones ni comandos que alteren datos para averiguarlo.
4. Determina qué hace el producto y cuál es su alcance a partir de README, código, rutas, componentes, contratos, pruebas y configuración. Separa funcionalidades existentes de las planeadas o incompletas.
5. Extrae las convenciones que impone cada lenguaje o herramienta. Explica qué papel cumplen los directorios y archivos de configuración clave en este proyecto; evita enumerarlos sin explicar su relación con el trabajo.
6. Registra restricciones explícitas y riesgos para el trabajo. Considera la triple restricción clásica —alcance, tiempo y costo— y los factores del entorno: plataforma y versiones, dependencias, infraestructura, permisos, conectividad, datos, compatibilidad, seguridad y requisitos operativos. No inventes presupuestos, fechas límite, límites de alcance ni requisitos. Marca como “por confirmar” lo que no esté documentado.

## Criterios

- Basa cada afirmación concreta en un archivo, configuración, comando de solo lectura o estado visible. Incluye rutas para que el usuario pueda comprobar hallazgos.
- Si hay varios paquetes o aplicaciones, descríbelos por separado y explica sus dependencias o límites principales.
- No trates nombres de carpetas, dependencias declaradas o comentarios como prueba suficiente de que una función está terminada o activa.
- No cambies archivos ni configures herramientas durante la inspección. Si el usuario también pide una implementación, presenta primero el contexto relevante y después continúa con ese trabajo.
- Ajusta la profundidad al tamaño del proyecto y a la petición. Prioriza lo que afectaría decisiones, alcance, estimaciones o compatibilidad.

## Formato de respuesta

Entrega un resumen con estas secciones, omitiendo las que no apliquen:

1. **Proyecto y propósito** — qué es y para quién, si se puede determinar.
2. **Entorno y estado** — tecnologías, versiones relevantes y estado observable; señala límites de la inspección.
3. **Funcionalidad y alcance** — qué existe, qué está incompleto y qué queda fuera o no se puede determinar.
4. **Estructura y convenciones** — mapa breve de directorios y archivos de configuración importantes, y cómo condicionan cambios.
5. **Restricciones** — alcance, tiempo, costo y factores de entorno, separados entre explícitos y por confirmar.
6. **Implicaciones para el trabajo solicitado** — decisiones, dependencias o preguntas que afecten el siguiente paso.

Sé conciso, cita rutas concretas y no rellenes huecos con suposiciones. Si el usuario pidió una tarea inmediata, evita convertir el resumen en un informe largo: incluye solo el contexto que cambia cómo conviene ejecutarla.
