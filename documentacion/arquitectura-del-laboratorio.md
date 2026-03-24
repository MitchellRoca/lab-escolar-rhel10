
# Arquitectura del Laboratorio - lab-escolar-rhel10

Este laboratorio utiliza una topología de red aislada para simular un entorno escolar seguro.

## Topología de Red
- **Nombre de red:** `lab-escolar-net`
- **Tipo:** NAT (aislada con salida a internet controlada)
- **Segmento:** `192.168.100.0/24`
- **Gateway (Host):** `192.168.100.1`

## Nodos del Proyecto
| Hostname | IP Sugerida | Rol Técnico |
| :--- | :--- | :--- |
| `srv-admin` | `192.168.100.10` | Administración, SSH, Documentación |
| `srv-web` | `192.168.100.20` | Apache httpd + PHP (Portal Escolar) |
| `srv-db` | `192.168.100.30` | MariaDB (Base de datos de alumnos/noticias) |
| `srv-storage` | `192.168.100.40` | Almacenamiento NFS y Backups |
