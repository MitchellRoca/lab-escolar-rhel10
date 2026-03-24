# 🏛️ Enterprise-School: Infraestructura RHEL 10 🚀

> **Simulación de Arquitectura Escolar de Alto Rendimiento**
> *Un proyecto nacido de la pasión por el Open Source y la ingeniería de sistemas.*

[![RHEL 10](https://img.shields.io/badge/OS-RHEL--10.1-red?style=for-the-badge&logo=redhat)](https://www.redhat.com/)
[![Hypervisor](https://img.shields.io/badge/Virtualization-KVM%20%2F%20QEMU-blue?style=for-the-badge&logo=linux)](https://www.linux-kvm.org/)
[![Status](https://img.shields.io/badge/Status-In--Progress-orange?style=for-the-badge)](https://github.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

## 🌟 Visión del Proyecto
Este no es solo un laboratorio; es un **desafío técnico personal**. Mi objetivo es desplegar una infraestructura "On-Premise" completa para un **Sistema Escolar**, validando cada bit de configuración bajo estándares de producción. 

Construyo esto porque me apasiona entender cómo el kernel, el almacenamiento y la red se entrelazan para crear servicios resilientes. **Sin atajos, sin internet (Offline-First), solo ingeniería pura.**

---

## 🏗️ Arquitectura de Red (Multi-Nodo)

He segmentado la infraestructura en **4 pilares estratégicos** para garantizar la máxima seguridad y eficiencia:

| Nodo | Icono | Rol Técnico | Stack |
| :--- | :---: | :--- | :--- |
| **srv-admin** | 🛠️ | **Control Central** | SSH Bastion, Ansible Ready, Logs |
| **srv-web** | 🌐 | **Frontend** | Apache httpd, PHP 8.x, Hardening |
| **srv-db** | 🗄️ | **Capa de Datos** | MariaDB Server, SQL Optimization |
| **srv-storage**| 📦 | **Recursos** | LVM, NFS Export, Backup Vault |

> [!TIP]
> **Estrategia Offline:** Todo el software se gestiona mediante el montaje de la ISO `rhel-10.1-x86_64-dvd.iso`. Cero dependencias externas.

---

## 🛣️ Roadmap de Ingeniería (Fases)

| Fase | Estado | Descripción |
| :--- | :---: | :--- |
| **01. Bootstrap** | ✅ | Preparación de Host KVM y despliegue de imagen base. |
| **02. Core Networking** | 🔄 | Configuración de red privada e IP estáticas. |
| **03. Hardening** | ⏳ | Firewalld, SELinux Booleans y políticas de acceso. |
| **04. Storage Layer** | ⏳ | Aprovisionamiento de LVM y montajes NFS remotos. |
| **05. Service Stack** | ⏳ | Despliegue de MariaDB + Apache (Sistema Escolar). |
| **06. Chaos Testing** | ⏳ | Pruebas de reinicio, logs y recuperación de fallos. |

---

## 🛠️ Áreas de Dominio Técnico

### 🛡️ Seguridad y Resiliencia
* **SELinux:** Administración de contextos `httpd_sys_content_t` y booleanos de red.
* **Firewalld:** Segmentación por zonas (Internal/Public) y gestión de servicios persistentes.
* **Systemd:** Creación y gestión de unidades de servicio para garantizar el *uptime*.

### 📊 Gestión de Datos
* **LVM Superior:** Expansión de volúmenes en caliente y gestión de Physical Volumes (PV).
* **NFS & Autofs:** Montajes bajo demanda para optimizar recursos de red.

---

## 📁 Estructura del Repositorio

```bash
laboratorio-escolar-rhel10/
├── 📂 fases/              # 📝 Guías de ejecución paso a paso
├── 📂 docs/               # 🗺️ Diagramas de red y arquitectura
├── 📂 runbooks/           # 📕 Comandos rápidos y configuraciones
├── 📂 troubleshooting/    # 🔧 Bitácora de errores (La zona de aprendizaje)
├── 📂 validation/         # ✅ Checklists post-reinicio
└── 📂 assets/             # 📸 Evidencia visual y capturas
