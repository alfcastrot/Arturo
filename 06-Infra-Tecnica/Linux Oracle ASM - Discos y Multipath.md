# Linux Oracle ASM - Discos y Multipath

## Proposito

Verificacion de discos, multipath y ASM en Linux / Oracle.

## Comandos principales

```text
/etc/init.d/oracleasm querydisk -v -d -p DATA01
asmcmd lsdsk -k
asmcmd lsdsk -gk -G datadg
asmcmd lsdg -g datadg
```

## Referencias de multipath

```text
multipaths {
 multipath {
  wwid 36589cfc000000580ddee277e9cda411e alias mpdata1
 }
 multipath {
  wwid 36589cfc00000025b4072a1536ade2f9d alias mpdata2
 }
 multipath {
  wwid 36589cfc000000f5feabc996aa1a12876 alias mpfra1
 }
}
```

## Notas

- `oracleasm querydisk` valida la asociacion del disco.
- `lsdsk` y `lsdg` sirven para revisar estado y capacidad del diskgroup.
- `multipath` ayuda a mapear WWIDs y aliases.
