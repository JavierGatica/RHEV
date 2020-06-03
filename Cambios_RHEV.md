# What is New or Changed </h1>

### Modernización de Infraestructura
* Soporte de Red Hat Virtualization Manager para Red Hat Enterprise Linux 7.2
* Hipervisor de próxima generación
* Soporte de Red Hat Enterprise Linux Atomic Host
* Políticas de migración avanzadas
* Afinidad basada en etiquetas

# Arquitectura de virtualización de Red Hat
### KVM
El corazón de Red Hat Virtualization es KVM.

Al igual que con cualquier plataforma de virtualización, Red Hat Virtualization abstrae las muchas capas de recursos informáticos, es decir, abstrae el hardware de la carga de trabajo y la aplicación. Esto lo hace el hipervisor KVM.

El hipervisor KVM tiene tres componentes principales:
* El módulo de kernel KVM interactúa directamente con las tecnologías de hardware que permiten la virtualización como AMD-V e Intel VT que descargan las llamadas de virtualización directamente al hardware físico.
* QEMU es un emulador de dispositivo que proporciona la interfaz en el módulo del kernel KVM y define el grupo de dispositivos virtuales que conforman la máquina virtual y se pasan para ser procesados ​​en el hardware físico.
* La API de libvirt es la API de virtualización estándar de la industria. Se utiliza para administrar y controlar la funcionalidad de QEMU, como la creación, el inicio, la detención y la migración de máquinas virtuales.

Otros componentes principales de Red Hat Virtualization también se relacionan específicamente con KVM y diferencian a Red Hat Virtualization de un hipervisor KVM básico.

* VDSM, que es la abreviatura de Virtual Desktop y Server Manager, es el agente host. Inicia acciones en máquinas virtuales y almacenamiento y también facilita la comunicación entre host. VDSM supervisa los recursos del host, como la memoria, el almacenamiento y las redes. Además, VDSM gestiona tareas como la creación de máquinas virtuales, la acumulación de estadísticas y la recopilación de registros. Una instancia de VDSM se ejecuta en cada host y recibe comandos de administración de Red Hat Virtualization Manager.

* qemu-kvm-rhev es el hipervisor de Red Hat Virtualization. Es una versión personalizada del espacio de usuario QEMU-KVM y la tecnología de kernel que convierte a Red Hat Enterprise Linux en un hipervisor e incluye componentes para la gestión centralizada de una infraestructura virtual distribuida a través de Red Hat Virtualization Manager.

### Next-Generation Node
* Red Hat Virtualization Host: nodo especialmente diseñado creado en Red Hat Enterprise Linux
* Se puede implementar a través de ISO, PXE, USB, clonado
* Sistema de archivos raíz grabables
* Utiliza el instalador de Anaconda recortado
* Cockpit administrative console
* Seguridad y servicios optimizados para admitir máquinas virtuales

### Red Hat Enterprise Linux Thick Node
* Red Hat Virtualization 4 supports Red Hat Enterprise Linux 7 as a node
* Uses qemu-kvm-rhev package
* Larger footprint than Red Hat Virtualization node
* Red Hat Virtualization Manager configures security and VDSM


### Red Hat Virtualization Deep Dive.
Desde un punto de vista informático, Red Hat proporciona máquinas virtuales a los usuarios para implementar aplicaciones. Red Hat tiene medios para organizar lógica y automáticamente máquinas virtuales:

* En el lenguaje de Red Hat Virtualization, un centro de datos es un grupo de clústeres que comparten el mismo almacenamiento. Un entorno de virtualización de Red Hat puede admitir muchos centros de datos lógicos separados.
* Un clúster es un grupo de hosts o hipervisores con la misma CPU que comparte redes lógicas. Un centro de datos de Red Hat Virtualization puede contener muchos clústeres.
* Una máquina virtual puede migrar en vivo entre hosts en el mismo clúster.
* Las máquinas virtuales pueden equilibrarse automáticamente.

El diagrama resalta los siguientes detalles:

* El centro de datos de la izquierda contiene un solo grupo de dos hipervisores. Ese centro de datos también proporciona almacenamiento y recursos de red a esos hipervisores para que puedan admitir las máquinas virtuales mencionadas anteriormente.

El centro de datos a la derecha contiene dos grupos. Esos clústeres comparten el mismo almacenamiento en el centro de datos 2, pero no tienen acceso al almacenamiento en el centro de datos 1. Los clústeres pueden acceder a las diferentes redes disponibles en el centro de datos 2.

Es posible que deba dividir los centros de datos en función de la aplicación, la unidad de negocios, la preparación, el ciclo de vida del desarrollo o el programa de respaldo. Es posible que deba dividir clústeres en función de las necesidades de CPU, memoria o red.

También es importante tener en cuenta que los recursos se pueden reasignar automáticamente, es decir, con equilibrio de carga, en función de diferentes umbrales.

### Seguridad informática: SELinux y sVirt
* Debido a que Red Hat Virtualization se basa en Red Hat Enterprise Linux, hereda las características de seguridad de Linux con seguridad mejorada (SELinux)
* SELinux basado en etiquetado
* Los procesos obtienen etiquetas, y las máquinas virtuales en KVM / QEMU son procesos
* Los archivos y dispositivos también reciben etiquetas, incluidas imágenes virtuales
* Las reglas de SELinux controlan cómo interactúan los procesos con las etiquetas de archivos y procesos.
* A su vez, sVirt dicta cómo los procesos interactúan con archivos y etiquetas de proceso que interactúan con archivos, procesos y libvirt relacionados con la virtualización.


### Seguridad informática - SELinux
* Implementación de MAC en el kernel de Linux
* Verifica las operaciones permitidas después de verificar los controles de acceso discrecional (DAC) estándar
* Puede aplicar una política de seguridad personalizable por el usuario en los procesos en ejecución y sus acciones, incluidos los intentos de acceder a los objetos del sistema de archivos
* Habilitado por defecto en Red Hat Enterprise Linux
* Limita el alcance del daño potencial que puede resultar de la explotación de vulnerabilidades en aplicaciones y servicios del sistema como hipervisores

### Seguridad informática - sVirt
* libvirt es la capa de abstracción de gestión de virtualización
* sVirt se integra con libvirt para proporcionar el marco MAC para máquinas virtuales
* La arquitectura permite que todas las plataformas de virtualización compatibles con libvirt y todas las implementaciones de MAC compatibles con sVirt interoperen
