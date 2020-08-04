# Arquitectura de virtualización de Red Hat


### El corazón de Red Hat Virtualization es KVM.

Al igual que con cualquier plataforma de virtualización, Red Hat Virtualization abstrae las muchas capas de recursos informáticos, es decir, abstrae el hardware de la carga de trabajo y la aplicación. Esto lo hace el hipervisor KVM.

*El hipervisor KVM tiene tres componentes principales:*

* El módulo de kernel KVM interactúa directamente con las tecnologías de hardware que permiten la virtualización como AMD-V e Intel VT que descargan las llamadas de virtualización directamente al hardware físico.
* QEMU es un emulador de dispositivo que proporciona la interfaz en el módulo del kernel KVM y define el grupo de dispositivos virtuales que conforman la máquina virtual y se pasan para ser procesados ​​en el hardware físico.
* La API de libvirt es la API de virtualización estándar de la industria. Se utiliza para administrar y controlar la funcionalidad de QEMU, como la creación, el inicio, la detención y la migración de máquinas virtuales.
