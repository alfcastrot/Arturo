# Uso del Vault

## Proposito

Reglas simples para trabajar en `Arturo` sin romper la organizacion ni la sincronizacion.

## Flujo diario

1. Abre `Arturo` en Obsidian.
2. Edita siempre en la carpeta local.
3. Guarda cambios en la nota correspondiente.
4. Si el cambio importa, ejecuta:
   - `git add .`
   - `git commit -m "<mensaje claro>"`
   - `git push`

## Reglas

- Git es la fuente principal de versionado.
- GitHub es el respaldo remoto.
- Google Drive solo se usa como espejo o respaldo.
- No editar el mismo archivo al mismo tiempo en varios sistemas.
- No guardar notas temporales fuera de la carpeta indicada.

## Carpetas clave

- `00-Core` reglas y contexto base.
- `06-Infra-Tecnica` comandos y referencias tecnicas.
- `90-Logs` historial diario.
- `99-Shared` plantillas y material comun.

## Criterio rapido

- Si es decision: se documenta.
- Si es error repetible: se registra.
- Si es comando util: se guarda en la nota tecnica correcta.
- Si es ruido temporal: se deja fuera o se elimina.
