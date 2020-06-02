# Características principales de Red Hat Virtualization </h1>

### Carateristicas Basicas.
* Migración en vivo
* Fijación de CPU
* Control de acceso basado en roles y acceso escalonado
* Administración de energía
* Plantillas de VM
* Cortafuegos / SELinux
* Soporte para Red Hat Enterprise Linux y Windows
* HA máquinas virtuales
* Soporte NUMA
* Gestión basada en navegador
* Paso de PCI
* Paso USB
* API REST
* Python y Java SDK

### Características avanzadas
* Host afinidad / anti-afinidad
* Migrar / importar máquinas virtuales
* Gestión automatizada de recursos / equilibrio de carga
* CPU QoS
* Despliegue automatizado de hipervisor
* Agregar memoria y CPU en caliente
* Reserva de recursos
* Reinicio automático de VM
* Sobrecompromiso (aumento de memoria)
* Compartir páginas de memoria
* Soporte de página grande
* Importar máquinas virtuales de VMware
  
La herramienta virt-v2v permite importar máquinas virtuales directamente desde VMware. Un botón Importar está disponible en Red Hat Virtualization Manager.

### Funciones de red
* Etiquetado de VLAN
* QoS de red
* Vinculación NIC
* Soporte VM-FEX
* Abra vSwitch (vista previa técnica)
* Soporte de IPv6 (dentro del SO huésped)
* Marcos jumbo
* Etiquetas de red

### Características de almacenamiento
* Almacenamiento de migración en vivo
* iSCSI, NFS, FC, POSIX, GlusterFS
* Instantáneas en vivo / fusión
* API REST para copia de seguridad / restauración
* QoS de almacenamiento
* Aprovisionamiento  preallocated—or thick-provisioned—disks

### Límites
* CPU lógicas por hipervisor = 240
* Núcleos por hipervisor = Ilimitado
* RAM por hipervisor = 12 TB
* VM por hipervisor = No hard limit
* Hosts por cluster = 250
* VM por clúster = No hard limit
* VCPU por VM = 240
* RAM por VM = 4 TB


## Integración de Red Hat Virtualization
### Red Hat CloudForms
* Comparación de deriva VM
* Análisis de VM
* Seguir la genealogía de VM
* Capacidad y utilización
* Capture cronogramas de eventos de infraestructura
* Capture líneas de tiempo de eventos de VM / instancia
* Optimización por identificación de cuellos de botella
* Informes
* Dimensionamiento correcto
* Contracargo
* Aplicación de cumplimiento de host
* Aplicación de políticas de host
* Aplicación de cumplimiento de VM / instancia
* Aplicación de políticas de VM / instancia
* Operaciones de energía de VM / instancia
* VM / retiro de instancia
* Control integra el servicio web
* Integrarse con catálogos de servicios.
* Flujos de trabajo de automatización
* Automatizar API REST (provisión)
* Ejecución remota (a través de proxy si es necesario)
* Aprovisionamiento de VM / instancia usando PXE
* Aprovisionamiento de VM / instancia usando ISO
* Provisión de plantilla / imagen a VM / instancia

### Satélite Red Hat
* Aprovisionar y actualizar nodos y máquinas virtuales:
* Actualización de un clic para hosts
* Hacer cumplir las normas, incluido OpenSCAP
* Red Hat Virtualization Manager puede consultar erratas para hosts e invitados
* Reciba y aplique actualizaciones de software de Satellite

## Plataforma Red Hat OpenStack
### Neutron
* Utilice el agente nativo de OVS ML2 para descargar la configuración de red de las máquinas virtuales y el control del plano de datos
* Admite operaciones de solo lectura que permiten al usuario encontrar redes externas, importarlas y adjuntarlas a máquinas virtuales

### Glance
* Use, comparta y exporte imágenes y plantillas entre Red Hat Virtualization y Red Hat OpenStack Platform

### Cinder
* Configurar dominios de almacenamiento Ceph a través de Cinder
* Descargue el almacenamiento para mejorar el aprovisionamiento de VM y las E / S de almacenamiento

