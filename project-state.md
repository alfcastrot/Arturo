# project-state

## Memoria Operativa Arturo

Objetivo:
Crear una capa Markdown/Obsidian organizada para continuidad entre Arturo/OpenClaw, Hermes, Daniel y Mercurio.

Estado actual:
- Diseño aprobado por Alfredo.
- Vault base creado en /home/openclaw/Obsidian/Arturo.
- Conectado a agents.defaults.memorySearch.extraPaths.
- Reindexado y verificado: 56/56 archivos, embeddings/vector/FTS ready.
- AGENTS.md actualizado con reglas compactas de Memoria Operativa Arturo.
- Centro de Mando Arturo incorporó la ruta web `/english-avatar` como avatar de inglés responsivo para móvil y desktop.
- El avatar usa voz del navegador cuando está disponible y conserva estado en localStorage.
- Se añadieron `index.md` y la plantilla `decisions/decision-template.md` para usar la base de conocimiento compartida entre Arturo, Hermes, Daniel y Mercurio.
- Se añadió `99-Shared/MODELO_3_CAPAS_AGENTES.md` para formalizar el esquema de evidencia, base viva y operación.
- El contexto compartido ahora referencia explícitamente la capa de gobernanza y trazabilidad.
- Se añadieron plantillas compartidas para `summary`, `research note` y `decision review`.
- Se añadió `99-Shared/TEMPLATE_CHOICE_GUIDE.md` para decidir automaticamente cuando usar cada plantilla.
- Se añadieron `99-Shared/log.md`, `99-Shared/sources-map.md` y `99-Shared/WORKFLOW_INGEST_QUERY_LINT.md` para acercar el sistema al patrón LLM Wiki.
- Se añadió `99-Shared/LLM_WIKI_FLUJO_1_PAGINA.md` como protocolo operativo corto de una pagina.
- Se organizo el vault tecnico en `06-Infra-Tecnica/` con notas por categoria: PowerMax, SRDF, SnapVX, Open Replicator, Isilon, Linux Oracle ASM, AIX y Miscelaneos.
- Se dejo registrado el flujo Git del vault principal `Arturo`.
- Repo remoto conectado: `https://github.com/alfcastrot/Arturo.git`.
- `git status` final limpio y `main` siguiendo `origin/main`.
- `.gitignore` ajustado para ignorar cache y archivos temporales de Obsidian.

Arquitectura:
- Memoria interna compacta para preferencias y hechos críticos.
- Reglas operativas para comportamiento.
- Vault Markdown/Obsidian para estado, decisiones, errores y handoffs.
- Session search como historial bruto automatico.
