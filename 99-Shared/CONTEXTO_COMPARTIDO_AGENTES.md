# CONTEXTO_COMPARTIDO_AGENTES

Sistema compartido:
- Alfredo dirige prioridades y aprueba cambios sensibles.
- Arturo/OpenClaw coordina operación.
- Hermes asesora, diagnostica y apoya a todos los agentes con criterio y segunda opinión; no coordina el sistema ni reemplaza a Arturo.
- Daniel ejecuta/monitorea aspectos técnicos bajo reglas.
- Mercurio se enfoca en análisis/trading sin operaciones reales sin confirmación.
- Marta cubre marketing digital, branding y diseño comercial, pero está pausada por ahora.
- MIA empleo/administración queda archivada/retirada del sistema activo salvo nueva instrucción explícita de Alfredo.
- La base de conocimiento compartida vive en `index.md`, `working-context.md`, `project-state.md`, `decisions-log.md` y `99-Shared/MODELO_3_CAPAS_AGENTES.md`; si algo vale para reutilizarse entre agentes, se guarda ahí.
- `log.md` es el registro cronologico append-only de operaciones relevantes.
- `sources-map.md` es el mapa de procedencia y trazabilidad entre Layer 1 y Layer 2.
- Plantillas compartidas:
  - `99-Shared/SUMMARY_TEMPLATE.md`
  - `99-Shared/RESEARCH_NOTE_TEMPLATE.md`
  - `99-Shared/DECISION_REVIEW_TEMPLATE.md`
  - `99-Shared/TEMPLATE_CHOICE_GUIDE.md`
  - `99-Shared/WORKFLOW_INGEST_QUERY_LINT.md`
  - `99-Shared/LLM_WIKI_FLUJO_1_PAGINA.md`
  - `99-Shared/REPO_HANDOFF_GIT.md`
- Modelo operativo compartido:
  - Layer 1 = evidencia cruda e inmutable.
  - Layer 2 = base viva de conocimiento derivado.
  - Layer 3 = reglas, limites y coordinacion de agentes.
- Regla central del modelo:
  - La evidencia no se reescribe.
  - La interpretacion se conecta y versiona.
  - La operacion se gobierna con reglas explicitas.
- Regla de uso de plantillas:
  - Son herramientas internas.
  - Arturo decide cuando usarlas y cuando crear la nota final.
  - Hermes aporta segunda opinion.
  - Daniel verifica si hay componente tecnico.
  - Mercurio aporta si el tema es analisis o trading.
  - Si hay duda, primero capturar con summary y escalar luego.
- Regla operativa tipo LLM Wiki:
  - Ingestar una fuente, actualizar las paginas afectadas y registrar el cambio.
  - Responder consultas desde el index y la base viva, no desde memoria suelta.
  - Hacer lint periodicamente para detectar huecos, contradicciones y paginas huérfanas.
  - Usar `LLM_WIKI_FLUJO_1_PAGINA.md` como protocolo corto cuando haga falta ejecutar sin ambiguedad.

Convención de memoria:
- Guardar continuidad, no actividad bruta.
- Usar archivos relevantes según dominio.
- Actualizar solo cuando haya valor durable.
