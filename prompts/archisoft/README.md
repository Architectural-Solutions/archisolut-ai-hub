# Biblioteca de prompts ARCHISOFT

**Prompts preparados para consultar los proyectos, las tareas y los equipos de Archisolut desde Claude, siempre dentro de los permisos de cada persona.**

Edición inicial: 25 de noviembre de 2026 · 17 prompts · Español.

**[Guía de uso](../../docs/GUIA-DE-USO-PROMPTS-ARCHISOFT.md)** — cómo conectarse, matriz de capacidades y límites del conector.

## ¿Qué es ARCHISOFT?

ARCHISOFT es el conector que permite a Claude **consultar** la información operativa de Archisolut que vive en el CRM: proyectos, fases, tareas, responsables, vencimientos y actividad registrada.

Tres ideas que conviene tener claras antes de empezar:

- **Es de solo lectura.** Puede leer y resumir; no cambia estados, no reasigna tareas y no envía correos.
- **Usa tus permisos, no los de otra persona.** Cada consulta ve exactamente lo que tú ves al entrar al CRM. Si algo no aparece, es que tu rol no tiene acceso: no es un error que haya que rodear.
- **No es un visor de documentos.** Consultar el CRM no equivale a abrir planos, PDFs, cálculos o el F006. Para cualquier análisis de entregables hay que adjuntar los documentos.

## Requisitos

1. Cuenta corporativa de Archisolut con acceso autorizado al conector ARCHISOFT.
2. Claude con el conector habilitado e iniciada la sesión.
3. Saber qué disciplina, equipo, proyecto y periodo quieres revisar: acotar antes de preguntar da respuestas mucho mejores.

## Empieza por aquí

Estos tres prompts cubren la mayor parte del uso diario y son el punto de partida recomendado:

| | Prompt | Para qué sirve |
| --- | --- | --- |
| ⭐ | **[Diagnóstico de mi disciplina](01-seguimiento-proyectos/01-diagnostico-de-mi-disciplina.md)** | Revisar los proyectos activos de tu disciplina y fijar las tres prioridades de la semana. |
| ⭐ | **[Tareas vencidas y próximos vencimientos](02-control-tareas/03-tareas-vencidas-y-proximos-vencimientos.md)** | Ver qué está vencido y qué vence en los próximos 7 días, ordenado por severidad. |
| ⭐ | **[Revisión semanal para manager](03-coordinacion/05-revision-semanal-para-manager.md)** | Preparar la reunión semanal: novedades, pendientes por responsable y decisiones a tomar. |

## Catálogo completo

### 1. Seguimiento de proyectos

| ID | Prompt | Descripción | Perfil recomendado | Validación |
| --- | --- | --- | --- | --- |
| 01 | [Diagnóstico de mi disciplina](01-seguimiento-proyectos/01-diagnostico-de-mi-disciplina.md) | Proyectos activos de una disciplina, su estado y las prioridades de la semana. | Disciplina · Coordinación | Documentado · Revisado |
| 02 | [Portafolio de proyectos activos](01-seguimiento-proyectos/02-portafolio-de-proyectos-activos.md) | Situación del conjunto de proyectos visibles, agrupada por equipo o disciplina. | Dirección · Portafolio | Documentado · Revisado |
| 13 | [Resumen ejecutivo de un proyecto](01-seguimiento-proyectos/13-resumen-ejecutivo-de-un-proyecto.md) | Ficha de una página sobre un proyecto concreto, con los IDs de las evidencias. | Cualquier perfil | Documentado · Revisado |

### 2. Control de tareas

| ID | Prompt | Descripción | Perfil recomendado | Validación |
| --- | --- | --- | --- | --- |
| 03 | [Tareas vencidas y próximos vencimientos](02-control-tareas/03-tareas-vencidas-y-proximos-vencimientos.md) | Lo vencido y lo que vence en 7 días, con días de atraso y próxima acción. | Cualquier perfil · Managers | Documentado · Revisado |
| 04 | [Proyectos sin seguimiento reciente](02-control-tareas/04-proyectos-sin-seguimiento-reciente.md) | Proyectos activos sin actividad registrada en los últimos 15 días. | Supervisión | Documentado · Revisado |
| 12 | [Carga de trabajo por responsable](02-control-tareas/12-carga-de-trabajo-por-responsable.md) | Reparto de tareas abiertas y vencidas entre el equipo, solo con asignaciones visibles. | Managers · Coordinación | Documentado · Revisado |

### 3. Coordinación

| ID | Prompt | Descripción | Perfil recomendado | Validación |
| --- | --- | --- | --- | --- |
| 05 | [Revisión semanal para manager](03-coordinacion/05-revision-semanal-para-manager.md) | Brief semanal con novedades verificables, pendientes y decisiones. | Managers | Documentado · Revisado |
| 06 | [Bloqueos y dependencias entre disciplinas](03-coordinacion/06-bloqueos-y-dependencias-entre-disciplinas.md) | Dependencias documentadas entre disciplinas en proyectos compartidos. | Coordinación interdisciplinaria | Documentado · Revisado |
| 07 | [Preparar reunión de seguimiento](03-coordinacion/07-preparar-reunion-de-seguimiento.md) | Agenda de 30 minutos, preguntas por responsable y plantilla de minuta. | Managers · Coordinación | Documentado · Revisado |
| 08 | [Seguimiento de compromisos de reunión](03-coordinacion/08-seguimiento-de-compromisos-de-reunion.md) | Contraste entre los acuerdos de una minuta y lo registrado en el CRM. | Coordinación | Documentado · Revisado |

### 4. Entregas y clientes

| ID | Prompt | Descripción | Perfil recomendado | Validación |
| --- | --- | --- | --- | --- |
| 09 | [Preparación de entrega por fase](04-entregas-clientes/09-preparacion-de-entrega-por-fase.md) | Avance operativo de proyectos próximos a Fase 2, Fase 3 o CT#. | Disciplina · Entregas | Documentado · Revisado |
| 10 | [Seguimiento de comentarios de ciudad](04-entregas-clientes/10-seguimiento-de-comentarios-de-ciudad.md) | Estado de los comentarios de ciudad o bomberos registrados. | Permisos · Coordinación | Documentado · Revisado |
| 11 | [Correcciones solicitadas por cliente](04-entregas-clientes/11-correcciones-solicitadas-por-cliente.md) | Correcciones de cliente documentadas y su relación con las tareas pendientes. | Clientes · Coordinación | Documentado · Revisado |

### 5. Dirección

| ID | Prompt | Descripción | Perfil recomendado | Validación |
| --- | --- | --- | --- | --- |
| 15 | [Alertas y decisiones para dirección](05-direccion/15-alertas-y-decisiones-para-direccion.md) | Informe priorizado de riesgos y decisiones, con anexo de evidencias. | Dirección | Documentado · Revisado |

### 6. Calidad de datos

| ID | Prompt | Descripción | Perfil recomendado | Validación |
| --- | --- | --- | --- | --- |
| 14 | [Auditoría de calidad de datos del proyecto](06-calidad-datos/14-auditoria-de-calidad-de-datos-del-proyecto.md) | Inconsistencias en los datos operativos del CRM y correcciones sugeridas. | Calidad · Coordinación | Documentado · Revisado |

### 7. Revisión técnica

| ID | Prompt | Descripción | Perfil recomendado | Validación |
| --- | --- | --- | --- | --- |
| 16 | [Revisión final PCL asistida con documentos](07-revision-tecnica/16-revision-final-pcl-asistida-con-documentos.md) | Acompaña la revisión final de PCL. **Requiere adjuntar el procedimiento interno y los documentos del proyecto.** | Revisión técnica PCL | Documentado · Revisado |
| 17 | [Revisión final MEF asistida con documentos](07-revision-tecnica/17-revision-final-mef-asistida-con-documentos.md) | Acompaña la revisión final de MEF. **Requiere adjuntar el procedimiento interno y los documentos del proyecto.** | Revisión técnica MEF | Documentado · Revisado |

Los procedimientos originales de revisión final redactados por jefatura **no se publican en este repositorio público**. Consulta [el aviso de la categoría](07-revision-tecnica/README.md) para saber por qué y cómo solicitarlos.

### Qué significa cada estado de validación

| Estado | Significado |
| --- | --- |
| **Documentado** | El prompt está escrito, con su propósito, público y límites. |
| **Revisado** | Una persona revisó su contenido y comprobó que no expone información sensible. |
| **Probado con MCP** | Se ejecutó contra el conector real y devolvió resultados coherentes. |
| **Validado funcionalmente** | Un responsable confirmó que el resultado sirve para la decisión que pretende apoyar. |

**Estado actual de toda la biblioteca: Documentado y Revisado.** Ningún prompt está todavía *Probado con MCP* ni *Validado funcionalmente*: las entidades, los campos y las capacidades que cada prompt supone deben comprobarse con un usuario real antes de adoptar la biblioteca como estándar corporativo.

## Cómo se usa

1. Abre Claude con el conector ARCHISOFT habilitado e inicia sesión con tu cuenta corporativa.
2. Entra al prompt que necesites y copia el bloque de **«Prompt para copiar»** completo.
3. Pégalo y añade tu contexto: disciplina, equipo, proyecto y periodo.
4. Revisa la evidencia que devuelve antes de reenviar nada.

### Ejemplos

**Acotar por disciplina y periodo**

> *(pegas el prompt 01)* Mi disciplina es plomería. Revisa únicamente los proyectos activos de las últimas dos semanas.

**Un proyecto concreto**

> *(pegas el prompt 13)* El proyecto es el de la dirección que te indico a continuación. Confirma primero que has identificado el proyecto correcto antes de resumir nada.

**Preparar la reunión del lunes**

> *(pegas el prompt 07)* Son los tres proyectos de mi equipo que entran en Fase 3 este mes. La reunión dura 30 minutos y asisten el coordinador y los dos dibujantes.

Cuanto más acotes, menos consultas hace el asistente y más fiable es el resultado.

## Advertencias

**Sobre permisos.** Cada consulta opera con tu identidad. Si una respuesta dice que no hay acceso, la vía correcta es solicitar el permiso por el canal corporativo, nunca buscar un rodeo. Estos prompts no deben modificarse para intentar leer información fuera de tu alcance.

**Sobre la calidad de los datos.** El resultado vale lo que vale el CRM. Una tarea sin responsable o sin fecha produce un hueco en el informe, no un dato. **«Sin registros visibles» no significa «sin trabajo realizado»**: antes de concluir que un proyecto está parado, pregunta al responsable.

**Sobre los límites de la información.** Conteos de tareas no son horas trabajadas ni rendimiento personal. Un proyecto visible no es un proyecto propio. Y ninguna salida de esta biblioteca aprueba un plano, cierra un comentario de ciudad ni sustituye la firma de un responsable técnico.

**Sobre lo que se escribe después.** Los resultados son borradores. No se firman con el nombre de otra persona ni se envían como si fueran una revisión aprobada.

## Origen y mantenimiento

Biblioteca preparada por el equipo de Archisolut sobre el conector ARCHISOFT (consulta de solo lectura del CRM). Las propuestas de mejora se canalizan por el procedimiento de contribución del repositorio; **no se añaden a este directorio datos reales de clientes, proyectos o personas**.
