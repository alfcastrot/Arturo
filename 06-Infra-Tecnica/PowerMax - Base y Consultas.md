# PowerMax - Base y Consultas

## Proposito

Comandos base para consultar, crear y validar objetos PowerMax / Symmetrix.

## Comandos principales

```text
symcfg list -ra all
symcfg list -sid XXXX -rdfg all
symcfg -sid 1234 list -rdfg all -dynamic
symcfg -sid 1910 list -tdev -sg SG_EPMPS14 -detail -gb
symcfg -sid 918 list -devs 00210,00228,0010B,0020E,00211,0010C,0020F,0010A,0010D,00161,0022B,0018B,0020D,00229 -cyl
symcfg -sid 1910 list -rdfg all -dynamic

symdev -sid 1910 list -devs 0050-0060 -wwn
symdev -sid 1910 list -devs 0050-0060 -identifier device_name
symdev -sid 1910 list -metroDR
symdev -sid 1910 list -sg SG_EPM-PS28-CLUSTER -identity -cyl
symdev -sid 910 list -wwn -sg SG_EPMCDP-PO27
symdev -sid 918 list -sg SG_EPM-PS28-CLUSTER -identity -cyl

symaccess -sid 1234 create view -name test -pg unix1 -ig test1 -sg test1
symaccess -sid 1234 list -type storage -dev AAA
symaccess -sid 1910 list -type storage -devs 0093-009a
symaccess -sid 1910 list -type port
symaccess -sid 1910 list -type Initiator
symaccess -sid 1234 list -type storage -dev AAA
```

## Notas

- `symcfg` y `symdev` son la base para identificar arrays, devs, RDFG y storage groups.
- `symaccess` sirve para views, initiators, ports y mapping de acceso.
- Si un comando se repite en otra nota, aquí queda la forma canonica.
