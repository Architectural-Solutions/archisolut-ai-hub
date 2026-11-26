# Instalación — Codex

**Versión:** 1.0.0 · Archivo de referencia: `skills/archisolut-digital-brain/SKILL.md`

1. Descarga el ZIP específico de Codex en la Release de GitHub aprobada.
2. Revisa su contenido. Copia la carpeta `archisolut-digital-brain` completa a la ruta indicada en el ZIP: `paquetes/codex/.agents/skills/archisolut-digital-brain`.
3. Abre una sesión nueva y prueba: **«¿Qué es el Digital Brain de Archisolut? Indica qué documentos del Vault puedes abrir realmente; no escribas nada»**.
4. Si no aparece el Skill o la app no permite importarlo, copia el texto de `bootstrap/INSTRUCCION-PARA-CHATS.md` en la configuración del agente o al inicio de la conversación.
5. Si la conexión corporativa de Google Drive no está autorizada o no existe, la instalación **no da acceso** al Vault. Solicita conexión mediante los canales de TI; nunca compartas contraseñas o tokens.

**Notas de compatibilidad:** Copia dentro de `.agents/skills/` del proyecto que quieres contextualizar. La compatibilidad depende de la edición y entorno; no garantiza activación en chats independientes.

**Guía oficial de la plataforma:** https://developers.openai.com/api/docs/guides/tools-skills

No configures acciones automáticas ni modifiques permisos como parte de esta instalación.
