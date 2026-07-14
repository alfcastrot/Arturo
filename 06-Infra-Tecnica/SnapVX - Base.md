# SnapVX - Base

## Proposito

Comandos y ejemplos para snapshots SnapVX.

## Comandos principales

```text
symsnapvx -sg database_sg list
symsnapvx -sid <SymmID> -name <SnapshotName> -file <DeviceFileName> -noprompt
symsnapvx -sid <SymmID> -file <DeviceFileName> -snapshot_name <SnapshotName> -generation <GenerationNumber> list
symsnapvx -sid <SymmID> -lnsg <SgName> -snapshot_name <SnapshotName> -generation <GenerationNumber> list -linked -by_tgt
symsnapvx -sid <SymmID> -sg <SgName> -snapshot_name <SnapshotName> -generation <GenerationNumber> list -summary
symsnapvx -sid 281 -sg SG_EPMPO27_CLUSTER_MPOLO -lnsg SG_EPMPO27_SnapVX_MPOLO -snapshot_name MPolo_OW_12-Horas -gen 0 relink -nop -v
symsnapvx -sid 281 -sg SG_EPMPO34_DATA -lnsg SG_EPMPO34_SnapVX -snapshot_name Open_24-Horas -gen 0 relink -nop -v
```

## Comandos relacionados

```text
symsg -sid 1234 -sg MyStorageGroup add sg ChildSG1,ChildSG2,ChildSG3
```

## Notas

- `list` muestra el estado de snapshots, `relink` vuelve a apuntar al target.
- Guarda aqui solo sintaxis de snapshot y ejemplos de uso.
