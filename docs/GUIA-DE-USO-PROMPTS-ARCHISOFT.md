# Guía de uso: Biblioteca de prompts ARCHISOFT — Proyectos, equipos y disciplinas

**Edición inicial:** 25 de noviembre de 2026
**Público:** Managers, coordinadores, responsables de disciplina y dirección de Archisolut.
**Integración:** Claude conectado al conector **ARCHISOFT**, de consulta y **solo lectura** sobre el CRM corporativo.

> Los prompts están en [`prompts/archisoft/`](../prompts/archisoft/README.md). Esta guía explica cómo usarlos y qué límites tienen.

## Cómo utilizarla

1. Abre Claude e inicia sesión en el conector ARCHISOFT con tu cuenta corporativa.
2. Elige un prompt del [catálogo](../prompts/archisoft/README.md), copia el bloque **«Prompt para copiar»** y especifica tu disciplina, equipo, proyecto y periodo si corresponde.
3. Revisa la evidencia reportada; el resultado **no constituye una aprobación técnica** ni sustituye a un responsable humano.

## Índice del catálogo

| ID | Prompt | Para quién | Modalidad |
| --- | --- | --- | --- |
| 01 | [Diagnóstico de mi disciplina](../prompts/archisoft/01-seguimiento-proyectos/01-diagnostico-de-mi-disciplina.md) | Disciplina / seguimiento | ARCHISOFT (si los datos están expuestos) |
| 02 | [Portafolio de proyectos activos](../prompts/archisoft/01-seguimiento-proyectos/02-portafolio-de-proyectos-activos.md) | Dirección / portafolio | ARCHISOFT (si los datos están expuestos) |
| 03 | [Tareas vencidas y próximos vencimientos](../prompts/archisoft/02-control-tareas/03-tareas-vencidas-y-proximos-vencimientos.md) | Productividad / alertas | ARCHISOFT (si los datos están expuestos) |
| 04 | [Proyectos sin seguimiento reciente](../prompts/archisoft/02-control-tareas/04-proyectos-sin-seguimiento-reciente.md) | Supervisión / actividad | ARCHISOFT (si los datos están expuestos) |
| 05 | [Revisión semanal para manager](../prompts/archisoft/03-coordinacion/05-revision-semanal-para-manager.md) | Managers / equipos | ARCHISOFT (si los datos están expuestos) |
| 06 | [Bloqueos y dependencias entre disciplinas](../prompts/archisoft/03-coordinacion/06-bloqueos-y-dependencias-entre-disciplinas.md) | Coordinación interdisciplinaria | ARCHISOFT (si los datos están expuestos) |
| 07 | [Preparar reunión de seguimiento](../prompts/archisoft/03-coordinacion/07-preparar-reunion-de-seguimiento.md) | Reuniones / coordinación | ARCHISOFT (si los datos están expuestos) |
| 08 | [Seguimiento de compromisos de reunión](../prompts/archisoft/03-coordinacion/08-seguimiento-de-compromisos-de-reunion.md) | Reuniones / compromisos | ARCHISOFT (si los datos están expuestos) |
| 09 | [Preparación de entrega por fase](../prompts/archisoft/04-entregas-clientes/09-preparacion-de-entrega-por-fase.md) | Entregas / fases | ARCHISOFT (si los datos están expuestos) |
| 10 | [Seguimiento de comentarios de ciudad](../prompts/archisoft/04-entregas-clientes/10-seguimiento-de-comentarios-de-ciudad.md) | Permisos / CT | ARCHISOFT (si los datos están expuestos) |
| 11 | [Correcciones solicitadas por cliente](../prompts/archisoft/04-entregas-clientes/11-correcciones-solicitadas-por-cliente.md) | Clientes / cambios | ARCHISOFT (si los datos están expuestos) |
| 12 | [Carga de trabajo por responsable](../prompts/archisoft/02-control-tareas/12-carga-de-trabajo-por-responsable.md) | Equipos / capacidad | ARCHISOFT (si los datos están expuestos) |
| 13 | [Resumen ejecutivo de un proyecto](../prompts/archisoft/01-seguimiento-proyectos/13-resumen-ejecutivo-de-un-proyecto.md) | Proyecto individual | ARCHISOFT (si los datos están expuestos) |
| 14 | [Auditoría de calidad de datos del proyecto](../prompts/archisoft/06-calidad-datos/14-auditoria-de-calidad-de-datos-del-proyecto.md) | Calidad de información | ARCHISOFT (si los datos están expuestos) |
| 15 | [Alertas y decisiones para dirección](../prompts/archisoft/05-direccion/15-alertas-y-decisiones-para-direccion.md) | Dirección / riesgos | ARCHISOFT (si los datos están expuestos) |
| 16 | [Revisión final PCL asistida con documentos](../prompts/archisoft/07-revision-tecnica/16-revision-final-pcl-asistida-con-documentos.md) | Revisión técnica / PCL | ARCHISOFT + documentos adjuntos |
| 17 | [Revisión final MEF asistida con documentos](../prompts/archisoft/07-revision-tecnica/17-revision-final-mef-asistida-con-documentos.md) | Revisión técnica / MEF | ARCHISOFT + documentos adjuntos |

## Prompts originales de jefatura

La biblioteca de origen incluye dos documentos extensos con el procedimiento de revisión final redactado por jefatura:

- **Revisión final de PCL** (plomería, civil, landscape, piscinas y OSTDS): criterios por fase y ronda, coordinación con arquitectura, F006, correcciones de cliente, documentación especializada y comentarios de ciudad.
- **Revisión final de MEF** (mecánica, eléctrica y fire): criterios técnicos, F006, cálculos, life safety plan, comentarios de ciudad y bomberos.

**Estos dos textos no se publican en este repositorio público.** Contienen criterios internos de aceptación, nombres de personas de la organización y referencias a registros internos de control. Se conservan en una ubicación interna de acceso restringido y se solicitan a jefatura por un canal autorizado. Consulta el [aviso de la categoría de revisión técnica](../prompts/archisoft/07-revision-tecnica/README.md).

Dos condiciones de uso:

- **No deben ejecutarse como auditoría documental solo mediante el conector:** requieren acceso a los planos y documentos listados en el procedimiento.
- **Nadie debe firmar un informe con el nombre del responsable de revisión final de jefatura** ni atribuirse una aprobación final sin su autorización expresa.

## Matriz de capacidades y límites

| Petición | Uso esperado | Límite |
| --- | --- | --- |
| Estados, tareas, responsables, vencimientos y equipos visibles | Consultas de CRM mediante ARCHISOFT | Sujetos a permisos, entidad expuesta y registros disponibles |
| Historial operativo de proyecto | Capacidad de historial que exponga el conector, cuando esté disponible | Empezar por consultas pequeñas; no solicitar históricos completos por defecto |
| Fases, alcance contractual, F006 y decisiones de cliente | Usar solo campos y documentos accesibles o adjuntos | No suponer que están presentes en el conector |
| Revisión de planos, PDFs, cálculo hidráulico o eléctrico, normativas y firmas | Claude con los documentos suministrados y revisión humana | No inferir cumplimiento técnico a partir de simples tareas del CRM |
| Modificar estados, enviar correos o reasignar tareas | Fuera del alcance del conector | ARCHISOFT es **solo lectura** |

## Estado de validación

Toda la biblioteca está **Documentada y Revisada**. **Ningún prompt ha sido probado todavía contra el conector real ni validado funcionalmente.** Las estructuras exactas de entidades y campos que cada prompt supone deben comprobarse con un usuario real antes de adoptarlo como estándar corporativo.

Esta guía no cambia el código, los permisos ni el alcance del conector.

## Fuentes de referencia

- Documentación MCP Archisolut Connectors (Notion, acceso interno).
- Documentación técnica Archisolut VPS (Notion, acceso interno).
- Procedimientos originales de revisión PCL y MEF de jefatura (distribución interna restringida; no publicados en este repositorio).
