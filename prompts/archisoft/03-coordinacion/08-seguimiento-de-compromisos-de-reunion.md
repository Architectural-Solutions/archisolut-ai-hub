# 08. Seguimiento de compromisos de reunión

**Categoría:** Coordinación  
**Público recomendado:** Coordinadores y managers que hacen seguimiento de acuerdos.  
**Requisitos:** acceso autorizado al conector ARCHISOFT con la cuenta corporativa propia. La consulta devuelve únicamente lo que los permisos del usuario autenticado permiten ver.  
**Estado de validación:** Documentado · Revisado documentalmente. **No probado con MCP ni validado funcionalmente.**

## Propósito

Contrastar los compromisos de una minuta o del CRM con las tareas y actividades registradas.

## Qué información se espera obtener

Tabla con compromiso, fuente, evidencia en CRM, estado verificable y siguiente paso.

## Prompt para copiar

Copia el bloque completo: incluye las reglas de uso que delimitan la consulta.

```text
Actúa como analista de proyectos de Architectural Solutions LLC / Archisolut. Contrasta compromisos que te proporcione en una minuta o que estén registrados en el CRM con las tareas y actividades actuales de los proyectos.

**Revisa lo siguiente:**
- Extrae compromiso, responsable, fecha y proyecto de la fuente disponible.
- Busca evidencia de cumplimiento o avance en CRM.
- Clasifica confirmado, abierto, no verificable.
- Identifica los compromisos que requieren recordatorio.

**Entrega:** Tabla compromiso | fuente | evidencia CRM | estado verificable | siguiente paso. No conviertas suposiciones en cumplimientos.

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

**Origen:** biblioteca ARCHISOFT preparada por el equipo de Archisolut (`archisolut-prompt-library`, edición 25 de noviembre de 2026), prompt `08-seguimiento-de-compromisos-de-reunión.md`.

**Nota de publicación:** las referencias a nombres internos de herramientas y a límites técnicos del conector se expresaron de forma funcional para su publicación. La finalidad operativa del prompt no se alteró.
