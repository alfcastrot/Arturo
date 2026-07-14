# Isilon - Identidad y SyncIQ

## Proposito

Comandos de identidad, mapping, zonas, SyncIQ y verificacion de directorio.

## Comandos principales

```text
isi auth mapping dump --zone=<ACCESS ZONE> --file=<file>
isi auth mapping delete --all
isi auth mapping delete --name=username
isi auth mapping import --zone=<access_zone> --file=<file>
isi auth mapping list --zone=<access_zone>
isi auth status
isi auth status --verbose
isi auth mapping flush --all
isi auth cache flush --all

isi sync policies modify <policy_name> --target-compare-initial-sync=on
isi job start DomainMark --root=<patm> --dm-type=synciq
isi_classic domain list -l
isi_run -z XX -l "domain\\user" login en la Zona
isi zone zones modify --zone=EPM-FT03 --add-user-mapping-rules="EPM-HADOOPSV\\* &= * []"
isi zone zones modify --zone=EPM-FT03 --add-user-mapping-rules="EPM-HADOOPSV\\* += * [group]"
isi zone zones modify --zone=EPM-FT03 --add-user-mapping-rules="EPM-HADOOPSV\\* += * [groups]"
isi zone zones modify --zone=<zone-name> --add-user-mapping-rules="domain\\ambari-qa-<clsname> => ambari-qa[]"
isi_for_array -s "isi auth status | grep -i corp.xxx.org "
isi_for_array -n 4-6 'isi auth refresh'
isi_classic auth ads status --refresh --all
isi_for_array '/usr/likewise/bin/lwsm refresh nfs'
```

## Notas

- Este bloque cubre identidad, mappings, zonas y SyncIQ.
- `auth mapping dump/import/delete` sirve para migrar o limpiar mappings entre clusters.
- `DomainMark` y `zone modify` suelen ir juntos cuando ajustas autenticacion o mapeo.
