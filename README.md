# Hybrid Infra as Code

Infraestructura híbrida (on-premises + Azure) gestionada íntegramente como código: nada se crea ni se configura a mano, todo nace de un commit.

## Objetivos

- Desplegar máquinas on-premises y en Azure de forma declarativa con Terraform
- Configurar los roles de cada máquina (Active Directory, servidor de ficheros) con Ansible
- Sincronizar la identidad del directorio local con Entra ID (Azure AD) y aplicar Conditional Access
- Monitorizar disponibilidad (Zabbix) y seguridad (Wazuh) de todo el entorno
- Documentar cada fase como se haría en un entorno de trabajo real

## Entorno

| Componente | Herramienta |
|---|---|
| Infraestructura como código | Terraform |
| Configuración | Ansible |
| Directorio local | Active Directory (Windows Server) |
| Identidad en la nube | Microsoft Entra ID (Azure AD) + Azure AD Connect |
| Control de acceso en la nube | Conditional Access |
| Monitorización de disponibilidad | Zabbix |
| Seguridad | Wazuh |
| Hipervisor | VMware Workstation |

## Fases del proyecto

| Fase | Contenido | Estado |
|---|---|---|
| Fase 0 | Repositorio y estructura | En curso |
| Fase 1 | Red y máquinas base | Pendiente |
| Fase 2 | Terraform — provisión declarativa | Pendiente |
| Fase 3 | Ansible — configuración de roles | Pendiente |
| Fase 4 | Identidad híbrida (Azure AD Connect + Conditional Access) | Pendiente |
| Fase 5 | Observabilidad (Zabbix + Wazuh) | Pendiente |
| Fase 6 | Documentación y cierre | Pendiente |

## Estructura del repositorio

- `terraform/`: código que define y crea las máquinas
- `ansible/`: playbooks que configuran las máquinas ya creadas
- `docs/`: guía paso a paso de cada fase

## Aviso

Todas las pruebas se realizan en un laboratorio aislado y propio, sobre máquinas y suscripciones creadas para este proyecto.

## Autor

Abdelhamid Boughafour · LinkedIn
