# AIX - Discos y Arranque

## Proposito

Comandos de diagnostico y administracion de discos, LVM y arranque en AIX.

## Comandos principales

```text
df -Pg
lqueryvg -Atp hdXXXXXXX
smitty
bootlist -m normal -o
bootlist -m normal -o hdiskX
lsmpio -ql hdisk0
lscfg -vl hdisk1
lsvg -o | lsvg -i -l
lspv | grep -i rootvg
lsdev -Cc adapter | grep -i fcs
lspath
lspv -u
lsdev -Cc disk
getconf DISK_SIZE /dev/hdisk0
lsmpio -q | hdiskXX
/usr/bin/rescan-scsi-bus.sh -a -r
```

## Utilidades

```text
for i in `lspv | awk '{print $1}'`; do bootinfo -s $i; done
```

## Notas

- `bootlist` y `bootinfo` ayudan con arranque y tamanio.
- `lsmpio`, `lspath`, `lspv` y `lsdev` sirven para trazabilidad de discos.
- `rescan-scsi-bus.sh` queda aqui como utilidad de reescaneo.
