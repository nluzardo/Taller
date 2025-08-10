1. ¿Qué es Ansible? Mencione dos actividades que se puedan hacer con Ansible

Es un motor open source que automatiza una gran cantidad de procesos informáticos, como la preparación de la infraestructura, la gestión de la configuración, la implementación de las aplicaciones y la organización de los sistemas.
Puede utilizarse para instalar software, automatizar tareas cotidianas, preparar elementos de infraestructura y de red, mejorar la seguridad y el cumplimiento normativo, aplicar parches a los sistemas y organizar flujos de trabajo complejos.

2. ¿Que es un playbook de Ansible?

Los playbooks de Ansible son listas de tareas que se ejecutan automáticamente en un inventario específico o en grupos de hosts. Se pueden combinar una o más tareas de Ansible para crear un play, un grupo ordenado de tareas asignados hosts determinados y las tareas se ejecutan en el orden en el que se escriben. El playbook puede incluir uno o más plays, así como funciones de Ansible.

3. ¿Que información contiene un inventario de Ansible?

Funciona con una lista de nodos o hosts administrados en la infraestructura, es decir, los servidores o dispositivos sobre los que se aplicarán las configuraciones utilizando un archivo de inventario. Al utilizar un archivo de inventario, Ansible puede administrar una gran cantidad de hosts con un solo comando. Los inventarios también le ayudan a utilizar Ansible de manera más eficiente al reducir la cantidad de opciones de línea de comandos que debe especificar.

4. Explique que es un módulo de Ansible y dé un ejemplo.

Las tareas se ejecutan por módulos, y cada uno de ellos lleva a cabo una de las tareas específicas que aparecen en el playbook. Los módulos contienen metadatos que determinan el momento y el lugar en los que se ejecuta una tarea, así como el usuario que lo hace. Los módulos pueden llevar a cabo funciones como las conexiones de red, la preparación de los sistemas, la seguridad, las comunicaciones, gestión de las nubes, los usuarios y las configuraciones. 

Ejemplo modulo user: Crea un usuario llamado "usuario" con una contraseña: 
Código
	- name: Crear un usuario llamado “usuario”
	user:
		name: usuario
		password: "{{ 'contraseña' }}"
5. ¿Que ventajas tiene Ansible sobre otros métodos de automatización?

Uno de los rasgos distintivos de Ansible es su capacidad para funcionar sin agentes adicionales instalados en los nodos gestionados. Esto significa que Ansible se comunica con los servidores a través de protocolos estándar, como SSH en sistemas Unix o WinRM en Windows, sin requerir software especial en cada máquina, simplificando la implementación como la carga de mantenimiento. La ausencia de agentes también mejora la seguridad, pues no se instalan componentes adicionales que puedan presentar vulnerabilidades.
