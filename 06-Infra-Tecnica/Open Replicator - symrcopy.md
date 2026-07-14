# Open Replicator - symrcopy

## Proposito

Comandos de Open Replicator para crear, consultar y cerrar sesiones.

## Comandos principales

```text
symrcopy create -copy -name Ben_1 -pull -hot -file 3Par-pull.txt -nop -v
symrcopy query -session_name orsession -detail
symrcopy query -file 3par-Pull.txt -nop
symrcopy -file 3par-Pull.txt activate -consistent -nop -v
symrcopy -file 3Par-Pull.txt set donor_update off -consistent -nop
symrcopy -file 3par-Pull.txt terminate -nop
symrcopy terminate -name rcopy_1 -nop -v -symforce
symrcopy create -copy -name test-1910 -pull -hot -file test1910.txt -nop -v -donor_update
symrcopy -file test1910.txt query
symrcopy -file test1910.txt set donor_update off -consistent -nop
```

## Notas

- El flujo normal es `create` -> `query` -> ajustes -> `terminate`.
- `donor_update off` se usa cuando quieres detener actualizaciones hacia el donante.
