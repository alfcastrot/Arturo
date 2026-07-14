# working-context

Contexto activo actual:
- Hermes revisado y alineado como asesor tecnico/estrategico en espanol.
- La base compartida ahora tiene `index.md` y plantilla de decisiones para reutilizar conocimiento entre agentes.
- El esquema de 3 capas ya esta aterrizado para uso de los agentes en `99-Shared/MODELO_3_CAPAS_AGENTES.md`.
- Ya existen plantillas compartidas para `summary`, `research note` y `decision review`.
- Ya existe una guia para decidir que plantilla usar segun el caso.
- Ya existen `log.md`, `sources-map.md` y un workflow de `ingest/query/lint`.

Estado:
- `~/.hermes/config.yaml` ahora usa `display.personality: technical` y `display.language: es`.
- `~/.hermes/SOUL.md` define a Hermes como asesor de Alfredo y Arturo.
- Hermes esta instalado y autenticado con OpenAI Codex, pero una prueba oneshot fallo por `HTTP 429: The usage limit has been reached`.
- `hermes doctor --fix` ya migro config v24 -> v26; quedan dependencias browser con 2 vulnerabilidades high y llaves/proveedores opcionales faltantes.
- El vault `Arturo` quedo conectado a GitHub y sincronizado correctamente.
- Repo remoto: `https://github.com/alfcastrot/Arturo.git`.
- El estado de Git quedo limpio; Google Drive queda solo como respaldo espejo.

Siguiente accion:
- Resolver provider/limite Codex y decidir si levantar Hermes gateway o mantenerlo como consultor CLI interno.

Regla:
Mantener este archivo corto. No usarlo como diario completo.
