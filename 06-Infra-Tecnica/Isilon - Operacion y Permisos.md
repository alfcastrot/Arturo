# Isilon - Operacion y Permisos

## Proposito

Servicios, permisos, Docker y comandos operativos auxiliares de Isilon / entorno.

## Comandos principales

```text
/etc/init.d/smas stop
/etc/init.d/smas start
/etc/init.d/smas status
/mnt/EMC/APG/bin/manage-modules.sh service status all
/mnt/EMC/APG/bin/manage-modules.sh service stop all
sudo /sbin/reboot vplex
docker exec -ti esrsde-app bash
systemctl stop esrswatchdog
postfix stop
docker container ls
docker stop Container
sudo systemctl start docker
isi_run -l VMTEST\\testuser1
isi event groups bulk --resolved=true
du -sSHAk /ifs/data
ls -ltr | wc -l
find -x / -type f -size +10000 -exec ls -lh {} \\; | awk '{ print $9 ": " $5 }'
```

## Permisos y ACL

```text
group:EPM\\ifs-admin allow dir_gen_read,dir_gen_write,dir_gen_execute,std_delete,object_inherit,container_inherit
group:EPM\\ifs-admin allow inherited dir_gen_all,object_inherit,container_inherit,inherited_ace
allow dir_gen_read,dir_gen_write,dir_gen_execute,std_write_dac,delete_child
allow dir_gen_all,object_inherit,container_inherit
user jparra allow dir_gen_all,object_inherit,container_inherit
user jparra allow inherited dir_gen_read,object_inherit,container_inherit,inherited_ace
chmod +a group everyone allow generic_all,object_inherit,container_inherit
chmod +a everyone allow dir_gen_all,object_inherit,container_inherit
chmod -RE *
chmod +a everyone allow read_data,execute,read_attributes,read_acl,object_inherit,container_inherit
```

## Notas

- `smas` y `manage-modules` van en el bloque de servicios.
- Docker y `isi event groups` quedan aqui por ser operacion diaria.
- Las ACL conviene revisar antes de ejecutar `chmod -RE *`.
