# Fase 01: Preparación del Hipervisor y Red Base

## Objetivo
Configurar el Host local con KVM/QEMU y establecer la red virtual `colegio-net` para la comunicación entre los servidores del proyecto.

## Tareas Ejecutadas
1. **Habilitación de Libvirt:** Se activó el demonio de virtualización para persistencia tras reinicio.
2. **Definición de Red:** Creación de red NAT `192.168.100.0/24`.
3. **Validación:** Comprobación de estado activo y autoarranque.

## Comandos Principales
- `sudo systemctl enable --now libvirtd`
- `sudo virsh net-define colegio-net.xml`
- `sudo virsh net-start colegio-net`

## Evidencia Visual
- [Estado de Libvirt](./capturas/01-host-kvm-host-01-libvirt-activo.png)
- [Red Colegio Activa](./capturas/01-host-kvm-host-02-red-colegio-creada.png)
