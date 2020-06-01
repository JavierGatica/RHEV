# Red Hat Virtualization 4 Foundations <h1>

## ¿Qué es la virtualización de Red Hat?

### Red Hat Enterprise Linux + KVM
* Soporte básico para hipervisor KVM
* Sin funciones de gestión de actualización empresarial
* Número limitado de máquinas virtuales permitidas
* Red Hat Virtualization se basa en Red Hat Enterprise Linux + KVM

### Red Hat Virtualization
* Gestión centralizada para el hipervisor KVM, así como recursos de cómputo, red y almacenamiento.
* Funciones empresariales para soportar aplicaciones de misión crítica

Red Hat Virtualization 4.0 ofrece funciones mejoradas de administración y automatización que permiten a los administradores de virtualización estandarizar procesos manuales y automatizar tareas que requieren mucho tiempo, al tiempo que obtienen visibilidad de las dependencias de infraestructura.

Red Hat Virtualization en realidad se basa en Red Hat Enterprise Linux: no puede existir sin Red Hat Enterprise Linux y KVM. Pero es importante comprender que la simple virtualización con Red Hat Enterprise Linux plus KVM proporciona solo lo básico, sin ninguna característica empresarial para cargas de trabajo de misión crítica.

Algunas fechas importantes en el historial del producto incluyen:

2006, cuando KVM fue aceptado en el kernel de Linux,

Enero de 2012, cuando se lanzó Red Hat Enterprise Virtualization 3.0 con un portal administrativo web de código abierto, y

En agosto de 2016, cuando salió la décima versión del producto, la versión 4.0, con un cambio de nombre a Red Hat Virtualization.
 
## Proceso de desarrollo.
Desde un alto nivel, todo el software de Red Hat sigue el modelo de "Participar, Integrar y Estabilizar".

Participa: en el mundo del código abierto, Red Hat desempeña un papel principal en muchos proyectos, como el kernel de Linux, la virtualización KVM, OpenStack, etc.

Integración: Red Hat patrocina e integra proyectos de código abierto en dos grandes proyectos de consolidación: Fedora, la base de Red Hat Enterprise Linux, y la comunidad de desarrolladores JBoss, la base de la cartera de productos Red Hat JBoss Middleware. Estos proyectos proporcionan entornos de trabajo gratuitos que se utilizan como laboratorios de desarrollo de software y campos de prueba para funciones que posteriormente pueden incorporarse a los productos comerciales de Red Hat. Red Hat también es el patrocinador principal de otros proyectos de consolidación en torno a la nube, el almacenamiento y la virtualización, así como muchos proyectos de consolidación más pequeños, que se muestran en la siguiente diapositiva.

Estabilizar: esta etapa es la creación de los productos empresariales de Red Hat. Este proceso implica más que simplemente recolectar proyectos maduros y de código abierto bien probados. Los proyectos se integran en productos completos listos para la empresa, creados con un gran ecosistema de soporte que incluye todo, desde socios hasta soporte, mantenimiento, documentación, capacitación, servicios de consultoría, certificaciones de hardware y software, etc. Red Hat se distingue de sus competidores por la integridad de su ecosistema y el trabajo de ingeniería de calidad que realiza, que incluye pruebas exhaustivas y actividades de preguntas y respuestas, certificaciones de hardware y software, y mantenimiento y soporte a largo plazo, de varios años: 10 años para la mayoría productos

El mantenimiento a largo plazo es una característica simple pero importante. Si se descubre un error de seguridad en un producto Red Hat de 5 años, Red Hat crea y entrega una solución. La solución puede ser transferida desde la base del código ascendente, o puede ser desarrollada recientemente. De cualquier manera, esta característica hace que los productos Red Hat sean adecuados para la implementación a largo plazo. Los proyectos de código abierto que han avanzado durante varios años generalmente no ofrecen parches para software antiguo. Por ejemplo, no puede obtener parches para versiones de 5 años de Fedora o la mayoría de los otros productos de código abierto como Ubuntu.
|
