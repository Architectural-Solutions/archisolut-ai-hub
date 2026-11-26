# 16. Revisión final PCL asistida con documentos

**Categoría:** Revisión técnica  
**Público recomendado:** Revisión técnica de PCL con acompañamiento de jefatura.  
**Requisitos:** acceso autorizado al conector ARCHISOFT con la cuenta corporativa propia. La consulta devuelve únicamente lo que los permisos del usuario autenticado permiten ver.  
**Estado de validación:** Documentado · Revisado documentalmente. **No probado con MCP ni validado funcionalmente.**

## Propósito

Apoyar la revisión final de PCL aplicando el procedimiento interno de jefatura sobre los documentos del proyecto.

## Qué información se espera obtener

La salida del procedimiento interno de jefatura, que no se reproduce en este repositorio público.

## Prompt para copiar

Copia el bloque completo: incluye las reglas de uso que delimitan la consulta.

```text
Actúa como analista de proyectos de Architectural Solutions LLC / Archisolut. Trabaja con el prompt original de revisión PCL de jefatura (documento interno de distribución restringida, no incluido en este repositorio público); solicítalo por un canal autorizado y aplícalo al proyecto que te indique solo después de recibir el set y documentos requeridos.

**Revisa lo siguiente:**
- Usa el documento original como fuente íntegra de criterios.
- Confirma fase, ronda y F006 antes de marcar faltantes.
- Valida planos de plomería, civil, landscape, piscinas y séptico cuando correspondan.
- Separa ERROR, CORRECCIÓN, PREGUNTA, PENDIENTE EXTERNO, VERIFICAR e INFORMATIVO.

**Entrega:** Reproduce el formato de salida del prompt original; no firmes con el nombre del responsable de revisión final de jefatura: el resultado es un borrador que requiere su revisión y autorización expresa.

- Emplea **ARCHISOFT (MCP de Archisolut)** como fuente de datos operativos de EspoCRM, con los permisos del usuario autenticado y en **solo lectura**. No intentes saltar permisos, modificar registros ni usar otras credenciales.
- Antes de consultar muchos registros, delimita **disciplina, equipo, proyecto y periodo**. Identifica la disciplina mediante los datos disponibles; si no es inequívoca, pregunta cuál revisar. No infieras que todos los proyectos visibles pertenecen al equipo del usuario.
- Consulta las capacidades de historial y seguimiento disponibles en ARCHISOFT, respetando las herramientas expuestas, los permisos del usuario y los límites de consulta aplicables. Si no existe una capacidad o faltan campos, señálalo. Si necesitas recuperar múltiples registros, utiliza la paginación permitida y no presentes resultados parciales como completos. Empieza por consultas pequeñas y específicas, y escala únicamente si hace falta.
- Distingue hechos con **identificador, proyecto y fecha** de hipótesis, y distingue **sin registros visibles** de **sin actividad real**. No inventes cifras, estados ni responsables.
- ARCHISOFT no equivale automáticamente a acceso a PDFs, planos, F006, correos o archivos externos. Para análisis técnico de entregables, pide adjuntar los documentos necesarios. Nunca dictamines conformidad de un plano que no has visto.
- No uses el nombre de otra persona como firma de un informe o correo sin autorización. Los resultados son borradores sujetos a revisión humana.

**Requisito documental:** Adjunta además el prompt original completo y los documentos del proyecto. No sustituyas el procedimiento técnico del original por un resumen.
```

## Limitaciones y verificaciones necesarias

- El resultado es un **borrador** sujeto a revisión humana; no constituye aprobación técnica ni cierre de una tarea.
- ARCHISOFT es **solo lectura**: no modifica estados, no reasigna tareas y no envía correos.
- Lo que no aparece en el CRM no existe para esta consulta. Distingue siempre **«sin registros visibles»** de **«sin actividad real»**.
- El acceso a un proyecto no implica responsabilidad sobre él ni autoriza a deducir la estructura completa del equipo.
- Para cualquier dictamen sobre planos, cálculos, PDFs o F006 hacen falta los documentos: el conector de CRM no los sustituye.

---

**Origen:** biblioteca ARCHISOFT preparada por el equipo de Archisolut (`archisolut-prompt-library`, edición 25 de noviembre de 2026), prompt `16-revisión-final-pcl-asistida-con-documentos.md`.

**Nota de publicación:** se ajustó el texto para no incluir un nombre personal como firma ni rutas de documentos internos no publicados, y las referencias a nombres internos de herramientas y a límites técnicos del conector se expresaron de forma funcional. Los criterios técnicos no se alteraron.
