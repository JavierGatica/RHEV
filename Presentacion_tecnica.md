# Arquitectura de virtualización de Red Hat


### El corazón de Red Hat Virtualization es KVM.

Al igual que con cualquier plataforma de virtualización, Red Hat Virtualization abstrae las muchas capas de recursos informáticos, es decir, abstrae el hardware de la carga de trabajo y la aplicación. Esto lo hace el hipervisor KVM.

*El hipervisor KVM tiene tres componentes principales:*

* El módulo de kernel KVM interactúa directamente con las tecnologías de hardware que permiten la virtualización como AMD-V e Intel VT que descargan las llamadas de virtualización directamente al hardware físico.
* QEMU es un emulador de dispositivo que proporciona la interfaz en el módulo del kernel KVM y define el grupo de dispositivos virtuales que conforman la máquina virtual y se pasan para ser procesados en el hardware físico.
* La API de libvirt es la API de virtualización estándar de la industria. Se utiliza para administrar y controlar la funcionalidad de QEMU, como la creación, el inicio, la detención y la migración de máquinas virtuales.
* VDSM, que es la abreviatura de Virtual Desktop y Server Manager, es el agente host. Inicia acciones en máquinas virtuales y almacenamiento y también facilita la comunicación entre host. VDSM supervisa los recursos del host, como la memoria, el almacenamiento y las redes. Además, VDSM gestiona tareas como la creación de máquinas virtuales, la acumulación de estadísticas y la recopilación de registros. Una instancia de VDSM se ejecuta en cada host y recibe comandos de administración de Red Hat Virtualization Manager.
* qemu-kvm-rheves el hipervisor de Red Hat Virtualization. Es una versión personalizada del espacio de usuario QEMU-KVM y la tecnología del núcleo que convierte a Red Hat Enterprise Linux en un hipervisor e incluye componentes para la gestión centralizada de una infraestructura virtual distribuida a través de Red Hat Virtualization Manager.
