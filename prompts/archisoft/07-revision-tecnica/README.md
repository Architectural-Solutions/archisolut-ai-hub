# Revisión técnica (PCL y MEF)

Esta categoría contiene los dos prompts que **acompañan** la revisión final de las disciplinas técnicas:

- [16. Revisión final PCL asistida con documentos](16-revision-final-pcl-asistida-con-documentos.md) — plomería, civil, landscape, piscinas y séptico (OSTDS).
- [17. Revisión final MEF asistida con documentos](17-revision-final-mef-asistida-con-documentos.md) — mecánica, eléctrica y protección contra incendio.

## Los procedimientos originales de jefatura no se publican aquí

La biblioteca de origen incluye dos documentos extensos con el procedimiento de revisión final redactado por jefatura (`revision-final-pcl-original.md` y `revision-final-mef-original.md`). **No se incorporan a este repositorio público.**

Motivo: contienen criterios internos de aceptación, nombres de personas de la organización, referencias a formatos y registros internos de control, y reglas internas de gestión del trabajo. Su divulgación pública no aporta valor al colaborador y sí expone método propio y datos de personas.

Esos documentos deben conservarse en una **ubicación interna de acceso restringido** (Archisolut Knowledge Vault o la carpeta de jefatura que corresponda), no en GitHub.

### Qué cubre cada original (descripción, no contenido)

| Documento | Alcance | Incluye criterios sobre |
| --- | --- | --- |
| Revisión final PCL | Plomería, civil, landscape, piscinas y séptico OSTDS | Fases y rondas, clasificación de observaciones, coordinación con arquitectura y site plan, F006, correcciones de cliente, documentación especializada, comentarios de ciudad y formato de salida |
| Revisión final MEF | Mecánica, eléctrica y fire | Fases y rondas, clasificación de observaciones, coordinación con arquitectura y life safety plan, F006, cálculos, comentarios de ciudad y de bomberos, y formato de salida |

### Cómo se usan entonces los prompts 16 y 17

1. Solicita a jefatura el procedimiento original por un canal autorizado.
2. Adjunta en la conversación el procedimiento original **completo** y los documentos del proyecto (set de planos, F006, cálculos, comentarios de ciudad).
3. Ejecuta el prompt 16 o 17 de esta carpeta.

Sin esos documentos la revisión está incompleta: ARCHISOFT consulta el CRM, **no abre planos, PDFs ni cálculos**. Ninguna salida de estos prompts es una aprobación técnica, y ninguna debe firmarse con el nombre del responsable de revisión final sin su autorización expresa.
