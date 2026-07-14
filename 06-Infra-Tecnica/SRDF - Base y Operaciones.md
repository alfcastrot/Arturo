# SRDF - Base y Operaciones

## Proposito

Comandos para crear, validar, mover, sincronizar y limpiar relaciones SRDF.

## Comandos principales

```text
symrdf -sid 1234 -rdfg 3 -type rdf1 -file rdf.txt createpair -establish -rdf_mode acp_disk
symrdf -sid 1234 -rdfg 3 -type rdf1 -file rdf.txt establish -full
symrdf -sid 1234 -rdfg 3 -type rdf1 -file rdf.txt -g mydg createpair -establish
symrdf -sid 123 -rdfg 3 -file xx createpair -type R1 -metro -exempt
symrdf -sid 046 -rdfg 101 -file PO33 createpair -establish -nop -v
symrdf -sid 046 -rdfg 101 -file PO33 set mode sync -nop -v
symrdf -sid 046 -rdfg 101 -file PO33 split -nop -v
symrdf -sid 046 -rdfg 101 -file PO33 deletepair -force -nop -v

symrdf -sid 281 -sg SG_EPMPO27_SnapVX -rdfg 100 verify -Synchronized
symrdf -sid 281 -sg SG_EPMPO27_SnapVX -rdfg 100 suspend -nop -v
symrdf -sid 281 -sg SG_EPMPO27_SnapVX -rdfg 100 establish -nop -v
symrdf -sid 281 -sg SG_EPMPO34_SnapVX -rdfg 101 suspend -nop -v
symrdf -sid 281 -sg SG_EPMPO34_SnapVX -rdfg 101 establish -nop -v

symrdf -g srdf_dg_Name set mode acp_disk -noprompt
symqos -g srdf_dg_Name set RDF priority 5
symrdf -g srdf_dg_Name establish -full -noprompt
symrdf -g srdf_dg_Name set mode sync -noprompt
symrdf -g srdf_dg_Name swap
symrdf -g srdf_dg_Name deletepair -noprompt
symdg delete srdf_dg_Name -force

symrdf -g DgName query -all
symrdf -g DgName query -summary
symrdf -sid SID -rdfg GrpNum -sg SgName query
symrdf -g srdf_dg_Name query
symrdf -g Migracion split
symrdf -sid 281 -sg SG_EPMPO27_SnapVX -rdfg 100 verify -Synchronized
symrdf -sid 000220200281 -label TEST-CAB -rdfg 51 -dir 3C:4,3C:5,4C:4,4C:5 -remote_sid 000220002480 -remote_rdfg 51 -remote_dir 1C:8,1C:9,2C:8,2C:9 addgr
symrdf -sid 1234 -rdfg 3 -type rdf1 -file rdf.txt createpair -establish -rdf_mode acp_disk
symrdf -sid 6180 -rdfg 4 set label newdyngrp4

symrdf -sid 1234 -rdfg 3 -type rdf1 -file rdf.txt -g mydg createpair -establish
symrdf -sid 1234 -rdfg 3 -type rdf1 -file rdf.txt establish -full
```

## Ciclo tipico

1. Crear o emparejar.
2. Establecer.
3. Verificar.
4. Sincronizar o cambiar modo.
5. Split / suspend si aplica.
6. Limpiar con `deletepair` y `symdg delete` cuando termina.

## Notas

- `addgrp` sirve para crear grupos RDF con direccionamiento remoto.
- Si el grupo metro queda vacio, se suele usar un disco dummy o `-exempt` antes de eliminar la sesion.
