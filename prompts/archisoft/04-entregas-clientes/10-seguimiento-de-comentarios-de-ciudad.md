# 10. Seguimiento de comentarios de ciudad

**Categoría:** Entregas y clientes  
**Público recomendado:** Responsables de permisos, coordinadores y managers.  
**Requisitos:** acceso autorizado al conector ARCHISOFT con la cuenta corporativa propia. La consulta devuelve únicamente lo que los permisos del usuario autenticado permiten ver.  
**Estado de validación:** Documentado · Revisado documentalmente. **No probado con MCP ni validado funcionalmente.**

## Propósito

Revisar el seguimiento operativo de los comentarios de ciudad o de bomberos registrados.

## Qué información se espera obtener

Tabla con jurisdicción, comentario, responsable, estado y próxima acción.

## Prompt para copiar

Copia el bloque completo: incluye las reglas de uso que delimitan la consulta.

```text
Actúa como analista de proyectos de Architectural Solutions LLC / Archisolut. Consulta proyectos con comentarios de ciudad o de bomberos registrados y revisa su seguimiento operativo.

**Revisa lo siguiente:**
- Comenta los registros de CT# solo cuando existan.
- Separa comentarios pendientes, respondidos, en espera de tercero y sin evidencia.
- Identifica responsable y fechas registradas.
- Enumera documentos que se mencionan como pendientes, si la evidencia lo permite.

**Entrega:** Proyecto | jurisdicción si consta | comentario/registro | responsable | estado | próxima acción. La conformidad técnica exige adjuntar comentarios y planos.

- Emplea **ARCHISOFT (MCP de Archisolut)** como fuente de datos operativos de EspoCRM, con los permisos del usuario autenticado y en **solo lectura**. No intentes saltar permisos, modificar registros ni usar otras credenciales.
- Antes de consultar muchos registros, delimita **disciplina, equipo, proyecto y periodo**. Identifica la disciplina mediante los datos disponibles; si no es inequívoca, pregunta cuál revisar. No infieras que todos los proyectos visibles pertenecen al equipo del usuario.
- Consulta las capacidades de historial y seguimiento disponibles en ARCHISOFT, respetando las herramientas expuestas, los permisos del usuario y los límites de consulta aplicables. Si no existe una capacidad o faltan campos, señálalo. Si necesitas recuperar múltiples registros, utiliza la paginación permitida y no presentes resultados parciales como completos. Empieza por consultas pequeñas y específicas, y escala únicamente si hace falta.
- Distingue hechos con **identificador, proyecto y fecha** de hipótesis, y distingue **sin registros visibles** de **sin actividad real**. No inventes cifras, estados ni responsables.
- ARCHISOFT no equivale automáticamente a acceso a PDFs, planos, F006, correos o archivos externos. Para análisis técnico de entregables, pide adjuntar los documentos necesarios. Nunca dictamines conformidad de un plano que no has visto.
- No uses el nombre de otra persona como firma de un informe o correo sin autorización. Los resultados son borradores sujetos a revisión humana.
```

## Limitaciones y verificaciones necesarias

- El resultado es un **borrador** sujeto a revisión humana; no constituye aprobación técnica ni cierre de una tarea.
- ARCHISOFT es **solo lectura**: no modifica estados, no reasigna tareas y no envía correos.
- Lo que no aparece en el CRM no existe para esta consulta. Distingue siempre **«sin registros visibles»** de **«sin actividad real»**.
- El acceso a un proyecto no implica responsabilidad sobre él ni autoriza a deducir la estructura completa del equipo.
- Para cualquier dictamen sobre planos, cálculos, PDFs o F006 hacen falta los documentos: el conector de CRM no los sustituye.

---

**Origen:** biblioteca ARCHISOFT preparada por el equipo de Archisolut (`archisolut-prompt-library`, edición 25 de noviembre de 2026), prompt `10-seguimiento-de-comentarios-de-ciudad.md`.

**Nota de publicación:** las referencias a nombres internos de herramientas y a límites técnicos del conector se expresaron de forma funcional para su publicación. La finalidad operativa del prompt no se alteró.
